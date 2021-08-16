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

Classification Report:

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       1.00      0.01      1.00      0.02      0.11      0.01        87
   low_risk       1.00      1.00      0.01      1.00      0.11      0.01     17118

avg / total       1.00      1.00      0.02      0.99      0.11      0.01     17205


Of the 87 high-risk loans, the Logistic regression without applying and oversampling or undersampling algorithms, only 1 was correctly classified. 


## Logistic Regression with Random Oversampling

Confusion Matrix:
[   54,    33]
[ 5498, 11620]

Balanced Accuracy Score:
0.6376117496807152

Classification Report:

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.62      0.68      0.02      0.65      0.42        87
   low_risk       1.00      0.68      0.62      0.81      0.65      0.42     17118

avg / total       0.99      0.68      0.62      0.80      0.65      0.42     17205


Of the 87 high-risk loans, 54 were correctly classified; however, 5,498 were incorrectly classified as high-risk.


## Logistic Regression with SMOTE Oversampling

Confusion Matrix:
[   55,    32]
[ 5879, 11239]

Balanced Accuracy Score:
0.6443721269403855

Classification Report:

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.63      0.66      0.02      0.64      0.41        87
   low_risk       1.00      0.66      0.63      0.79      0.64      0.42     17118

avg / total       0.99      0.66      0.63      0.79      0.64      0.42     17205


Of the 87 high-risk loans, 55 were correctly classified; additionally, 5,879 were incorrectly classified as high-risk.


## Logistic Regression with ClusterCentroids Undersampling

Confusion Matrix:
[  53,   34]
[9428, 7690]

Balanced Accuracy Score:
0.5292150629907619

Classification Report:

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.61      0.45      0.01      0.52      0.28        87
   low_risk       1.00      0.45      0.61      0.62      0.52      0.27     17118

avg / total       0.99      0.45      0.61      0.62      0.52      0.27     17205

Of the 87 high-risk loans, 53 were correctly classified; additionally, 9,428 were incorrectly classified as high-risk.


## Logistic Regression with SMOTEENN Combination Sampling

Confusion Matrix:

[  61,   26]
[7291, 9827]

Balanced Accuracy Score:
0.6376117496807152

Classification Report:

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.70      0.57      0.02      0.63      0.41        87
   low_risk       1.00      0.57      0.70      0.73      0.63      0.40     17118

avg / total       0.99      0.57      0.70      0.73      0.63      0.40     17205


Of the 87 high-risk loans, 61 were correctly classified; additionally, 7,291 were incorrectly classified as high-risk.

## Logistic Regression with Balanced Random Forest Classifier

Confusion Matrix:
[   42,    45]
[  442, 16676]

Balanced Accuracy Score:
0.7284689236174061

Classification Report:

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.09      0.48      0.97      0.15      0.69      0.45        87
   low_risk       1.00      0.97      0.48      0.99      0.69      0.49     17118

avg / total       0.99      0.97      0.49      0.98      0.69      0.49     17205


Of the 87 high-risk loans, 42 were correctly classified; additionally, 442 were incorrectly classified as high-risk.


## Logistic Regression with Easy Ensemble AdaBoost Classifier

Confusion Matrix:
[   79,     8]
[ 1017, 16101]

Balanced Accuracy Score:
0.9243174154247797

Classification Report:

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.07      0.91      0.94      0.13      0.92      0.85        87
   low_risk       1.00      0.94      0.91      0.97      0.92      0.86     17118

avg / total       0.99      0.94      0.91      0.96      0.92      0.86     17205


# Summary

Of the regressions performed, the Easy Ensemble correctly identified the highest number of high-risk loans (79 out of 87) for a recall score of 91%. 

Correctly identifying high-risk loans is of more importance than incorrectly identifying low-risk loans, as such, it is recommended that for high-risk loan determination the Easy Ensemble algorithm should be used. As a cross-check, another method can be used to see if any of the high-risk loans were incorrectly classified. 