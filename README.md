# Phase-DATASET-and-DATA-cleaning
Phase 1-This phase consists of the raw datasets which has all the raw entries and the data dimensions are as follows:-
rows-12(approx)
columns-12300(approx)
 # Dataset Overview

This repository contains a dataset structured with **12 rows** and **12,300 columns**.  
It is designed for high-dimensional analysis, where each row represents an observation and each column corresponds to a distinct feature.

--- Structure
- **Rows (Observations):** 12  
- **Columns (Features):** 12,300  
- **Format:** Tabular (CSV/Excel recommended)  
- **Size:** Wide dataset (many features, few samples)

---
 Usage
Due to its high dimensionality:
- Apply **dimensionality reduction**  before visualization.  
- Consider **feature selection** or **regularization techniques** for modeling.  
- Suitable for experiments in **machine learning**, **bioinformatics**, or **text embeddings**.

Phase 2- This phase consists of the dataset pre training and data cleaning codes which consists of the model accuracy consists of the following algorithms of supervised learning:-
1)KNN
2)Logistic Regression

# High-Dimensional Dataset Project

## 📊 Dataset Overview
- **Rows (Observations):** 12  
- **Columns (Features):** 12,300  
- **Format:** Tabular (CSV recommended)  
- **Target:** Classification task  

This dataset is intentionally **wide** (many features, few samples), making it suitable for testing algorithms in **high-dimensional learning** scenarios.

 Preprocessing
Steps applied before training:
1. **Missing Values:** Filled with column mean/median.  
2. **Scaling:** Standardized features using `StandardScaler`.  
3. **Dimensionality Reduction:** Applied PCA to reduce features to ~200 components.  
4. **Train/Test Split:** 70% training, 30% testing.  

Algorithms
Two models were trained and evaluated:

- **Logistic Regression**
  - Regularized with `max_iter=1000`.
  - Performs well in high-dimensional spaces.

- **K-Nearest Neighbors (KNN)**
  - Used `k=3`.
  - Sensitive to scaling and dimensionality.

Evaluation
Accuracy was measured using both **train/test split** and **cross-validation**.

```python
from sklearn.metrics import accuracy_score
print("Logistic Regression Accuracy:", acc_lr)
print("KNN Accuracy:", acc_knn)
