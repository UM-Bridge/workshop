# UM-Bridge Workshop 2025

![UM-Bridge logo](/UM-bridge.png)

UM-Bridge is a language-agnostic interface linking Uncertainty Quantification (UQ) packages and numerical model software. It allows

* Speeding up UQ projects from prototype to HPC
* Making UQ and model software available to a wide audience
* Reproducible, community-driven UQ benchmarking

For more information, see [UM-Bridge documentation](https://um-bridge-benchmarks.readthedocs.io/en/docs/).

This workshop has the following goals:

* Get users familiar with UM-Bridge
* Initiate collaborations between UQ and model experts
* Advance the UQ software ecosystem

## Organizers

* Anne Reinarz [anne.k.reinarz@durham.ac.uk](mailto:anne.k.reinarz@durham.ac.uk)
* Chung Ming Loi [chung.m.loi@durham.ac.uk](chung.m.loi@durham.ac.uk)

## Time and Location

The workshop will be held online and span two half days:
* Tuesday, December 9 2025, 13:00 - 17:00 CET
* Wednesday, December 10 2025, 13:00 - 17:00 CET

## Registration

Registration is available through the [registration form](https://forms.gle/Xm4GZDuPttLW1Psf8).

## Prerequisites

For practical exercises, you will need working installations of
* docker (available at [docker.com](https://www.docker.com/))
* Python

## Schedule
Tuesday, 9. December 2025

| Time  | Session                                                                                       |
| ----- | --------------------------------------------------------------------------------------------- |
| 13:00 | Welcome                                                                                       |
| 13:05 | Anne Reinarz (Durham University): Introduction to UM-Bridge                                   |
| 13:40 | Practical: UM-Bridge basics / Participants' projects                                          |
| 14:20 | Alan Correa (RWTH Aachen): Intro containers, containerized UM-Bridge models/benchmarks |
| 14:40 | Practical: Containerized models / Participants' projects                                      |
| 15:00 | Coffee break                                                                                  |
| 15:30 | Chung Ming Loi (Durham University): UM-Bridge models in the cloud and on classical HPC              |
| 16:00 | Practical: UM-Bridge cloud + HPC / Participants' projects                                     |
| 17:00 | Wrap up                                                                                       |


Wednesday, 10. December 2025

| Time  | Session                                                                 |
| ----- | ----------------------------------------------------------------------- |
| 13:00 | Invited talk: William Hornsby, UKAEA                                    |
| | The use of turbulence surrogate models in plasma integrated modelling|
| 13:30 | Louise Kluge: Bayesian Inference in Expensive Models using MLDA and GP-Surrogates    |
|       | Vikas Kurapati: Fused ensembles of dynamic‑rupture earthquake simulations to accelerate Bayesian inference    |
| 14:00 | Short break / discussion                                                |
| 14:30 | Invited talk: Amal Mohammed A Alghamdi, Technical University of Denmark |
| | Bayesian inversion of CT data to characterize transport in the mouse ear |
| 15:00 | Alan Correa: Robustifying Model-Based Engineering Workflows: A Sustainable Approach to Manage Heterogeneity                                              |
|       | Juliette Dubois: Bayesian Inference for coupled acoustic-gravity systems |
| 15:30 | Coffee break                                                            |
| 16:00 | Lightning talks (various)                                                             |
| 16:20 | Invited Talk: Linus Seelinger, Pasteur Labs                             |
| 16:50 | Closing Remarks / Wrap-up                                               |

## Abstracts

#### Amal Mohammed A Alghamdi: Bayesian inversion of CT data to characterize transport in the mouse ear

Recent studies in rodents and humans show that gene therapy agents or tracers injected into the cerebrospinal fluid (CSF) reach the inner ear. The communication of fluid between the cochlear and the subarachnoid spaces of the brain has been controversial for decades. Observations of transport between the cochlea and the subarachnoid space contrast with the different composition of the fluids. The recent discovery of a membrane in the cochlear aqueduct raises further questions about the restrictions of transport between the compartments. This study aims to numerically quantify the diffusive and advective modes of transport of inert molecules from CSF to an intact cochlea. We use imaging data of the transport of a small tracer through the cochlear aqueduct in five sedated mice (8-week-old males). To estimate the transport model parameters, we formulate and solve a Bayesian inverse problem in which we allow the diffusivity to vary in the presence of potential membranes. We also discuss how modeling choices affect the inference. We carry out the implementation using the software tool CUQIpy (Computational Uncertainty Quantification for Inverse Problems in Python). In this talk we also introduce CUQIpy-UMBridge plugin which allows CUQIpy models and distributions to be served via an Um-Bridge server.

#### William Hornsby: The use of turbulence surrogate models in plasma integrated modelling

Abstract: Plasma micro-turbulence is one of the dominant transport mechanisms of heat from the core of a fusion power plant. Direct numerical calculation of the micro-instabilities that form turbulence is computationally expensive and is a significant bottleneck in integrated plasma modelling, in which the many physical processes are coupled to predict reactor-level behaviour and to optimise operational scenarios of fusion power plants. The considerable number of geometric and thermodynamic parameters, the interactions that influence the turbulence and the resolutions needed to accurately resolve these turbulent modes, makes direct numerical simulation for parameter space exploration computationally extremely challenging. However, this makes it suitable for surrogate modelling, where speed ups of up to 105 are possible making rapid scenario development a possibility. In this talk the integrated plasma modelling use-case will be introduced as well as the turbulence surrogate modelling efforts at UKAEA, including how the models are integrated into larger workflows.


#### Alan Correa: Robustifying Model-Based Engineering Workflows: A Sustainable Approach to Manage Heterogeneity

Model-based development, design, decision support, and diagnostics in engineering applications often require complex workflows. These workflows involve heterogeneity across their components: data, computational models, analysis techniques, compute environments -- including programming languages, operating systems, and hardware platforms -- and importantly, humans who bring diverse skill sets and preferred tools. Building robust, agile, and scalable end-to-end model-based workflows thus presents a significant challenge, limiting the usability and subsequent reusability of the generated digital assets, including software, data and workflows.

We present SHOWME.how -- A solution to heterogeneous workflows in model-based engineering applications based on three key pillars: Isolation, Interoperation, and Orchestration. Firstly, we isolate computational units using technologies like cross-platform package managers (e.g., Conda, Mamba) and containerization (e.g., Docker, Aptainer). Secondly, we enable these computational units to interoperate with each other and exchange data through language-agnostic file formats (e.g., JSON, HDF5, Zarr) for data interchange and platform-agnostic transfer protocols (e.g., HTTP, S3) for data exchange. 
An exemplary implementation is UM-Bridge, which enables cross-language interoperability via HTTP and JSON while providing a streamlined interface for coupling model codes with uncertainty quantification libraries. Lastly, we orchestrate the computational units along with the data using modern graph-based workflow managers (e.g., Nextflow or Snakemake). Such an approach not only enhances the combined value of individual workflow components through synergy, but also enables the reuse of existing research software, or parts of it, in its native environment, eliminating the need to build wrappers, develop language-bridging interfaces, or rely on suboptimal implementations. Ultimately, this facilitates the rapid and seamless integration of state-of-the-art research methodologies into application-driven engineering tasks.



#### Vikas Kurapati: Fused ensembles of dynamic‑rupture earthquake simulations to accelerate Bayesian inference  

Understanding earthquake dynamics is essential for seismic hazard assessment and risk mitigation. 
In this context, Bayesian inference yields valuable insights into model parameters through a combination of simulation models and real-world data. 
Such Bayesian parameter inference with uncertainty quantification (UQ) requires numerous simulation runs and is therefore often computationally out of reach.
Already a single high-fidelity earthquake simulation -- governed by a linear hyperbolic seismic wave equation coupled nonlinearly to a friction law -- is computationally expensive. 
In this study, we investigate the use of fused ensemble simulations as a means to accelerate large earthquake simulation workflows and UQ studies. 
Via fused ensembles, we turn the element-local small sparse/ dense matrix operations into tensor contractions working on a dense rank-3 tensor and sparse matrices. 
These are executed with better computational efficiency on CPUs, due to better exploitation of SIMD instructions.
We implement and evaluate this approach in SeisSol, a high-performance computing software for simulation of complex earthquake events, which implements an Arbitrary high-order DERivative Discontinuous Galerkin (ADER-DG) scheme.
Our results demonstrate that fused simulations can be up to 4.56 times faster than with single execution -- though depending strongly on discretization order, size of the problem and compute architecture.   For a full UQ example workflow, we demonstrate savings of 35% of node hours for the entire workflow.
