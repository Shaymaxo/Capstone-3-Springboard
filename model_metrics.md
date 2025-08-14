# 🎯 Model Performance Metrics — Customer Churn Analysis

**File:** `model_metrics.md`  
**Author:** Shayma Remy  
**Date:** 2025-08-14


**Test set size:** 1,409

## Logistic Regression (Primary)
- AUC: **0.836**
- Accuracy: **73.8%**
- Precision (churn): **80.5%**
- Recall (churn): **50.4%**
- F1-score: **0.621**
- Confusion matrix (ACTUAL rows / PREDICTED cols):
  - No Churn: [TN=739, FP=73] (total 812)
  - Churn:    [FN=296, TP=301] (total 597)
- Notes: Use as primary production model. See `notebooks/` for hyperparameters and exact feature list.

## Decision Tree (Secondary)
- AUC: **0.765**
- Accuracy: **65.3%**
- Precision (churn): **42.6%**
- Recall (churn): **87.9%**
- F1-score: **0.574**
- Confusion matrix (ACTUAL rows / PREDICTED cols):
  - No Churn: [TN=591, FP=444] (total 1035)
  - Churn:    [FN=45, TP=329] (total 374)
- Notes: High-recall model — useful when missing churners is very costly.

