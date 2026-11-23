---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 4
---

<!-- To update the CV, replace assets/pdf/cv.pdf with the new PDF (keep the same file name). -->

{% assign cv_pdf = '/assets/pdf/cv.pdf' | relative_url %}

<p>
  <a class="btn btn-sm z-depth-0" href="{{ cv_pdf }}" target="_blank" rel="noopener noreferrer">
    <i class="fa-solid fa-file-pdf"></i> Open or download the PDF
  </a>
</p>

<div id="cv-pages" class="cv-pages" data-pdf="{{ cv_pdf }}">
  <p class="cv-status">Loading CV…</p>
</div>

<noscript>
  <p>Your browser has JavaScript turned off, so the CV can't be shown here. <a href="{{ cv_pdf }}">Open the CV as a PDF</a>.</p>
</noscript>

<style>
  .cv-pages canvas {
    display: block;
    width: 100%;
    height: auto;
    margin: 0 auto 1.5rem;
    background: #fff;
    border-radius: 4px;
    box-shadow: 0 1px 6px rgba(0, 0, 0, 0.15);
  }
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
<script>
  (function () {
    var container = document.getElementById('cv-pages');
    var url = container.getAttribute('data-pdf');
    var status = container.querySelector('.cv-status');

    function fail() {
      status.innerHTML = 'The CV could not be displayed here. <a href="' + url + '">Open the CV as a PDF</a>.';
    }
    if (!window.pdfjsLib) return fail();

    pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';

    var pdfDoc = null;
    var renderedWidth = 0;

    function renderAll() {
      var width = container.clientWidth;
      if (!pdfDoc || !width || Math.abs(width - renderedWidth) < 40) return;
      renderedWidth = width;
      var ratio = window.devicePixelRatio || 1;
      container.querySelectorAll('canvas').forEach(function (c) { c.remove(); });

      var chain = Promise.resolve();
      for (var n = 1; n <= pdfDoc.numPages; n++) {
        (function (pageNum) {
          var canvas = document.createElement('canvas');
          canvas.setAttribute('role', 'img');
          canvas.setAttribute('aria-label', 'CV page ' + pageNum + ' of ' + pdfDoc.numPages);
          container.appendChild(canvas);
          chain = chain.then(function () {
            return pdfDoc.getPage(pageNum).then(function (page) {
              var base = page.getViewport({ scale: 1 });
              var viewport = page.getViewport({ scale: (width / base.width) * ratio });
              canvas.width = viewport.width;
              canvas.height = viewport.height;
              return page.render({ canvasContext: canvas.getContext('2d'), viewport: viewport }).promise;
            });
          });
        })(n);
      }
      return chain;
    }

    pdfjsLib.getDocument(url).promise.then(function (doc) {
      pdfDoc = doc;
      status.remove();
      return renderAll();
    }).catch(fail);

    var resizeTimer;
    window.addEventListener('resize', function () {
      clearTimeout(resizeTimer);
      resizeTimer = setTimeout(renderAll, 250);
    });
  })();
</script>
