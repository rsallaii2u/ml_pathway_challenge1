# ml_pathway_challenge1

## Overview

The purpose of this analysis is to evaluate different machine learning models using resampling techniques to determina which is better at predicting credit risk.

The target loan_status is 1 if the risk is high and 0 otherwise.

## Results
- Random Oversampling

![alt text](https://github.com/rsallaii2u/ml_pathway_challenge1/blob/main/RandomOverSampler.PNG)

The Random Oversampling is the first model and will be used as a baseline.
The precision for high risk is low compared to low risk. This is indicative of a large number of false positives.
The recall for high and low risk are in line with each other. The lower precision for high risk is also reflected in the dropped f1 score as well.

- SMOTE Oversampling

![alt text](https://github.com/rsallaii2u/ml_pathway_challenge1/blob/main/SMOTEOversampling.PNG)

The precision for high risk is low compared to low risk. This is indicative of a large number of false positives. The result is the same as Random Oversampling.
The recall for high and low risk started to diverge from each other. The f1 score improved 1% for both high and low risk.

- Cluster Centroids Undersampling

![alt text](https://github.com/rsallaii2u/ml_pathway_challenge1/blob/main/ClusterCentroidsUndersampling.PNG)

The precision for high risk is low compared to low risk. This is indicative of a large number of false positives. This is 1% higher than Random Oversampling.
The recall for high and low risk are in line with each other, but about 10% lower than Random oversampling. The f1 score also dropped.

- SMOTEENN Oversampling and Undersampling

![alt text](https://github.com/rsallaii2u/ml_pathway_challenge1/blob/main/SMOTEEN.PNG)

Same results as Cluster Centroids Undersampling

- Balanced Random Forest Classifier Ensemble

![alt text](https://github.com/rsallaii2u/ml_pathway_challenge1/blob/main/BalancedRandomForestClassifier.PNG)

The precision for high risk is low compared to low risk. This is indicative of a large number of false positives. This is 6% higher than Random Oversampling.
The recall for high risk is much lower than for low risk, but the compared to Random Oversampling the f1 score is higher.

- Easy Ensemble AdaBoost Classifier Ensemble

![alt text](https://github.com/rsallaii2u/ml_pathway_challenge1/blob/main/EasyEnsembleClassifier.PNG)

The precision for high risk is low compared to low risk. This is indicative of a large number of false positives. This is 3% higher than Random Oversampling, but 3% lower than Balanced Random Forest Classifier Ensemble.
The recall for high and low risk are in line with each other and about 9% higher than Random oversampling. The f1 score also increased.

## Summary

The ensemble models outperformed the resampling techniques.

A good model to predict credit risk needs to consider the cost benefit of making more false positives than negatives.

If making more false positives than negatives is better one should choose the Easy Ensemble AdaBoost Classifier Ensemble model. Otherwise, the Balanced Random Forest Classifier Ensemble would be a better choice.
