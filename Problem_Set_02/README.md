# Bank Term Deposit Prediction using Logistic Regression

## Overview
This project aims to predict whether a customer will subscribe to a term deposit based on their banking behavior using Logistic Regression.

The model is built using the Bank Marketing Dataset, which contains customer demographic and financial information.

---

## Dataset
The dataset includes 17 attributes such as:
- Age
- Job
- Marital status
- Education
- Balance
- Loan information
- Contact communication type
- Campaign details

Target Variable:
- y → Whether the customer subscribed to a term deposit (Yes/No)

---

## Methodology

### Data Preprocessing
- Handled categorical variables using encoding
- Feature scaling applied where necessary
- Train-test split performed

---

### Model Used
- Logistic Regression

### Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

---

## Results

### Model Performance Summary

- Accuracy    : 89.14%  
- Precision   : 59.45%  
- Recall      : 22.59%  
- F1-Score    : 32.74%  
- Specificity : 97.96%  
- ROC-AUC     : 87.26%  

---

### Confusion Matrix

- True Negatives  (TN): 7822  
- False Positives (FP): 163  
- False Negatives (FN): 819  
- True Positives  (TP): 239  

---

### Classification Report

| Class | Precision | Recall | F1-score | Support |
|------|----------|--------|----------|--------|
| No (0)  | 0.91 | 0.98 | 0.94 | 7985 |
| Yes (1) | 0.59 | 0.23 | 0.33 | 1058 |

---

## Analysis

- The model achieves high overall accuracy (89.14%), mainly due to correctly predicting the majority class ("No").
- Recall for the "Yes" class is low (22.59%), indicating that many actual subscribers are not correctly identified.
- High specificity (97.96%) shows the model is very good at identifying non-subscribers.
- This imbalance suggests the dataset is skewed toward the "No" class.

---

## Conclusion

The Logistic Regression model performs well in identifying non-subscribers but struggles to correctly identify customers who will subscribe.

---

## Future Improvements

- Handle class imbalance using:
  - SMOTE (oversampling)
  - Class weighting
- Try advanced models:
  - Random Forest
  - Gradient Boosting
- Feature engineering for better prediction
