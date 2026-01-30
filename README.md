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

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-0pky">Taxonomy</th>
    <th class="tg-c3ow">Name</th>
    <th class="tg-c3ow">Title</th>
    <th class="tg-c3ow">Venue</th>
    <th class="tg-c3ow">Paper</th>
    <th class="tg-0lax">Code</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-c3ow" rowspan="5"><br><br><br>Latent Feature <br>Space-Oriented <br>Fine-Tuning</td>
    <td class="tg-0pky">GT3</td>
    <td class="tg-0pky">Test-Time Training for Graph Neural Networks</td>
    <td class="tg-0pky">arXiv</td>
    <td class="tg-0pky">[PDF](https://arxiv.org/abs/2210.08813)</td>
    <td class="tg-0lax">[N/A]</td>
  </tr>
  <tr>
    <td class="tg-0pky">HomoTTT</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-0pky">TARD</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-0pky">IGT</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-0pky">MATCHA</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">Graph Learning <br>Task-Oriented</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-c3ow" rowspan="3"><br><br>Fully <br>Fine-Tuning</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-0lax"></td>
  </tr>
  <tr>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-0lax"></td>
  </tr>
</tbody></table>


#### 1.2 Adapter-Based Model Learning 




#### 1.3 Joint Model-Adapter Learning




### 2. Data-Centric TTA Methods on Graphs

#### 2.1 Additive Graph Refinement




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
