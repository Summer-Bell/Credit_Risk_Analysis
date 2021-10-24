# Credit Risk Analysis

## Overview of the Credit Risk Analysis
Loan prediction risk analysis is an inherently unbalanced classification problem because good loans outnumber bad loans.
There are different techniques that can be used to train and evaluate unbalanced models.

### Purpose
Imbalanced-learn and scikit-learn libraries will be used to build and evaluate models using resampling.
In the file [credit_risk_resampling.ipynb](credit_risk_resampling.ipynb) the data will be oversampled, undersampled and a combination approach of over-and-undersampling will be demonstrated.
To oversample the data the RandomOverSampler and SMOTE algorithms will be used.
Then to undersample the data the ClusterCentroids algorithms will be used.
SMOTEENN will be used for the combinatorial approach.
In the file [credit_risk_ensemble.ipynb](credit_risk_ensemble.ipynb) machine learning models BalancedRandomForestClassifier and EasyEnsembleClassifier will be used to reduce bias.


## Results
-  Random Oversampling:
	- Balanced Accuracy - .661
	- Precision: High Risk (HR) - .01, Low Risk (LR) - 1.00
	- Recall: HR - .66, LR - .67

-  SMOTE Oversampling:
	- Balanced Accuracy - .63
	- Precision: HR - .01, LR - 1.00
	- Recall: HR - .62, LR - .64

-  Undersampling:
	- Balanced Accuracy - .529
	- Precision: HR - .01, LR - 1.00
	- Recall: HR - .61, LR - .45

-  SMOTEEN:
	- Balanced Accuracy - .638
	- Precision: HR - .01, LR - 1.00
	- Recall: HR - .70, LR - .57

-  Balanced Random Forest Classifier:
	- Balanced Accuracy - .783
	- Precision: HR - .04, LR - 1.00
	- Recall: HR - .67, LR - .89

-  Easy Ensemble AdaBoost Classifier:
	- Balanced Accuracy - .918
	- Precision: HR - .09, LR - 1.00
	- Recall: HR - .89, LR - .94

## Credit Risk Analysis Summary
There are tradeoffs between using the different resampling models.
For credit analysis it is critical to be able to identify the small number of bad loans.
You do not want a model that has a high percentage of false positives.
Based on the data the Easy Ensemble AdaBoost Classifier model is the best for preventing fraudulent loans.
It has a high accuracy score and it has relatively good precision and recall scores.
