# Passenger-Transportation-Analysis
This classification problem predicts whether a passenger will be successfully transported during interplanetary travel based on personal and travel attributes.

# 🚀 Passenger Transportation Classification Challenge

## Project Overview
This repository contains my solution to an assessment project aimed at predicting whether a passenger will be successfully transported during interplanetary travel based on personal and travel attributes. The project was completed for the **Galactic Transportation Initiative (GTI)**, focusing on optimizing passenger safety and travel efficiency.

---

## 📄 Problem Statement
The goal is to predict passengers' `Transported` status (TRUE/FALSE) using classification models. The dataset includes various features such as passenger attributes (`Age`, `VIP` status), spending patterns, cabin information, and travel details. The challenge involves:
1. Comparing classification models and selecting the best one based on metrics like AUC-ROC.
2. Adjusting thresholds for specific scenarios where False Negatives (FN) and False Positives (FP) have varying costs.

---

## 📋 Objectives

### Part A: Initial Model Comparison and Hyperparameter Tuning
1. Compare two baseline classification models:
   - Logistic Regression
   - K-Nearest Neighbors (KNN)
2. Optimize the models using `RandomizedSearchCV` with 5-fold cross-validation (`cv=5`), tuning two hyperparameters for each model.
3. Evaluate optimized models using:
   - Accuracy
   - Precision
   - Recall
   - F1-score
   - AUC-ROC
4. Plot ROC-AUC curves for visualization and comparison.
5. Select the best model (`best_model`) based on performance metrics.

### Part B: Error Analysis and Threshold Selection
1. Use the `best_model` from Part A to analyze and adjust thresholds for two scenarios:
   - **Scenario 1**: Balanced approach minimizing both FN and FP.
   - **Scenario 2**: Prioritizing recall to minimize FN, even at the cost of higher FP.
2. Document the thresholds chosen for each scenario and the trade-offs encountered.

---

## 📂 Repository Structure
- `README.md`: Overview and project details (this file).
- `preprocessor.py`: The preprocessing pipeline is provided by GTI for data transformation and feature encoding.
- `notebooks/`: Contains Jupyter notebooks for model training, evaluation, and threshold analysis.
- `data/`: Dataset files used for training and testing.
- `results/`: Performance metrics, ROC-AUC curves, and threshold analysis results.

---

## 🧠 Methodology
1. **Data Preprocessing**:
   - Utilized the `preprocessor` pipeline provided by GTI to transform and encode features.
   - Ensured the dataset was clean and ready for model training and evaluation.

2. **Model Selection and Tuning**:
   - Compared Logistic Regression and KNN models.
   - Tuned hyperparameters using `RandomizedSearchCV` and cross-validation.

3. **Threshold Optimization**:
   - Adjusted thresholds based on GTI's specific error-cost scenarios:
     - Scenario 1: Balanced approach.
     - Scenario 2: Prioritizing recall to minimize FN.

---

## 📝 Deliverables
1. **Optimized Models**:
   - Logistic Regression and KNN models with hyperparameter tuning.
2. **Final Model**:
   - `best_model` selected based on AUC-ROC and other performance metrics.
3. **Threshold Analysis**:
   - Threshold adjustments documented for both scenarios.
4. **Documentation**:
   - Markdown summaries explaining model selection, tuning, and error analysis.

---

## 🎯 Key Takeaways
This repository demonstrates the ability to:
- Compare and optimize classification models for a real-world problem.
- Use AUC-ROC and other metrics for model evaluation.
- Adjust decision thresholds for scenarios with varying costs of FN and FP.
- Communicate results and findings effectively.

---
