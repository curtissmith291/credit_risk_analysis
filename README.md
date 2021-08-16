# credit_risk_analysis
Module 17 Challenge


# Overview

Using credit card data from LendingClub, we applied various oversampling, undersampling, and ensemble  algorithms to produce a model that maximizes the number of high-risk loans. 


# Results

## Logistic Regression without Oversampling or Undersampling

Confusion Matix:
[    1,    86]
[    0, 17118]

Accuracy Score:
0.9950014530659692

Of the 87 high-risk loans, the Logistic regression without applying and oversampling or undersampling algorithms, only 1 was correctly classified. 


## Logistic Regression with Random Oversampling

Confusion Matrix:
[   54,    33]
[ 5498, 11620]

Balanced Accuracy Score:
0.6376117496807152

Of the 87 high-risk loans, 54 were correctly classified; however, 5,498 were incorrectly classified as high-risk.


## Logistic Regression with SMOTE Oversampling

Confusion Matrix:
[   55,    32]
[ 5879, 11239]

Balanced Accuracy Score:
0.6443721269403855

Of the 87 high-risk loans, 55 were correctly classified; additionally, 5,879 were incorrectly classified as high-risk.


## Logistic Regression with ClusterCentroids Undersampling

Confusion Matrix:
[  53,   34]
[9428, 7690]

Balanced Accuracy Score:
0.5292150629907619

Of the 87 high-risk loans, 53 were correctly classified; additionally, 9,428 were incorrectly classified as high-risk.


## Logistic Regression with SMOTEENN Combination Sampling

Confusion Matrix:

[  61,   26]
[7291, 9827]

Balanced Accuracy Score:
0.6376117496807152

Of the 87 high-risk loans, 61 were correctly classified; additionally, 7,291 were incorrectly classified as high-risk.

## Logistic Regression with Balanced Random Forest Classifier

Confusion Matrix:
[   42,    45]
[  442, 16676]

Balanced Accuracy Score:
0.7284689236174061

Of the 87 high-risk loans, 42 were correctly classified; additionally, 442 were incorrectly classified as high-risk.


## Logistic Regression with Easy Ensemble AdaBoost Classifier

Confusion Matrix:
[   79,     8]
[ 1017, 16101]

Balanced Accuracy Score:
0.9243174154247797


# Summary

Of the regressions performed, the Easy Ensemble correctly identified the highest number of high-risk loans (79 out of 87) for a recall score of 91%. 

Correctly identifying high-risk loans is of more importance than incorrectly identifying low-risk loans, as such, it is recommended that for high-risk loan determination the Easy Ensemble algorithm should be used. As a cross-check, another method can be used to see if any of the high-risk loans were incorrectly classified. 