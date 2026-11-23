---
layout: page
permalink: /research/
title: research
nav: true
nav_order: 1
---

Our research is spanned by three partially overlapping dimensions:

- **Neural theory** to understand how the circuitry and learning rules of motor regions generate behavior.
- **Advanced neural and behavioral data analysis** in close collaboration with experimentalists.
- **Development of rigorously grounded data-driven methods** to identify latent structure in high-dimensional data.

<div class="research-fig research-fig--narrow">
  {% include figure.liquid loading="eager" path="assets/img/research/fig1.png" class="img-fluid" alt="Venn diagram of neural theory, data analysis and data-driven methods" %}
</div>

We use a variety of quantitative tools, from traditional methods in dynamical systems to more recent tools in machine learning.

<div class="research-icons">
  {% include figure.liquid loading="eager" path="assets/img/research/fig2.png" class="img-fluid" alt="Feedforward neural network" caption="machine learning" %}
  {% include figure.liquid loading="eager" path="assets/img/research/fig2_2.png" class="img-fluid" alt="Phase portrait of a dynamical system" caption="dynamical systems" %}
  {% include figure.liquid loading="eager" path="assets/img/research/fig2_3.png" class="img-fluid" alt="Clustered data points" caption="statistical modeling" %}
</div>

Below you can find a non-exhaustive list of our research interests.

---

## Evolution of neural dynamics over learning

Neural circuits perform complex tasks through recurrently generated dynamics. How do these dynamic modes evolve over the course of learning, and how can we identify these changes from data recorded over learning?

<div class="research-fig">
  {% include figure.liquid loading="eager" path="assets/img/research/fig3.png" class="img-fluid" alt="Neural trajectories in a low-dimensional subspace before and after learning" %}
</div>

<div class="related-pubs" markdown="1">

**Related publications**

- H Gurnani, NA Cayco-Gajic. [Signatures of task learning in neural representations](https://www.sciencedirect.com/science/article/abs/pii/S0959438823000843). _Current Opinion in Neurobiology_ 83, 102759. ([pdf](https://drive.google.com/file/d/1ZFVVVTRfUYqHTWImeZEzQAboW9uq_vUw/view))
- A Pellegrino, NA Cayco-Gajic\*, A Chadwick\*. [Low tensor rank learning of neural dynamics](https://proceedings.neurips.cc/paper_files/paper/2023/file/27030ad2ec1d8f2c3847a64e382c30ca-Paper-Conference.pdf). _Advances in Neural Information Processing Systems_ 37.

</div>

## Dimensionality reduction and neural manifolds

Neural manifolds reflect task-relevant information that is often not visible in single-neuron activity. How can we develop new dimensionality reduction methods that extend the classic view that task-relevant information is embedded in low-dimensional neural subspaces while remaining (mathematically) interpretable?

<div class="research-fig">
  {% include figure.liquid loading="eager" path="assets/img/research/fig4.png" class="img-fluid" alt="Slice tensor decomposition of a neuron by time by trials data tensor" %}
</div>

<div class="related-pubs" markdown="1">

**Related publications**

- A Pellegrino\*, H Stein\*, NA Cayco-Gajic. [Dimensionality reduction beyond neural subspaces with slice tensor component analysis](https://www.nature.com/articles/s41593-024-01626-2). _Nature Neuroscience_ 27, 1199–1210.
- A Pellegrino, NA Cayco-Gajic\*, A Chadwick\*. [Low tensor rank learning of neural dynamics](https://proceedings.neurips.cc/paper_files/paper/2023/file/27030ad2ec1d8f2c3847a64e382c30ca-Paper-Conference.pdf). _Advances in Neural Information Processing Systems_ 37.
- F Lanore\*, NA Cayco-Gajic\*, H Gurnani, D Coyle, RA Silver. [Cerebellar granule cell axons support high-dimensional representations](https://www.nature.com/articles/s41593-021-00873-x). _Nature Neuroscience_ 24, 1142–1150.

</div>

## Theories of cerebellar learning

Because of its largely feedforward, relatively homogenous architecture and supervised learning signals, the cerebellar cortex has been hypothesized to perform pattern separation by projecting input patterns into a high-dimensional space, as in a multilayer perceptron. How well do these classic theories fit new experimental data? How can they be extended to understand how the cerebellum learns in coordination with other motor regions?

<div class="research-fig">
  {% include figure.liquid loading="eager" path="assets/img/research/fig5.png" class="img-fluid" alt="Cerebellar granule cell expansion and error-based supervised learning at the Purkinje cell" %}
</div>

<div class="related-pubs" markdown="1">

**Related publications**

- L Agueci, NA Cayco-Gajic. (2025) Distributed learning across fast and slow neural systems supports efficient motor adaptation. ([bioRxiv](https://www.biorxiv.org/content/biorxiv/early/2025/06/01/2025.06.01.657238.full.pdf))
- F Lanore\*, NA Cayco-Gajic\*, H Gurnani, D Coyle, RA Silver. (2021) [Cerebellar granule cell axons support high-dimensional representations](https://www.nature.com/articles/s41593-021-00873-x). _Nature Neuroscience_ 24, 1142–1150.
- NA Cayco-Gajic, RA Silver. (2019) [Re-evaluating circuit mechanisms underlying pattern separation](https://www.sciencedirect.com/science/article/abs/pii/S0896627319300716). _Neuron_ 101 (4), 584–602.
- NA Cayco-Gajic, C Clopath, RA Silver. (2017) [Sparse synaptic connectivity is required for decorrelation and pattern separation in feedforward networks](https://www.nature.com/articles/s41467-017-01109-y). _Nature Communications_ 8 (1), 1116.

</div>

## Learning during complex behaviours

Classic motor learning studies often consider simple behaviors in which variability is constrained as much as possible. But naturalistic behavior is characterized by a combination of spontaneously transitioning motor actions and continuous kinematics. How can we develop new behavioral models that can disentangle these sources of variability to understand the neural control of behavior in complex learning paradigms?

<div class="research-fig">
  {% include figure.liquid loading="eager" path="assets/img/research/fig6.png" class="img-fluid" alt="Interlimb coordination of mouse forelimbs during locomotion" %}
</div>

<div class="related-pubs" markdown="1">

**Related publications**

- A Andrianarivelo, H Stein, J Gabillet, C Batifol, A Jalil, NA Cayco-Gajic, M Graupner. (2023) Cerebellar interneuron activity is triggered by reach endpoint during learning of a complex locomotor task. ([bioRxiv](https://www.biorxiv.org/content/10.1101/2023.10.10.561690v2.abstract))
- H Stein, A Andrianarivelo, J Gabillet, C Batifol, A Jalil, M Graupner, NA Cayco Gajic. The emergence of fixed points in interlimb coordination underlies the learning of stable gaits in mice. (In preparation; see an early version in Heike's Cosyne 2022 talk [here](https://www.youtube.com/watch?v=DvsflwKOWs0&t=10967s).)

</div>

<style>
  .research-fig { margin: 1.25rem auto; }
  .research-fig--narrow { max-width: 50%; }
  .research-fig figure, .research-icons figure { margin: 0; }
  .research-icons {
    display: flex;
    gap: 1.25rem;
    justify-content: center;
    align-items: flex-start;
    text-align: center;
    margin: 1.25rem 0 1.75rem;
  }
  .research-icons > * { flex: 1 1 0; min-width: 0; }
  .research-icons figcaption { margin-top: 0.4rem; }
  .related-pubs {
    background: #f6f6f6;
    border-radius: 6px;
    padding: 0.9rem 1.25rem 0.3rem;
    margin: 1rem 0 2.25rem;
  }
  .related-pubs p { margin-bottom: 0.5rem; }
  .related-pubs ul { padding-left: 1.2rem; }
  .related-pubs li { margin-bottom: 0.5rem; }
  html[data-theme="dark"] .related-pubs { background: rgba(255, 255, 255, 0.06); }
  @media (max-width: 576px) {
    .research-fig--narrow { max-width: 80%; }
    .research-icons { gap: 0.6rem; }
  }
</style>
