<div align="center">
  <h1>🧠 Spatio-Temporal Graph Neural Network for Motor Movement Classification Using 64-Channel EEG Signals</h1>
  <p><strong>PhysioNet EEG Motor Movement/Imagery Database (EEGMMIDB)</strong></p>

  ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
  ![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)
  ![Machine Learning](https://img.shields.io/badge/Machine_Learning-FF6F00?style=for-the-badge&logo=scikit-learn&logoColor=white)
</div>

<br />

## 👥 Project Team
| Role | Name | ID |
| :--- | :--- | :--- |
| **Author** | Asfar Hossain SItab | `2026-2-74-008` |
| **Author** | Parmita Hossain Simia | `2026-2-74-009` |
| **Supervisor** | Raihan Ul Islam | *Associate Professor, Dept. of CSE, East West University (EWU)* |

---

## 📌 Track Information
- **Group:** 01
- **Dataset:** PhysioNet EEG MMI
- **Track:** Machine Learning

---

## 🚀 TASK-1: Exploratory Data Analysis (EDA)

### 📊 EDA Summary
The initial phase focuses on deeply exploring the **PhysioNet EEG Motor Movement/Imagery Database (EEGMMIDB)**. 
- **Scale:** 109 subjects with 64 EEG channels sampled at 160 Hz.
- **Scope:** Analyzes motor execution runs (left/right fist) alongside motor imagery runs to identify signal patterns.
- **Techniques:** Signal filtering, epoching, and robust visualizations to lay the groundwork for our downstream machine learning classification tasks.

### 🖼️ Visual Insights (Task 1)
Here are some of the key visual findings extracted from our EDA notebook. These visualizations help us understand the spatial and temporal distributions of the EEG signals.

<details open>
<summary><b>View Visualizations</b></summary>
<br>

| **Topographic Brain Mapping** | **Channel Activity Analysis** |
| :---: | :---: |
| <img src="images/Task1/topomap.png" alt="Topographic Map" width="400"/> | <img src="images/Task1/eda_2.png" alt="EDA Visualization 2" width="400"/> |

| **Signal Distributions** | **Temporal Features** |
| :---: | :---: |
| <img src="images/Task1/eda_3.png" alt="EDA Visualization 3" width="400"/> | <img src="images/Task1/eda_4.png" alt="EDA Visualization 4" width="400"/> |

| **Frequency Domains** | **Spectral Density** |
| :---: | :---: |
| <img src="images/Task1/eda_5.png" alt="EDA Visualization 5" width="400"/> | <img src="images/Task1/eda_6.png" alt="EDA Visualization 6" width="400"/> |

</details>

---

## 🚀 TASK-2: Motor Movement Classification

### 🧠 Classification Summary
Building upon the insights from our EDA, Task 2 focuses on constructing robust machine learning models to classify motor movements using the EEG signals. We explore both baseline deep learning approaches (1D CNN) and advanced Spatio-Temporal Graph Neural Networks (ST-GNN) to capture the complex spatial correlations and temporal dynamics inherent in EEG data.

### 🖼️ Model & Performance Visual Insights (Task 2)
These visualizations illustrate the data processing, model architectures, and training evaluation results for our classification models.

<details open>
<summary><b>View Visualizations</b></summary>
<br>

| **ERD/ERS Topomaps** | **Class Distribution** |
| :---: | :---: |
| <img src="images/Task2/erd_ers_topomaps.png" alt="ERD ERS Topomaps" width="400"/> | <img src="images/Task2/class_distribution.png" alt="Class Distribution" width="400"/> |

| **Brain Graph** | **Normalized Adjacency** |
| :---: | :---: |
| <img src="images/Task2/brain_graph.png" alt="Brain Graph" width="400"/> | <img src="images/Task2/normalized_adjacency.png" alt="Normalized Adjacency" width="400"/> |

| **ST-GNN Architecture Diagram** | **Hybrid ST-GNN Test Confusion Matrix** |
| :---: | :---: |
| <img src="images/Task2/stgnn_architecture_diagram.png" alt="ST-GNN Architecture Diagram" width="400"/> | <img src="images/Task2/hybrid_stgnn_test_confusion_matrix.png" alt="Hybrid ST-GNN Test Confusion Matrix" width="400"/> |

| **1D CNN Learning Curve** | **Hybrid ST-GNN Learning Curve** |
| :---: | :---: |
| <img src="images/Task2/1d_cnn_learning_curve.png" alt="1D CNN Learning Curve" width="400"/> | <img src="images/Task2/hybrid_st_gnn_learning_curve.png" alt="Hybrid ST-GNN Learning Curve" width="400"/> |

</details>

> ⚠️ *Note: **TASK-3** and **TASK-4** methodologies and results will be uploaded in subsequent updates.*

---

## 💻 How to Run
All execution scripts, models, and notebooks are located in the `code/`, `models/`, and `report/` directories. Navigate to specific task folders to reproduce our findings.

```bash
# Example for running EDA (Task 1)
jupyter notebook code/task1/Group01_PhysioNet_EEG_MMI_task1_eda.ipynb
```

---

## 📈 Results
* Our Hybrid ST-GNN effectively classifies motor tasks by capturing both spatial dependencies (via GCNs) and temporal features (via CNNs/LSTMs).
* See the confusion matrix and learning curves in the visualizations section for specific performance metrics.

<div align="center">

### Model Performance Metrics

<table>
  <thead>
    <tr>
      <th align="center">Model</th>
      <th align="center">Test Accuracy</th>
      <th align="center">Precision (Macro)</th>
      <th align="center">Recall (Macro)</th>
      <th align="center">F1-Score (Macro)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>1D-CNN</b></td>
      <td align="center">65.96%</td>
      <td align="center">0.6596</td>
      <td align="center">0.6596</td>
      <td align="center">0.6596</td>
    </tr>
    <tr>
      <td align="center"><b>XGBoost</b></td>
      <td align="center">64.27%</td>
      <td align="center">0.6426</td>
      <td align="center">0.6426</td>
      <td align="center">0.6426</td>
    </tr>
    <tr>
      <td align="center"><b>Random Forest</b></td>
      <td align="center">64.27%</td>
      <td align="center">0.6429</td>
      <td align="center">0.6425</td>
      <td align="center">0.6423</td>
    </tr>
    <tr>
      <td align="center"><b>Motor-area CSP-LDA</b></td>
      <td align="center">64.12%</td>
      <td align="center">0.6412</td>
      <td align="center">0.6412</td>
      <td align="center">0.6412</td>
    </tr>
    <tr>
      <td align="center"><b>Extra Trees</b></td>
      <td align="center">63.84%</td>
      <td align="center">0.6393</td>
      <td align="center">0.6382</td>
      <td align="center">0.6376</td>
    </tr>
    <tr>
      <td align="center"><b>Gradient Boosting</b></td>
      <td align="center">63.56%</td>
      <td align="center">0.6361</td>
      <td align="center">0.6354</td>
      <td align="center">0.6350</td>
    </tr>
    <tr>
      <td align="center"><b>Logistic Regression</b></td>
      <td align="center">61.86%</td>
      <td align="center">0.6186</td>
      <td align="center">0.6186</td>
      <td align="center">0.6186</td>
    </tr>
    <tr>
      <td align="center"><b>MLP</b></td>
      <td align="center">61.72%</td>
      <td align="center">0.6174</td>
      <td align="center">0.6171</td>
      <td align="center">0.6170</td>
    </tr>
    <tr>
      <td align="center"><b>RBF SVM</b></td>
      <td align="center">61.16%</td>
      <td align="center">0.6116</td>
      <td align="center">0.6116</td>
      <td align="center">0.6116</td>
    </tr>
    <tr>
      <td align="center"><b>Decision Tree</b></td>
      <td align="center">57.77%</td>
      <td align="center">0.5780</td>
      <td align="center">0.5774</td>
      <td align="center">0.5768</td>
    </tr>
    <tr>
      <td align="center"><b>k-NN</b></td>
      <td align="center">57.20%</td>
      <td align="center">0.5738</td>
      <td align="center">0.5724</td>
      <td align="center">0.5701</td>
    </tr>
    <tr>
      <td align="center"><b>Hybrid ST-GNN</b></td>
      <td align="center">50.99%</td>
      <td align="center">0.5100</td>
      <td align="center">0.5090</td>
      <td align="center">0.4975</td>
    </tr>
  </tbody>
</table>

</div>
