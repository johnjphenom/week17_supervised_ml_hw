# Supervised Machine Learning and Credit Risk

## Overview of the Analysis
In the realm of credit risk there is an inherently unbalanced classification problem. This is because good loans far outweigh the risky loans. In order to truly determine the best process to take one will need to employ different techniques to train and evaluate models and unbalanced classes. First is resampling, with imbalanced-learn and sci-kit learn. First oversampling will take place with RandomOverSampler and then SMOTE algorithms. Then it will move on to under sampling with ClusterCentroids. After this a combinatorial approach with the SMOTEENN algorithm is required. Lastly, the two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, with be employed and evaluated.

## Results

RandomOverSampler
  Balanced Accuracy Score = .6573
  High Risk Precision Score = .01
  Low Risk Precision Score = 1.0
  High Risk Recall Score = .71
  Low Risk Recall Score = .60

SMOTE
  Balanced Accuracy Score = .6622
  High Risk Precision Score = .01
  Low Risk Precision Score = 1.0
  High Risk Recall Score = .63
  Low Risk Recall Score = .69

ClusterCentroids
  Balanced Accuracy Score = .5442
  High Risk Precision Score = .01
  Low Risk Precision Score = 1.0
  High Risk Recall Score = .69
  Low Risk Recall Score = .40

SMOTEENN
  Balanced Accuracy Score = .6392
  High Risk Precision Score = .01
  Low Risk Precision Score = 1.0
  High Risk Recall Score = .70
  Low Risk Recall Score = .58

BalancedRandomForestClassifier
  Balanced Accuracy Score = .7885
  High Risk Precision Score = .03
  Low Risk Precision Score = 1.0
  High Risk Recall Score = .70
  Low Risk Recall Score = .87

EasyEnsembleClassifier
  Balanced Accuracy Score = .9155
  High Risk Precision Score = .05
  Low Risk Precision Score = 1.0
  High Risk Recall Score = .93
  Low Risk Recall Score = .90
  
## Summary

The six different methods utilized in this testing and analysis performed to varying degrees of success. From a quick glance it is apparent that both of the ensemble algorithms did much better than any of those in the resampling section. This difference becomes most stark when looking at the recall score. This is important because it shows that those who have high-risk credit scores, will be categorized correctly. The lowest of these scores is with SMOTE at .63 and is greatly outperformed by the EasyEnsembleClassifier with a High-Risk Recall Score of .93. This shows that in order provide the best predictive measures it is necessary to use an ensemble algorithm and, in this case, specifically the EasyEnsembleClassifier.
