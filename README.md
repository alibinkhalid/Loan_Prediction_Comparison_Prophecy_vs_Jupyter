# Model Comparison: Jupyter (Python) vs Prophecy

## Overview

This repository has been created to **compare machine learning model results developed in two different environments**:

- **Jupyter Notebook (Python / scikit‑learn)**
- **Prophecy (Enterprise data & ML platform)**

The objective is to analyse and understand **performance differences, consistency, and ranking of models** when implemented across platforms using the same underlying dataset and problem statement.

---

## Problem Statement

The project focuses on a **binary classification problem** (e.g. loan approval prediction), where multiple supervised learning algorithms are trained and evaluated.

Key evaluation criteria:

- Accuracy  
- Confusion Matrix metrics (TN, FP, FN, TP)  
- Model ranking across platforms  

---

## Jupyter Notebook Models (Python)

The following models were developed and evaluated using **Python (scikit‑learn)** in a Jupyter Notebook environment.

### Jupyter Model Accuracy Results

| Rank | Model                   | Accuracy (%) |
|------|-------------------------|--------------|
| 1    | Random Forest           | 80.8 |
| 2    | Logistic Regression     | 79.2 |
| 3    | K Nearest Neighbours    | 78.4 |
| 4    | Gradient Boost          | 76.8 |
| 5    | SVM                     | 74.4 |
| 6    | Decision Tree           | 73.6 |
| 7    | Gaussian Naive Bayes    | 66.4 |
| 8    | Categorical Naive Bayes | 57.6 |

### Notes

- Models were trained using standard train/test splits
- Feature preprocessing, imputation, and scaling were handled in Python
- Model evaluation used accuracy, confusion matrix, and classification reports

---

## Prophecy Platform Models

The same modelling logic was implemented in **Prophecy**, and results were captured using confusion‑matrix driven evaluation.

### Prophecy Model Results

| Rank | Model Name           | TN | FP | FN | TP | Accuracy (%) |
|------|----------------------|----|----|----|----|--------------|
| 1    | Random Forest        | 67 | 6  | 7  | 65 | 91.03 |
| 2    | Decision Tree        | 68 | 5  | 10 | 62 | 89.66 |
| 3    | Gradient Boost       | 63 | 10 | 7  | 65 | 88.28 |
| 4    | SVM                  | 49 | 24 | 16 | 56 | 72.41 |
| 5    | KNN                  | 55 | 18 | 25 | 47 | 70.34 |
| 6    | Naive Bayes          | 32 | 41 | 7  | 65 | 66.90 |
| 7    | Logistic Regression  | 38 | 35 | 18 | 54 | 63.45 |

### Notes

- Prophecy models were evaluated using confusion matrix metrics
- Accuracy was derived from (TP + TN) / Total
- Model ranking differs from Jupyter due to platform‑specific optimisations and execution behaviour

---

## Key Observations

- **Random Forest performs best on both platforms**, but with significantly higher accuracy in Prophecy
- **Model rankings differ** between Jupyter and Prophecy (e.g. Logistic Regression and Decision Tree)
- Platform‑level differences such as:
  - Feature handling  
  - Execution engine  
  - Optimisation strategies  

can impact model performance.

---

## Purpose of This Repository

This repository exists to:

- Provide a **transparent comparison** between notebook‑based ML and enterprise ML platforms
- Help understand **performance drift across implementations**
- Support learning, validation, and stakeholder discussions around model portability

---

## Technologies Used

- Python (Jupyter Notebook)
- scikit‑learn
- Pandas, NumPy, Matplotlib, Seaborn
- Prophecy Platform

---

## Disclaimer

Results may vary depending on:

- Data preprocessing steps
- Random seeds
- Platform execution semantics

This comparison is intended **for analysis and learning purposes only**.

---

## Author

This repository is maintained as part of a comparative analytics and modelling exercise.
