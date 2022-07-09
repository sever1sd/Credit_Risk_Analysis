# Credit Risk Analysis

## Purpose

The purpose of this analysis was to review publically available credit card risk data from LendingClub and utilize supervised machine learning to create models to create credit riskiness. Because good loans generally out number risky loans, evaluating credit risk is an inherently unbalanced classification problem. As such, six different variants of machine learning models were used to determine the model that best fits the data. The models used were "RandomOverSampler," "SMOTE," "ClusterCentroids," "SMOTEENN,"BalancedRandomForestClassifier," and "EasyEnsembleClassifer."

## Model Results

"Loan Status" was the primary driver of this analysis. It was used to determine whether a data point was considered "low" or "high" risk. 

### Over Sample Models

1. RandomOverSampler

![alt text](https://github.com/sever1sd/Credit_Risk_Analysis/blob/42fe1425006ff129af6742123ef834e35c802a69/Images/RandomOverSampler.png)

* This model had an accuracy score of ~64%
* The "high risk" category had a precision of 1% and recall of 71%
* The "low risk" category had precision of 100% and recall of 58%

2. SMOTE

![alt text](https://github.com/sever1sd/Credit_Risk_Analysis/blob/42fe1425006ff129af6742123ef834e35c802a69/Images/SMOTE.png)

* This model had an accuracy score of ~66%
* The "high risk" category had a precision of 1% and recall of 63%
* The "low risk" category had precision of 100% and recall of 68%

### Under Sample Model

3. ClusterCentroids

![alt text](https://github.com/sever1sd/Credit_Risk_Analysis/blob/42fe1425006ff129af6742123ef834e35c802a69/Images/ClusterCentroids.png)

* This model had an accuracy score of ~66%
* The "high risk" category had a precision of 1% and recall of 69%
* The "low risk" category had precision of 100% and recall of 40%

### Combinatorial Model

4. SMOTEENN

![alt text](https://github.com/sever1sd/Credit_Risk_Analysis/blob/42fe1425006ff129af6742123ef834e35c802a69/Images/SMOTEEN.png)

* This model had an accuracy score of ~65%
* The "high risk" category had a precision of 1% and recall of 72%
* The "low risk" category had precision of 100% and recall of 57%

### Bias Reduction Models

5. BalancedRandomForestClassifier

![alt text](https://github.com/sever1sd/Credit_Risk_Analysis/blob/42fe1425006ff129af6742123ef834e35c802a69/Images/BalancedRandomForestClassifier.png)

* This model had an accuracy score of ~79%
* The "high risk" category had a precision of 1% and recall of 70%
* The "low risk" category had precision of 100% and recall of 87%

6. EasyEnsembleClassifier

![alt text](https://github.com/sever1sd/Credit_Risk_Analysis/blob/42fe1425006ff129af6742123ef834e35c802a69/Images/EasyEnsembleClassifier.png)

* This model had an accuracy score of ~92%
* The "high risk" category had a precision of 9% and recall of 92%
* The "low risk" category had precision of 100% and recall of 94%

## Summary

Each of the models generally had low precision when evaluating high credit risk. Of the six models tested, however, the EasyEnsembleClassifier performed best with an accuracy of 92%, precision of 9% and recall of 92% for high risk applications, and a precision of 100% and recall of 94% for low risk applications. This suggest that nearly 92% of all high risk applications are captured using this model. Due to the low precision, however, the model is also capturing low risk applications and classifying them as high risk. None of these models have high precision metrics, so it is recommended that other models are researched to determine if they could be more successful as predicting credit risk. In the interim, however, the EasyEnsembleClassifier is the best choice because it will capture the overwhelming majority of high risk applications. While it does also capture low risk applications, it is better to over-capture low risk applications than miss a significant portion of high risk applications. 
