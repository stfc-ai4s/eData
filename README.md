<img src="./sciml_bench/docs/markdown/resources/logo.png" alt="logo" width="500"/>



# SciML-Bench: Table of Contents
- [1. Synopsis](#1-synopsis)
- [2. Benchmark Suite](#2-benchmark-suite)
  * [2.1 Organisation](#21-organisation)
  * [2.2 Features](#22-features)
  * [2.3 Benchmarks and Datasets](#23-benchmarks-and-datasets)
- [3. Installation and Usage](#3-installation-and-usage)
- [4. Citation](#4-citation)
- [5. Acknowledgments](#5-acknowledgments)



# 1. Synopsis

Benchmarking is a valuable tool in computational science that allows effective comparison of software and/or hardware systems.  With the rise of machine learning and AI, the need for benchmarking AI algorithms is  increasing. The SciMLBench is aimed at the ‘*AI for Science*’ research community.  

With an ever-growing number of machine learning models and algorithms, a range of scientific problems, and the proliferation of AI systems, the development of cutting-edge ML/AI algorithms requires a detailed understanding of all of these aspects as well as effective mechanisms for measuring their effectiveness.

The SciML-Bench toolkit aims to provide such mechanisms. It is an open-source initiative and covers a range of scientific problems from various domains of science, including materials, life and environmental scienceS, as well as particle physics and astronomy. The benchmarks are implemented in Python and rely on one or more machine learning frameworks, such as TensorFlow, PyTorch or SciKit-Learn.

The overarching purpose of this initiative is to support the ‘*AI for Science*’ community in the development of more powerful, robust and understandable machine learning solutions.


# 2. Benchmark Suite 


## 2.1 Organisation

The suite has three components, namely, 

1. **Benchmarks**: In our case, a benchmark is a machine learning application performing a specific scientific task, written in Python. These are included as part of the distribution, and can be found inside the [benchmarks](./sciml_bench/benchmarks/) directory. In the scale of *micro-apps*, *mini-apps*, and *apps*, benchmarks are full-fledged applications.

2. **Datasets**: Each benchmark in (1) relies on one or more datasets, for example for training and/or inference. These datasets are open, task- or domain-specific, and FAIR compliant. Most of these datasets being large, they are hosted separately,  on one of the servers (or mirrors), and are downloaded separately on demand. The framework (see (3)), supports manual downloading of these datasets. 

3. **Framework**:  The framework serves two purposes: first, at the user level, it facilitates an easier approach to benchmarking, logging and reporting of the results. Secondly, at the developer level, it provides a coherent API for unifying and simplifying the development of AI benchmarks. Sources related to the framework can be found inside the [core](./sciml_bench/core/) directory. 

The source tree, which captures these aspects,  is organised as follows:

```bash
├── README.md                   <This file>
└── sciml_bench/                <Root folder for the framework and benchmarks>
    ├── core/                   <Core scripts> 
    └── docs/                   <Main documentation folder>
        ├── full/               <Full HTML documentation> 
        ├── benchmarks/         <Documentation on benchmarks>
        ├── datasets/           <Documentation on datasets>
        ├── resources/          <image and other resources for documentation> 
    ├── benchmarks/             <Benchmark sources> 
    |   └──.../                 <Various benchmarks>
    └── etc/                    <Extra core files>
        ├── configs/            <Configuration files> 
        ├── recipes/            <Container and other recipes>
        └── templates/          <Template files> 

```

We have annotated the purpose of each folder/directory within `<>`.  

## 2.2 Features 

A typical user-base for the benchmarking framework may cover a broad spectrum of user communities, such as system manufacturers and integrators (for assessing system performance), scientists (for developing new algorithms), and computer scientists  or ML enthusiasts (for understanding the basics of various machine learning models and algorithms). It is a challenging task to design for and cover all these requirements in a single framework. Here, with SciML-Bench, we have attempted to cover these requirements through the following set of features:

* Very flexible, customisable and lightweight framework,
* Powerful logging and monitoring capabilities, 
* Support for multiple machine learning frameworks (TensorFlow, PyTorch, Apache MXNet, and SciKit-Learn), 
* Simplified application programming interface (API), to support easier development of benchmarks, 
* Fully customisable installation, 
* Simplified use of framework that encourages a wide range of users, and
* Fully decoupled, on-demand, and user-initiated data downloads. 



## 2.3 Benchmarks and Datasets 
The number of datasets and benchmarks may vary with every release. Please consult the [Benchmarks](./sciml_bench/docs/markdown/benchmarks_summary.md) and  [Datasets](./sciml_bench/docs/markdown/datasets_summary.md) documents for more details. You can also check out the full documentation [here](./sciml_bench/docs/). A number of authors have contributed towards the development of the benchmarks,  and these contributions are stated in [Credits](./sciml_bench/docs/markdown/credits.md). If you are thinking of contributing towards the benchmarks or datasets, please see the [Contributing Datasets & Benchmarks](./sciml_bench/docs/markdown/main/contributing.md).



# 3. Installation and Usage

Please consult  [Installation](./sciml_bench/docs/markup/main/installation.md) and [Usage](./sciml_bench/docs/markup/main/usage.md)for getting started. The [Frequently Asked Questions (FAQ)](./sciml_bench/docs/markup/main/faq.md) covers a number of installation issues. We have also included a short [tutorial](./sciml_bench/docs/markup/main/tutorial.md) on installing and using the framework. 



# 4. Citation 

Cite this benchmark suite as follows:

    ```
    @misc{scimlbench:2021,
        title  = {SciML-Bench: A Benchmarking Suite for AI for Science},
        author = {Jeyan Thiyagalingam, Juri Papay, Kuangdai Leng, Samuel Jackson, Mallikarjun Shankar, Geoffrey Fox,  Tony Hey},
        url    = {https://github.com/stfc-sciml/sciml-bench},
        year   = {2021}
    }
    ```

# 5. Publications

 - B Henghes, J Thiyagalingam, T Hey, & O Lahav, Benchmarking and Scalability of Machine Learning Methods for Photometric Redshift Estimation, Monthly Notices of Royal Astronomical Society (MNRAS), 2021.
 - B Henghes, J Thiyagalingam, T Hey, & O Lahav, Deep Learning Methods for Obtaining Photometric Redshift Estimations from Images, Monthly Notices of Royal Astronomical Society (MNRAS), 2022.
 - J Thiyagalingam, M Shankar, G Fox,  T Hey, Scientific Machine Learning Benchmarks, Nature Reviews Physics, 2022
 - J Thiyagalingam et. al.,  AI Benchmarking for Science: Efforts from the MLCommons Science Working Group, In: Anzt, H., Bienz, A., Luszczek, P., Baboulin, M. (eds), High Performance Computing. ISC High Performance 2022 International Workshops. ISC High Performance 2022. Lecture Notes in Computer Science (13387). Springer,
 - L Lucie-Smith, H V Peiris,  A Pontzen,  B Nord,  J Thiyagalingam,  D Piras, Discovering the building blocks of dark matter halo density profiles with neural networks, Physical Review D, 105(10), American Physical Society, 2022


# 6. Acknowledgments

This benchmarking programme is supported by [1] Wave I of the UKRI Strategic Priorities Fund under the EPSRC grant (EP/T001569/1), particularly the AI for Science theme in that grant and the Alan Turing Institute, [2] the Benchmarking for AI for Science at Exascale (BASE), EPSRC ExCALIBUR Phase I grant (EP/V001310/1), and [3] the Blueprinting for AI for Science at Exascale (BASE-II, EP/X019918/1), which is Phase II of the [2].

<div style="text-align: right">◼︎</div>
