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

### 📌1. Model-Centric TTA Methods on Graphs

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
    <td rowspan="5"><br><br>Latent Feature <br>Space-Oriented <br>Fine-Tuning</td>
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


### 📌2. Data-Centric TTA Methods on Graphs

#### 2.1 Additive Graph Refinement

|     Name     |                                                Title                                               |     Venue    |                                                          Paper                                                          |                        Code                       |
|:------------:|:--------------------------------------------------------------------------------------------------:|:------------:|:-----------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------:|
|    GTrans    | Empowering Graph Representation Learning with Test-Time Graph Transformation                       |   ICLR 2023  |                                     [PDF](https://openreview.net/pdf?id=Lnxl5pr018)                                     |  [Torch](https://github.com/ChandlerBang/GTrans)  |
|     GOAT     | Map to Optimal: Adapting Graph Out-of-Distribution in Test Time                                    |       -      |                                     [PDF](https://openreview.net/pdf?id=6j0oKBo196)                                     |                       [N/A]                       |
|     AAGOD    | A data-centric framework to endow graph neural networks with out-of-distribution detection ability |   KDD 2023   |                                [PDF](https://dl.acm.org/doi/pdf/10.1145/3580305.3599244)                                |    [Torch](https://github.com/BUPT-GAMMA/AAGOD)   |
| Graphpatcher | GRAPHPATCHER: mitigating degree bias for graph neural networks via test-time augmentation          | NeurIPS 2023 | [PDF](https://proceedings.neurips.cc/paper_files/paper/2023/file/ae9bbdcea94d808882f3535e8ca00542-Paper-Conference.pdf) | [Torch](https://github.com/jumxglhf/GraphPatcher) |


#### 2.2 Reconstructive Graph Adaptation

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
    <td rowspan="2"><br>Feature-Level <br>Reconstruction</td>
    <td>Yang et al.</td>
    <td>Control the GNN: Utilizing Neural Controller with Lyapunov Stability for Test-Time Feature Reconstruction</td>
    <td>arXiv 2024</td>
    <td><a href="https://arxiv.org/pdf/2410.09708">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>FR-GNN</td>
    <td>FRGNN: Mitigating the Impact of Distribution Shift on Graph Neural Networks via Test-Time Feature Reconstruction</td>
    <td>IEEEIOT2024</td>
    <td><a href="https://arxiv.org/pdf/2308.09259">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td rowspan="3"><br>Joint Feature &amp; Structure <br>Reconstruction</td>
    <td>GOODAT</td>
    <td>GOODAT: Towards Test-time Graph Out-of-Distribution Detection</td>
    <td>AAAI 2024</td>
    <td><a href="https://arxiv.org/pdf/2401.06176">[PDF]</a></td>
    <td><a href="https://github.com/Ee1s/GOODAT">[Code]</a></td>
  </tr>
  <tr>
    <td>TT-GREB</td>
    <td>Test-Time Graph Rebirth: Serving GNN Generalization Under Distribution Shifts</td>
    <td>ICDM 2025</td>
    <td><a href="https://openreview.net/pdf?id=rW3NVhKtQ2">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>TTA-GREC</td>
    <td>Test-time adaptation on recommender system with data-centric graph transformation</td>
    <td>AAAI 2025</td>
    <td><a href="https://www.ijcai.org/proceedings/2025/0510.pdf">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>Generative Reconstruction</td>
    <td>TT-GNDS</td>
    <td>Test-Time Graph Neural Dataset Search With Generative Projection</td>
    <td>ICML 2025</td>
    <td><a href="https://openreview.net/pdf?id=824TCt6CkE">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
</tbody>
</table>


### 📌3. Hybrid TTA Methods on Graphs

|   Name   |                                          Title                                          |    Venue   |                           Paper                           |                       Code                       |
|:--------:|:---------------------------------------------------------------------------------------:|:----------:|:---------------------------------------------------------:|:------------------------------------------------:|
| GraphCTA | Collaborate to Adapt: Source-Free Graph Domain Adaptation via Bi-directional Adaptation |  WWW 2024  | [PDF](https://dl.acm.org/doi/pdf/10.1145/3589334.3645507) | [Torch](https://github.com/cszhangzhen/GraphCTA) |
|   IGFT   | 3D Test-time Adaptation via Graph Spectral Driven Point Shift                           | arXiv 2025 |          [PDF](https://arxiv.org/pdf/2507.18225)          |                       [N/A]                      |




### 📌4. Application Scenarios

#### 4.1 Test-Time GNN Model Evaluation

|     Name     |                                   Title                                  |    Venue    |                                                          Paper                                                          |                          Code                         |
|:------------:|:------------------------------------------------------------------------:|:-----------:|:-----------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------:|
| GNNevaluator | GNNEvaluator: evaluating GNN performance on unseen graphs without labels | NeurIPS2023 | [PDF](https://proceedings.neurips.cc/paper_files/paper/2023/file/6a55f024db3f771194bdadc8f3a35381-Paper-Conference.pdf) | [Torch](https://github.com/Amanda-Zheng/GNNEvaluator) |
|     LeBed    | Online GNN Evaluation Under Test-Time Graph Distribution Shifts          |  ICLR 2024  |                                     [PDF](https://openreview.net/pdf?id=KbetDM33YG)                                     |     [Torch](https://github.com/Amanda-Zheng/LEBED)    |
| DYGevaluator | Test-time GNN Model Evaluation on Dynamic Graphs                         |  ICDM 2025  |                                         [PDF](https://arxiv.org/pdf/2509.23816)                                         |                         [N/A]                         |


#### 4.2 Test-Time Graph OOD & Anomaly Detection

|  Name  |                                                Title                                               |   Venue   |                           Paper                           |                          Code                          |
|:------:|:--------------------------------------------------------------------------------------------------:|:---------:|:---------------------------------------------------------:|:------------------------------------------------------:|
|  AAGOD | A data-centric framework to endow graph neural networks with out-of-distribution detection ability |  KDD 2023 | [PDF](https://dl.acm.org/doi/pdf/10.1145/3580305.3599244) |      [Torch](https://github.com/BUPT-GAMMA/AAGOD)      |
| GOODAT | GOODAT: Towards Test-time Graph Out-of-Distribution Detection                                      | AAAI 2024 |          [PDF](https://arxiv.org/pdf/2401.06176)          |         [Torch](https://github.com/Ee1s/GOODAT)        |
|  GOAT  | Map to Optimal: Adapting Graph Out-of-Distribution in Test Time                                    |     -     |      [PDF](https://openreview.net/pdf?id=6j0oKBo196)      |                          [N/A]                         |
|  GADT3 | Cross-Domain Graph Anomaly Detection via Test-Time                                                 | TMLR 2025 |          [PDF](https://arxiv.org/pdf/2502.14293)          | [Torch](https://github.com/delaramphf/GADT3-Algorithm) |


#### 4.3 Test-Time Graph Learning for Social Benefits

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
    <td rowspan="2">Recommendation <br>System</td>
    <td>TTA-GREC</td>
    <td>Test-time adaptation on recommender system with data-centric graph transformation</td>
    <td>AAAI 2025</td>
    <td><a href="https://www.ijcai.org/proceedings/2025/0510.pdf">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>DT3OR</td>
    <td>Dual Test-Time Training for Out-of-Distribution Recommender System</td>
    <td>TKDE 2025</td>
    <td><a href="https://dl.acm.org/doi/10.1109/TKDE.2025.3548160">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>Cybersecurity</td>
    <td>Tran et al.</td>
    <td>Mitigating Distribution Shift in Graph-Based Android Malware Classification via Function Metadata and LLM Embeddings</td>
    <td>arXiv 2025</td>
    <td><a href="https://arxiv.org/pdf/2508.06734">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td rowspan="3"><br><br>Healthcare</td>
    <td>GTTA</td>
    <td>Graph-guided test-time adaptation for glaucoma diagnosis using fundus photography</td>
    <td>arXiv 2024</td>
    <td><a href="https://arxiv.org/abs/2407.04396v1">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
  <tr>
    <td>TTDG-MGM</td>
    <td>Test-Time Domain Generalization via Universe Learning: A Multi-Graph Matching Approach for Medical Image Segmentation</td>
    <td>CVPR 2025</td>
    <td><a href="https://openaccess.thecvf.com/content/CVPR2025/papers/Lv_Test-Time_Domain_Generalization_via_Universe_Learning_A_Multi-Graph_Matching_Approach_CVPR_2025_paper.pdf">[PDF]</a></td>
    <td><a href="https://github.com/Yore0/TTDG-MGM">[Code]</a></td>
  </tr>
  <tr>
    <td>SPA</td>
    <td>Recognizing Surgical Phases Anywhere: Few-Shot Test-time Adaptation and Task-graph Guided Refinement</td>
    <td>MICCAI 2025</td>
    <td><a href="https://papers.miccai.org/miccai-2025/paper/1469_paper.pdf">[PDF]</a></td>
    <td>[N/A]</td>
  </tr>
</tbody>
</table>


## 📌 Datasets

<table style="width:100%; border-collapse: collapse; text-align: center; font-size: 0.9em;">
<caption style="caption-side: top; font-weight: bold; margin-bottom: 10px; font-size: 1.1em;">
  Statistics and characteristics of graph datasets for evaluating test-time adaptation on graphs.
</caption>
<thead>
<tr style="border-bottom: 2px solid #000;">
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">Distribution Shift</th>
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">Datasets</th>
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">#Nodes / #Graphs</th>
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">#Edges / Avg. Size</th>
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">#Classes</th>
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">Task Level</th>
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">Metric(s)</th>
  <th rowspan="2" style="border-bottom: 1px solid #ddd; padding: 8px;">Splits</th>
</tr>
</thead>
<tbody>
<tr style="border-top: 2px solid #666;">
  <td rowspan="5" style="vertical-align: middle; font-weight: bold; padding: 8px;">Feature/Structural Shift</td>
  <td style="padding: 6px;">Cora</td>
  <td style="padding: 6px;">2,703</td>
  <td style="padding: 6px;">5,278</td>
  <td style="padding: 6px;">10</td>
  <td style="padding: 6px;">Node</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">1/1/8</td>
</tr>
<tr>
  <td style="padding: 6px;">Amazon-Photo</td>
  <td style="padding: 6px;">7,650</td>
  <td style="padding: 6px;">119,081</td>
  <td style="padding: 6px;">10</td>
  <td style="padding: 6px;">Node</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">1/1/8</td>
</tr>
<tr>
  <td style="padding: 6px;">IMDB-BINARY</td>
  <td style="padding: 6px;">1,000</td>
  <td style="padding: 6px;">19</td>
  <td style="padding: 6px;">2</td>
  <td style="padding: 6px;">Graph</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">1/1/8</td>
</tr>
<tr>
  <td style="padding: 6px;">PROTEINS</td>
  <td style="padding: 6px;">1,113</td>
  <td style="padding: 6px;">39</td>
  <td style="padding: 6px;">2</td>
  <td style="padding: 6px;">Graph</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">8/1/1</td>
</tr>
<tr style="border-bottom: 1px solid #ddd;">
  <td style="padding: 6px;">ENZYMES</td>
  <td style="padding: 6px;">587</td>
  <td style="padding: 6px;">33</td>
  <td style="padding: 6px;">6</td>
  <td style="padding: 6px;">Graph</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">4/1</td>
</tr>

<tr style="border-top: 2px solid #666;">
  <td rowspan="6" style="vertical-align: middle; font-weight: bold; padding: 8px;">Domain Shift</td>
  <td style="padding: 6px;">Twitch-E</td>
  <td style="padding: 6px;">1,912-9,498</td>
  <td style="padding: 6px;">31,299–153,138</td>
  <td style="padding: 6px;">2</td>
  <td style="padding: 6px;">Node/Graph</td>
  <td style="padding: 6px;">ROC-AUC</td>
  <td style="padding: 6px;">1/1/5</td>
</tr>
<tr>
  <td style="padding: 6px;">FB-100</td>
  <td style="padding: 6px;">769-41,536</td>
  <td style="padding: 6px;">16,656–1,590,655</td>
  <td style="padding: 6px;">2</td>
  <td style="padding: 6px;">Node</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">3/2/3</td>
</tr>
<tr>
  <td style="padding: 6px;">ACMv9</td>
  <td style="padding: 6px;">7,410</td>
  <td style="padding: 6px;">22,270</td>
  <td style="padding: 6px;">6</td>
  <td style="padding: 6px;">Node/Graph</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">1/1/369 (3-domains: A, D, C)</td>
</tr>
<tr>
  <td style="padding: 6px;">DBLPv8</td>
  <td style="padding: 6px;">5,578</td>
  <td style="padding: 6px;">14,682</td>
  <td style="padding: 6px;">6</td>
  <td style="padding: 6px;">Node/Graph</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">1/1/369 (3-domains: A, D, C)</td>
</tr>
<tr>
  <td style="padding: 6px;">Citationv2</td>
  <td style="padding: 6px;">4,715</td>
  <td style="padding: 6px;">13,466</td>
  <td style="padding: 6px;">6</td>
  <td style="padding: 6px;">Node/Graph</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">1/1/369 (3-domains: A, D, C)</td>
</tr>
<tr style="border-bottom: 1px solid #ddd;">
  <td style="padding: 6px;">ogbg-molhiv</td>
  <td style="padding: 6px;">41,127</td>
  <td style="padding: 6px;">25.3</td>
  <td style="padding: 6px;">2</td>
  <td style="padding: 6px;">Graph</td>
  <td style="padding: 6px;">ROC-AUC</td>
  <td style="padding: 6px;">8/1/1</td>
</tr>

<tr style="border-top: 2px solid #666;">
  <td rowspan="2" style="vertical-align: middle; font-weight: bold; padding: 8px;">Temporal Shift</td>
  <td style="padding: 6px;">OGB-arXiv</td>
  <td style="padding: 6px;">169,343</td>
  <td style="padding: 6px;">1,166,243</td>
  <td style="padding: 6px;">40</td>
  <td style="padding: 6px;">Node/Graph</td>
  <td style="padding: 6px;">Accuracy</td>
  <td style="padding: 6px;">1/1/3</td>
</tr>
<tr style="border-bottom: 2px solid #000;">
  <td style="padding: 6px;">Elliptic</td>
  <td style="padding: 6px;">203,769</td>
  <td style="padding: 6px;">234,355</td>
  <td style="padding: 6px;">2</td>
  <td style="padding: 6px;">Node</td>
  <td style="padding: 6px;">F1 Score</td>
  <td style="padding: 6px;">5/5/33</td>
</tr>
</tbody>
</table>
