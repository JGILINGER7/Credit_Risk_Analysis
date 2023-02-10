# Credit_Risk_Analysis
## Overview
The goal of this analysis is to use supervised machine learning to analyze credit risk. To that end we used oversampling, undersampling, combination sampling, and boosting to try and get the most accurate analysis possible. 

## Results
Most tests resulted in low accuracy with the first 4, oversampling, undersampling, smote oversampling, and combination falling under 70% accuracy. This shows a disqualifying problem with these methods. ![Alt text](resources/overacc.png) seen here the score using the Random Oversampler and its accompanying classification report ![Alt text](resources/classrepover.png) show a failure to classify high risk credit. This same probllem is seen in the other 4 tests in credit_risk_resampling.ipynb. It is not until the final test with Easy Ensemble that we find a test with both high precision and recall scores. ![Alt text](resources/classrepeasy.png). 

## Summary 
The only model I can reccomend is the Easy Ensemble and even with those results I feel we need an improvement in the data to help further train this model, the first suggestion I'd make is removing the issue_date, payement_dude and verification columns to reduce noise, I would also look into if any additional columns that could be removed. The biggest singular issue with this is a lack of high risk examples for the model to train on so reducing noise and simplifying the model will mark the biggest improvement short of adding a few thousand additional high risk loans into the model. 