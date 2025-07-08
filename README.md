# Prediction-using-Machine-Learning
Blood Clot Prediction using Machine Learning
Author: Kabi Veronicah
Date: July 8, 2025

Objective
To build a machine learning model that predicts the presence of a blood clot in patients based on medical features such as D-dimer levels, platelet count, blood pressure, and lifestyle indicators like smoking and diabetes.

Dataset
Source: Simulated dataset with 500 patient records

Features:

Age, D-dimer, Platelet Count, Blood Pressure, Cholesterol

Smoking (binary), Diabetes (binary)

Target: Clot_Present (1 = clot present, 0 = no clot)

Class balance:

Clot cases: 50 (10%)

Non-clot cases: 450 (90%)

Models Applied
Logistic Regression:Logistic Regression was initially used to model the clot prediction task. While it performed well in terms of overall accuracy, it struggled with recall on the minority class (clot present). As a result, more robust classifiers like Random Forest and XGBoost were implemented. These models significantly improved clot detection performance, especially after threshold tuning and class balancing.

Random Forest Classifier (with and without SMOTE)

XGBoost Classifier (Final model)

✅ Best Model: XGBoost with Threshold Tuning (0.4)
Confusion Matrix:
[[130   2]
 [  7  11]]
Metric	Class 0 (No Clot)	Class 1 (Clot)
Precision	95%	85%
Recall	98%	61%
F1-Score	97%	71%

Accuracy: 94%

ROC AUC: ~0.84

Key Findings
XGBoost with original training data (no SMOTE) and threshold adjustment to 0.4 produced the most balanced results.

The model achieves high precision and acceptable recall, meaning:

It detects most clots without generating too many false alarms.

Using SMOTE improved recall but led to higher false positives.

Threshold tuning was crucial to optimize the trade-off between recall and precision, which is critical in medical predictions.

Conclusion
The final XGBoost model performs reliably, with 94% accuracy and a 61% recall rate for detecting clots. This balance between sensitivity and specificity makes it suitable for early screening in medical contexts, where missing true clots is riskier than false alarms.
