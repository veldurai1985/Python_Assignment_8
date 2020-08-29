## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, a client has asked that you help them predict credit risk with machine learning techniques.

In this assignment you will build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so you will need to employ different techniques for training and evaluating models with imbalanced classes. You will use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

- - -

### Files

[Resampling Notebook](credit_risk_resampling.ipynb)

[Ensemble Notebook](credit_risk_ensemble.ipynb)

### Data

[Lending Club Loans Data](Resources/LoanStats_2019Q1.csv.zip)

- - -

#### Resampling

* Which model had the best balanced accuracy score?
    - Of all the models, Naive Random Oversampling and SMOTE Oversampling have the best accuracy score (0.9936781215845847)
 
* Which model had the best recall score?
    - Of all the models, Naive Random Oversampling, SMOTE Oversampling and SMOTEENN have the best recall score (0.99) for all the classification (High_Risk, Low_Risk and Combined Avg).
>
* Which model had the best geometric mean score?
    - Except Simple Logistic Regression, All the models have the best geo score (0.99) for all the classification (High_Risk, Low_Risk and Combined Avg).

#### Ensemble Learning

* Which model had the best balanced accuracy score?
    - Between Balanced Random Forest Classifier and an Easy Ensemble AdaBoost classifier mode, Easy Ensemble AdaBoost Classifier has a better balanced accuracy score (0.9931452145768576). But, the difference is not much and it is too close. 
   - Balanced Random Forest Classifier = 0.9927988250218349 Vs Easy Ensemble AdaBoost Classifier = 0.9931452145768576

* Which model had the best recall score?
    - Both models have the same recall score for all of the parameters (High_Risk, Low_Risk and Combined Avg)
    - Balanced Random Forest Classifier 
        - High_Risk_Recall = 0.99
        - Low_Risk_Recall  = 0.99
        - Avg_Recall       = 0.99

    - Easy Ensemble AdaBoost Classifier 
        - High_Risk_Recall = 0.99
        - Low_Risk_Recall  = 0.99
        - Avg_Recall       = 0.99

* Which model had the best geometric mean score?
    - Both models have the same geo score for all of the parameters (High_Risk, Low_Risk and Combined Avg)
    - Balanced Random Forest Classifier 
        - High_Risk_Geo   = 0.99
        - Low_Risk_Geo    = 0.99
        - Avg_Geo         = 0.99

    - Easy Ensemble AdaBoost Classifier 
        - High_Risk_Geo   = 0.99
        - Low_Risk_Geo    = 0.99
        - Avg_Geo         = 0.99  


* What are the top three features?
    As per Balanced Random Forest Classifier, These are all the top three features.
    - (0.21788480603139448, 'borrower_income')
    - (0.19595880072166166, 'interest_rate')
    - (0.1770964986362893, 'debt_to_income')
- - -
