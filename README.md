# Credit_Risk_Analysis
Assessing the probability of credit default using Machine Learning techniques

## Overview

The purpose of this project is to build a machine learning model using prior loan information to qualify future applicants as high risk borrowers or low risk borrowers. Due to he wide range of algorithms to choose from, this project aims to determine which of six machine learning algorithms most accurately flags applicants. Given the very small number of high risk applicants (347 vs 68470) in the training data, a number of over- and under-sampling algorithms were chosen. The input data is scaled to assist the algorithms in processing. 

## Results 

 - Random Over Sampler 
    - Balanced Accuracy Score: 78.6%
    - Precision: 2% of high risk, 100% of low risk
    - Recall: 71% of high risk, 86% of low risk

- SMOTE Oversampling
    - Balanced Accuracy Score: 79.7%
    - Precision: 3% of high risk, 100% of low risk
    - Recall: 71% of high risk, 88% of low risk

- Cluster Centroids
    - Balanced Accuracy Score: 77.4%
    - Precision: 2% of high risk, 100% of low risk
    - Recall: 78% of high risk, 77% of low risk

- SMOTEEN sampling
    - Balanced Accuracy Score: 79.8%
    - Precision: 3% of high risk, 100% of low risk
    - Recall: 72% of high risk, 87% of low risk

- Balanced Random Forest Classifier
    - Balanced Accuracy Score: 77.8%
    - Precision: 3% of high risk, 100% of low risk
    - Recall: 68% of high risk, 88% of low risk

- AdaBoost Classifier
    - Balanced Accuracy Score: 64.9%
    - Precision: 93% of high risk, 100% of low risk
    - Recall: 30% of high risk, 100% of low risk

## Summary

From our experimentation, we were able to come accross some interesting results. Most of our algorithms found it very difficult to identify high risk borrowers. All of our algorithms were able to identify 100% of the low risk borrowers, so each algorithm's ability to spot high risk borrowers is their determining factor. 

Despite having the lowest balanced accuracy score, our final AdaBoost Classifier was successfully able to identify 93% of all high risk borrowers, in addition to 100% of low risk borrowers. The low recall rate of 30% for high-risk applicants implies that this algorithm flags more low-risk borrowers as high-risk than the others. With such a high degree of precision, however, this may actually be in the best interest of the lending institution. Erring on the 'safe side' would allow the institution to hedge itself against credit default by qualifying a dispropportionate - but not prohibitive - number of low-risk applicants as high-risk. 

Given this information, we would recommend using the AdaBoost Classifier to identify future applicants as high- or low-risk. Its high degree of precision and error in the favor of the lending institution both would make this the most viable option for automatically flagging future loan applicants. All other algorithms had a detrimentally small percentage of high-risk applicants successfully flagged, opening up the institution to dramatic credit risk. 