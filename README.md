# Test-Time-Adaptation-for-Graph-Learning
Graph distribution shifts between training and test graphs pose severe challenges to the generalization of graph neural networks (GNNs). In real-world deployment, application environments are continuously evolving, while retraining or redesigning GNNs is often costly and impractical. In light of this, **test-time adaptation on graphs**, which aims to dynamically adapt well-trained GNNs or adjust test graphs to improve inference performance, has attracted growing attention as a practical solution. In this survey, we provide a comprehensive review of test-time adaptation on graphs, an emerging yet underexplored research direction. We identify two fundamental challenges: (1) **Data-level**: *complex graph distribution shifts*; and (2) **Model-level**: *limited test-time learning information*. Upon this, we present a systematic taxonomy of existing methods into (a) model-centric, (b) data-centric, and (c) hybrid methods, followed by a summary of representative applications, benchmarks, and open opportunities. We aim to bridge the gap between laboratory GNN development and real-world deployment via test-time adaptation.

## Overview

The outline corresponds to the taxonomy in our survey paper.
 
- [1. Model-Centric TTA Methods on Graphs](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#1-Model-Centric-TTA-Methods-on-Graphs)
  - [1.1 Full Model Fine-Tuning](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#11-Full-Model-Fine-Tuning)
  - [1.2 Adapter-Based Model Learning](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#12-Adapter-Based-Model-Learning)
  - [1.3 Joint Model-Adapter Learning](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#13-Joint-Model-Adapter-Learning)
- [2. Data-Centric TTA Methods on Graphs](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#2-Data-Centric-TTA-Methods-on-Graphs)
  - [2.1 Additive Graph Refinement](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#21-Additive-Graph-Refinement)
  - [2.2 Reconstructive Graph Adaptation](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#22-Reconstructive-Graph-Adaptation)
- [3. Hybrid TTA Methods on Graphs](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#3-Hybrid-TTA-Methods-on-Graphs)
- [4. Application Scenarios](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#4-Application-Scenarios)
  - [4.1 Test-Time GNN Model Evaluation](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#41-Test-Time-GNN-Model-Evaluation)
  - [4.2 Test-Time Graph OOD & Anomaly Detection](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#42-Test-Time-Graph-OOD--Anomaly-Detection)
  - [4.3 Test-Time Graph Learning for Social Benefits](https://github.com/jiayichen1121/Test-Time-Adaptation-for-Graph-Learning#43-Test-Time-Graph-Learning-for-Social-Benefits)


## Literature

### 1. Model-Centric TTA Methods on Graphs

#### 1.1 Full Model Fine-Tuning

<table>
<thead>
  <tr>
    <th>Taxonomy</th>
    <th>Name</th>
    <th>Title</th>
    <th>Venue</th>
    <th>Paper</th>
    <th>Code</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="5"><br><br><br>Latent Feature <br>Space-Oriented <br>Fine-Tuning</td>
    <td>GT3</td>
    <td>Test-Time Training for Graph Neural Networks</td>
    <td>arXiv 2022</td>
    <td><a href="https://arxiv.org/pdf/2210.08813">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>HomoTTT</td>
    <td>A Fully Test-time Training Framework for Semi-supervised Node Classification on Out-of-Distribution Graphs</td>
    <td>TKDD 2024</td>
    <td><a href="https://dl.acm.org/doi/epdf/10.1145/3649507">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>TARD</td>
    <td>Out-of-distribution Rumor Detection via Test-Time Adaptation</td>
    <td>arXiv 2024</td>
    <td><a href="https://arxiv.org/pdf/2403.17735">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>IGT</td>
    <td>Test-Time Training with Invariant Graph Learning for Out-of-Distribution Generalization</td>
    <td>SSRN 2024</td>
    <td><a href="https://iopscience.iop.org/article/10.1088/2631-8695/ae2781/pdf">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>MATCHA</td>
    <td>Matcha: Mitigating Graph Structure Shifts with Test-Time Adaptation</td>
    <td>ICLR 2025</td>
    <td><a href="https://arxiv.org/pdf/2410.06976">[PDF]</a></td>
    <td><a href="https://github.com/baowenxuan/Matcha">[Torch]</a></td>
  </tr>
  <tr>
    <td>Graph Learning <br>Task-Oriented</td>
    <td>LLMTTT</td>
    <td>Test-Time Training on Graphs with Large Language Models (LLMs)</td>
    <td>MM 2024</td>
    <td><a href="https://dl.acm.org/doi/pdf/10.1145/3664647.3680865">[PDF]</a></td>
    <td><a href="https://github.com/Vanessa-ZZZ/LLMTTT">[Torch]</a></td>
  </tr>
  <tr>
    <td rowspan="3"><br><br>Fully <br>Fine-Tuning</td>
    <td>SOGA</td>
    <td>Source Free Graph Unsupervised Domain Adaptation</td>
    <td>WSDM 2024</td>
    <td><a href="https://dl.acm.org/doi/pdf/10.1145/3616855.3635802">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>PROGRAM</td>
    <td>PROGRAM: PROtotype GRAph Model based Pseudo-Label Learning for Test-Time Adaptation</td>
    <td>ICLR 2024</td>
    <td><a href="https://openreview.net/pdf?id=x5LvBK43wg">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>DT3OR</td>
    <td>Dual Test-Time Training for Out-of-Distribution Recommender System</td>
    <td>TKDE 2025</td>
    <td><a href="https://dl.acm.org/doi/10.1109/TKDE.2025.3548160">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
</tbody>
</table>

#### 1.2 Adapter-Based Model Learning 

|          Taxonomy         |  Name |                        Title                       |    Venue   |                  Paper                  |                          Code                          |
|:-------------------------:|:-----:|:--------------------------------------------------:|:----------:|:---------------------------------------:|:------------------------------------------------------:|
| Ahead Well-Trained Model  | GADT3 | Cross-Domain Graph Anomaly Detection via Test-Time |  TMLR 2025 | [PDF](https://arxiv.org/pdf/2502.14293) | [Torch](https://github.com/delaramphf/GADT3-Algorithm) |
| Behind Well-Trained Model |  TSA  | Training with Homophily-Guided Self-Supervision    | arXiv 2025 | [PDF](https://arxiv.org/pdf/2502.18334) |        [Torch](https://github.com/Graph-COM/TSA)       |


#### 1.3 Joint Model-Adapter Learning

|  Name  |                                              Title                                              |        Venue       |                      Paper                      |                      Code                      |
|:------:|:-----------------------------------------------------------------------------------------------:|:------------------:|:-----------------------------------------------:|:----------------------------------------------:|
|  GAPGC | GraphTTA: Test Time Adaptation on Graph Neural Networks                                         | ICML 2022 Workshop |     [PDF](https://arxiv.org/pdf/2208.09126)     |                      [N/A]                     |
| ASSESS | Test-time Adaptation on Graphs via Adaptive Subgraph-based Selection and Regularized Prototypes |      ICML 2025     | [PDF](https://openreview.net/pdf?id=lC40m2jjUO) | [Torch](https://github.com/YushengZhao/ASSESS) |
|  GCAL  | GCAL: Adapting Graph Models to Evolving Domain Shifts                                           |      ICML 2025     | [PDF](https://openreview.net/pdf?id=zVBYbjjlMX) |     [Torch](https://github.com/joe817/GCAL)    |


### 2. Data-Centric TTA Methods on Graphs

#### 2.1 Additive Graph Refinement

|     Name     |                                                Title                                               |     Venue    |                                                          Paper                                                          |                        Code                       |
|:------------:|:--------------------------------------------------------------------------------------------------:|:------------:|:-----------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------:|
|    GTrans    | Empowering Graph Representation Learning with Test-Time Graph Transformation                       |   ICLR 2023  |                                     [PDF](https://openreview.net/pdf?id=Lnxl5pr018)                                     |  [Torch](https://github.com/ChandlerBang/GTrans)  |
|     GOAT     | Map to Optimal: Adapting Graph Out-of-Distribution in Test Time                                    |       -      |                                     [PDF](https://openreview.net/pdf?id=6j0oKBo196)                                     |                       [N/A]                       |
|     AAGOD    | A data-centric framework to endow graph neural networks with out-of-distribution detection ability |   KDD 2023   |                                [PDF](https://dl.acm.org/doi/pdf/10.1145/3580305.3599244)                                |    [Torch](https://github.com/BUPT-GAMMA/AAGOD)   |
| Graphpatcher | GRAPHPATCHER: mitigating degree bias for graph neural networks via test-time augmentation          | NeurIPS 2023 | [PDF](https://proceedings.neurips.cc/paper_files/paper/2023/file/ae9bbdcea94d808882f3535e8ca00542-Paper-Conference.pdf) | [Torch](https://github.com/jumxglhf/GraphPatcher) |


#### 2.2 Reconstructive Graph Adaptation




### 3. Hybrid TTA Methods on Graphs






### 4. Application Scenarios

#### 4.1 Test-Time GNN Model Evaluation




#### 4.2 Test-Time Graph OOD & Anomaly Detection




#### 4.3 Test-Time Graph Learning for Social Benefits




## Datasets

### 📌 Feature/Structural Shift Datasets


---

### 📌 Domain Shift Datasets

---

### 📌 Temporal Shift Datasets
