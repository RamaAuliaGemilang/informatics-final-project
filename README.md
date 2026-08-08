# 🎵 Combining Graph Neural Network with Attention Mechanism in Sequence-Based Music Recommendation System

This repository is part of an **Undergraduate Thesis** entitled:

**Combining Graph Neural Network with Attention Mechanism in Sequence-Based Music Recommendation System**

## 📖 Research Overview

This research focuses on developing a **sequence-based music recommendation system** by combining **Graph Neural Networks (GNN)** and **Attention Mechanism**.

* **GNN** captures relationships between users, music, albums, and artists.
* **Attention Mechanism** captures short-term user preferences within a session.
* **Long-term** and **dynamic preferences** are incorporated to provide a more comprehensive representation of user behavior.
* The model is adapted from the **Graph-based Attentive Sequential Model with Metadata (GASM)** and applied to the larger-scale **Music4All** dataset.

## 📂 Dataset

The research uses the **Music4All** dataset, consisting of music metadata and user listening history.

The dataset used in this study contains **7,998 users**, providing a larger and more diverse user distribution compared to previous GASM experiments.

## 🎯 Research Contributions

1. Adapted the GASM approach to the larger-scale Music4All dataset.
2. Combined **GNN and Attention Mechanism** to model sequential music preferences.
3. Incorporated **short-term, long-term, and dynamic preferences**.
4. Evaluated the model through hyperparameter tuning, preference scenario analysis, and comparison with a baseline model.

## 🛠️ Methodology

1. **Data Preprocessing**

   * Process music metadata and listening history.
   * Select and compact the dataset.
   * Construct user listening sequences.

2. **Graph Construction**

   * Build a heterogeneous graph consisting of users, music, albums, and artists.

3. **Preference Modeling**

   * GNN for graph-based representations.
   * Attention Mechanism for short-term preferences.
   * Long-term and dynamic preference representations.
   * Combine all preferences into a hybrid user representation.

4. **Recommendation**

   * Predict the next music track based on the hybrid user preference.
   * Evaluate both **Next-One** and **Next-New** recommendations.

## 📈 Results

### Best Hyperparameters

The best configuration obtained from 8 random search trials:

```text
Learning Rate = 0.001
L2 Regularization = 0.00001
Hidden Size = 100
```

This configuration achieved **HR@10 = 22.92** and **HR@20 = 26.25** during hyperparameter tuning.

### Best Model Performance

Using the full preference model:

| Recommendation |     HR@10 |     HR@20 |    MRR@10 |    MRR@20 |
| -------------- | --------: | --------: | --------: | --------: |
| **Next-One**   | **44.25** | **49.16** | **30.36** | **30.71** |
| **Next-New**   | **32.69** | **37.06** | **23.34** | **23.64** |

The model achieved its best performance when combining **short-term, long-term, and dynamic preferences**.

### 🆚 Baseline Comparison

Compared with **SRGNN**, the proposed model improved performance across all evaluation metrics:

| Recommendation | Metric | SRGNN | Proposed Model | Improvement |
| -------------- | ------ | ----: | -------------: | ----------: |
| Next-One       | HR@10  | 43.53 |      **44.25** |      +1.65% |
| Next-One       | HR@20  | 48.39 |      **49.16** |      +1.61% |
| Next-One       | MRR@10 | 29.75 |      **30.36** |      +2.05% |
| Next-One       | MRR@20 | 30.10 |      **30.71** |      +2.04% |
| Next-New       | HR@10  | 32.34 |      **32.69** |      +1.10% |
| Next-New       | HR@20  | 36.60 |      **37.06** |      +1.27% |
| Next-New       | MRR@10 | 22.91 |      **23.34** |      +1.89% |
| Next-New       | MRR@20 | 23.20 |      **23.64** |      +1.89% |

## 💡 Key Findings

* The combination of **GNN + Attention Mechanism** effectively captures sequential music preferences.
* **Short-term preference** has a significant impact on recommendation performance; removing it caused a substantial decline across evaluation metrics.
* **Long-term and dynamic preferences** complement short-term preference to create a more comprehensive user representation.
* The proposed heterogeneous graph model outperformed the **SRGNN baseline** across all evaluated metrics.

## 🛠️ Tools & Technologies

* Python
* PyTorch
* Graph Neural Network (GNN)
* Attention Mechanism
* Graph Processing
* Music4All Dataset

## 🎓 Project Information

* **Project:** Undergraduate Thesis
* **Field:** Music Recommendation System
* **Dataset:** Music4All
* **Model:** GNN + Attention Mechanism
* **Base Model:** GASM
* **Baseline:** SRGNN
* **Author:** Rama Aulia Gemilang
* **Institution:** Telkom University
