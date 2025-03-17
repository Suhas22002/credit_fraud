# Fraud Detection & Prevention Model

## Overview
PredCatch Analytics has been tasked with building a fraud detection model for an Australian banking client. The client's profitability and reputation are being impacted by fraudulent ATM transactions. This project aims to build a predictive model to detect and prevent fraudulent transactions in real time.

## Problem Statement
The dataset contains a large number of clean transactions (label `0`) and very few fraudulent transactions (label `1`), making it an **imbalanced classification problem**. The objective is to:

- Identify fraudulent transactions with high accuracy.
- Minimize false negatives (missed frauds) and false positives (declining legitimate transactions).
- Provide an explainable and scalable solution for real-time fraud prevention.

## Data Description
The dataset includes masked variables related to each transaction, as well as additional proprietary features:

- **geo_scores**: Location-based risk score.
- **Lambda_wts**: Proprietary index score.
- **Qset_tats**: Network turnaround times.
- **instance_scores**: Vulnerability qualification score.
- **Target**: The prediction target (1 = Fraud, 0 = Clean).

## Approach
1. **Exploratory Data Analysis (EDA)**
   - Analyze missing values, distributions, and correlations.
   - Identify patterns in fraudulent transactions.
   
2. **Data Preprocessing & Feature Engineering**
   - Handle missing values and scale numerical features.
   - Apply transformations to improve model performance.
   - Address class imbalance using **oversampling (SMOTE)** and **undersampling techniques**.
   
3. **Model Development**
   - Train baseline models (Logistic Regression, Decision Trees).
   - Implement advanced models: **Random Forest, XGBoost, LightGBM, and Neural Networks**.
   - Evaluate models based on **Precision, Recall, F1-score, and AUPRC (Area Under Precision-Recall Curve)**.

4. **Real-Time Fraud Prevention Strategy**
   - Deploy the model as an API for real-time transaction scoring.
   - Implement threshold-based flagging for manual review.

5. **Model Explainability & Business Impact**
   - Use **SHAP values and LIME** for interpretability.
   - Perform a **cost-benefit analysis** to measure fraud prevention gains.

## Results & Findings
- The **best-performing model** achieved an **F1-score of X** and an **AUPRC of Y**.
- Feature importance analysis revealed that **geo_scores** and **Qset_tats** significantly impact fraud detection.
- The model can be deployed in real time, reducing fraudulent losses by an estimated **Z%**.

## Next Steps
- Fine-tune the model further with additional data.
- Deploy the solution as a **real-time API**.
- Implement feedback loops to improve accuracy over time.
