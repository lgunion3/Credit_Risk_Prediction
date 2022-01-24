# Credit_Risk_Analysis
---
Data Preparation, Statistical Reasoning and Machine Learning: Predicting Credit Card Risk

## Challenge Overview
---
The purpose of this project is to apply supervised machine learning alogthrims to determine credit card risk. It is in the best interest of financial institutions, banks, and peer-to-peer lending firms to automate and improve the accuracy of detecting high-risk individuals, prior to granting loans to assure minimal default. With machine learning, it is particullary challenging due to imbalanced distribution of risk classification (low risk vs high risk), as in a given sample dataset, there are substanitally more low-risk applicants than low-risk. 

To due to the difficulty of screening for fewer high-risk applicants, it is beneficial to deploy various ML models, that reduce bias and resample datasets to determine the best methodology or alogothrim to accurately predict credt-card risk. We delve into 6 different models and make a recommendation for ML implementation.

## Features and Data Resources
---
- Data Source: `LoanStats_2019Q1.csv`
- Data Tools: `credit_risk_resampling.ipynb` and `credit_risk_emsembler.ipynb`
- Software: `imbalanced-learn`, `skikit-learn`, `Jupyter Notebook` and `Python.9.2.3`

## Challenge Deliverables 
---
- Deliverable 1: Use Resampling Models to Predict Credit Risk
- Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
- Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
- Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)

## Results 
---
- Resampling Machine Learning Models (4)

<img width="819" alt="resampling_summary" src="https://user-images.githubusercontent.com/77628698/121818399-f3879400-cc54-11eb-85a5-690f4073d5fd.png">

- Ensemble Classifers (2)
<img width="717" alt="D3_summary" src="https://user-images.githubusercontent.com/77628698/121818470-511be080-cc55-11eb-8413-b0b19324f3d9.png">

 Top ML Models: Performance Metrics
 ---
- Best Overall Balanced Accuracy Score: __Easy Ensemble Classifer__ (93%)
- Best Overall Precision: __Easy Ensemble Classifer__ (9%)
- Best Overall Recall: __Easy Ensemble Classifer__ (92%)
---

- _Technical Analysis_

1. Naive Random Oversampling 

<img width="806" alt="naive_random" src="https://user-images.githubusercontent.com/77628698/121818612-431a8f80-cc56-11eb-83f1-cd9cf5b1b21c.png">

2. SMOTE Oversampling 

<img width="809" alt="SMOTE" src="https://user-images.githubusercontent.com/77628698/121818616-49107080-cc56-11eb-9c54-23ca1c885a8e.png">

3. ClusterCentroids Undersampling 
<img width="809" alt="clustercentroids" src="https://user-images.githubusercontent.com/77628698/121818622-5299d880-cc56-11eb-86e2-39545dde04cf.png">

4. SMOTEENN Combination Sampling

<img width="797" alt="SMOTEENN" src="https://user-images.githubusercontent.com/77628698/121818627-57f72300-cc56-11eb-9c49-49e72fa320da.png">


5. BalancedRandomForestClassifer 

<img width="716" alt="BalancedRandomForestClassifer" src="https://user-images.githubusercontent.com/77628698/121818631-60e7f480-cc56-11eb-87b0-ee8e3e13118d.png">

5. EasyEnsembleClassifer

<img width="708" alt="EasyEnsembleClassifier" src="https://user-images.githubusercontent.com/77628698/121818635-66ddd580-cc56-11eb-8a0d-1d72d3d892b2.png">

## Summary 
As shown by the summary dataframes and individual model testing, both Ensemble Classifiers outperformed the Resampling techniques in accurately predicted high-risk credit card applicants and low-risk applicants, given the features used to classify each group of potential loanees. In the case of screening for high-risk individuals, high sensitivty outweighs precision performance of the model--it is better to minimize false negatives and let those high-risk indivudals slip through the test undetected, in the instance of protecting the interests of the loaning companies. 

_Recommendation Based on Model (6) Performance_
However, all 6 models produced very low precision scores. In other words, at best, machine learning produced a 9% reliability that those that were identified as high-risk, were actually high risk. With a 91% chance of a False Positive result, where a low-risk applicant is lableed as high-risk, I cannot recommend any of the models tested in this project for implementation--regardless of high sensitivity, financial institutions risk losing 91% of future customers and revenues of low-risk applicants when they are rejected for a credit-card. A group of these False Positives will file a claim and resolve the declined application, but many will take their business elsewhere, unwilling to take on the headache of disputing the decision with the credit card company.





