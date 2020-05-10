# Credit_Risk Module Work
Used Python to build and evaluate several machine learning models to predict credit risk. The ablity to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud.

# Challenge Overview

Use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Evaluated the performance of these models and provide a recommendation on whether they should be used to predict credit risk.

## Objectives

	•	Implement machine learning models.
	•	Use resampling to attempt to address class imbalance.
	•	Evaluate the performance of machine learning models.

## Process - For each of the models RandomOverSampler, SMOTE, Cluster Centroids, and SMOTEENN:

	1. Trained a logistic regression classifier (from Scikit-learn) using the resampled data.
	2. Calculated the balanced accuracy score using balanced_accuracy_score.
	3. Generated a Confusion Matrix.
	4. Printed the Classification Reports.

Oversampled the data using the RandomOverSampler.
	- Balanced Accuracy Score: 65.12%
	- Precision: high_risk = 0.01, low_risk = 1.00
	- Recall: high_risk = 0.74, low_risk = 0.56
	- Imbalanced Classification Report:
	
	![alt text](https://github.com/Al-Huneidi/Credit_Risk/blob/master/ScreenShots/credit-risk-resampling/RandomOverSampler_Class_Report.png)
