# Credit Risk Analysis

## Overview

This analysis is to compare different types of supervised machine learning algorithms used to predict whether a loan will be low-risk or high-risk based on various input factors. Approaches include oversampling, undersampling, combination, random forest, and ensemble models.

## Results

The input data was imbalanced as it contained 68,470 low risk loans but only 347 high risk loans.

For each model, the classifier was trained on a subset of the data and tested on a different subset to evaluate its success. For each one, a balanced accuracy score, confusion matrix, and classification report were produced e.g. as follows:

![Undersampling model statistics](<./undersampling_stats.png>)

Summary results for each of the six tested models are as follows.

* Naive Random Oversampling
  * Balanced accuracy score: 0.7856360112968401
  * Precision: 0.99
  * Recall: 0.86
* SMOTE Oversampling
  * Balanced accuracy score: 0.7966770207605626
  * Precision: 0.99
  * Recall: 0.88
* Cluster Centroid undersampling
  * Balanced accuracy score: 0.7742313998976678
  * Precision: 0.99
  * Recall: 0.77
* SMOTEENN (combination)
  * Balanced accuracy score: 0.7983056754132573
  * Precision: 0.99
  * Recall: 0.87
* Balanced Random Forest
  * Balanced accuracy score: 0.9063644289450741
  * Precision: 0.99
  * Recall: 0.91
* Easy Ensemble AdaBoost
  * Balanced accuracy score: 0.9426910781749491
  * Precision: 0.99
  * Recall: 0.94

## Summary

Each of the models was capable of classifying low-risk loans with a high degree of accuracy (precision of 1.00 in the imbalanced classification report for all models). However, the challenge is correctly identifying the high-risk loans. The balanced accuracy score for the Easy Ensemble AdaBoost model is highest at 0.94 and is also reflected in the recall and F1 statistics which are both higher than all other models:

![Easy Ensemble AdaBoost statistics](<./easy_ensemble.png>)

Due to the higher performance on the split training/testing data it appears the AdaBoost model performs the best and should be selected for the greatest accuracy.
