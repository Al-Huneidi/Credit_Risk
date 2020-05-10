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
	- Precision: high_risk = 1%, low_risk = 100%
	- Recall: high_risk = 74%, low_risk = 56%
	- Imbalanced Classification Report:
	
![alt text](https://github.com/Al-Huneidi/Credit_Risk/blob/master/ScreenShots/credit-risk-resampling/RandomOverSampler_Class_Report.png)

Oversampled the data using the SMOTE algorithms.

	- Balanced Accuracy Score: 65.48%
	- Precision: high_risk = 1%, low_risk = 100%
	- Recall: high_risk = 62%, low_risk = 69%                                                                                                                                                  
	- Imbalanced Classification Report:

![alt text](https://github.com/Al-Huneidi/Credit_Risk/blob/master/ScreenShots/credit-risk-resampling/SMOTE_Oversampling_Class_Report.png)

Undersampled the data using the ClusterCentroids algorithm.

	- Balanced Accuracy Score: 53.3%
	- Precision: high_risk = 1%, low_risk = 100%
	- Recall: high_risk = 66%, low_risk = 40%
	- Imbalanced Classification Report: 
	
![alt text](https://github.com/Al-Huneidi/Credit_Risk/blob/master/ScreenShots/credit-risk-resampling/ClusterCentroids_Class_Report.png)

Used a combination approach with the SMOTEENN algorithm.

	- Balanced Accuracy Score: 64.83%
	- Precision: high_risk = 1%, low_risk = 100%
	- Recall: high_risk = 72%, low_risk = 57%
	- Imbalanced Classification Report: 
	
![alt text](https://github.com/Al-Huneidi/Credit_Risk/blob/master/ScreenShots/credit-risk-resampling/SMOTEEN_Class_report.png)

## Analysis Report

The Balanced Accuracy Score is telling us the percentage of predictions that are correct and the best model is SMOTE with the highest percentage of 65.48%.  For the sake of not losing money, I think the percentage of predictions that are correct needs to be higher.

Precision tells us how reliable a positive classification is and all the models give us a precision of 100% for the low-risk applicants and 1% for the high-risk applicants so none of the models are good at predicting the high-risk applicants and that is not good for business because if you give credit to people with a high risk of not paying their bill the company will lose money.

Recall (Sensitivity) indicates the ability of the classifier to find all positive samples. Looking at the recall numbers, all the models did better at finding the high-risk applications with the RandomOverSampler model generating the best results at 74% for high-risk and 56% for low-risk ( not a high percentage but over 50%). 

Overall, Recall seems to be the most important because it is better even if it means a certain number of false positives, than to miss those with a high-risk. Essentially, highly sensitive test and algorithms tend to be aggressive as they do a good job of detecting the intended target, even if that means they result in a number of false positives.  In this case, I think it is better to have false positives than not because you really want to target the high-risk applications.  The false positives in a highly sensitive test are accepted as a cost of doing business.


# Challenge Extension
For the extension, trained and compared two different ensemble classifiers to predict loan risk and evaluate each model to combine resampling and model training into a single step. 

Used BalancedRandomForestClassifer and EasyEnsembleClassifier models, using 100 estimators for both classifiers to train the models and generate predictions.

1. Balanced Accuracy Scores:

	- BalancedRandowmForestClassifier - 78.55%
	- Easy EnsembleClassifier - 93.16%

2. Generated a confusion matrix for each method.

3. Printed the classification reports

BalancedRandomForestClassifier
	- Precision Score: high-risk 4%, low-risk 100%
	- Recall Score: high-risk 67%, low-risk 90%

![alt text](https://github.com/Al-Huneidi/Credit_Risk/blob/master/ScreenShots/credit-risk-ensemble/BalancedRandomForest_class_report.png)
		
EasyEnsembleClassifier
	- Precision Score: high-risk 9%, low-risk 100%
	- Recall Score: high-risk 92%, low-risk 94%

![alt text](https://github.com/Al-Huneidi/Credit_Risk/blob/master/ScreenShots/credit-risk-ensemble/EasyEnsemble_class_report.png)

4. For the BalancedRandomForestClassifier, printed the feature importance, sort in descending order (from most to least important feature), along with the feature score.
