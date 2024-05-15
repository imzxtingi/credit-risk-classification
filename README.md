# Credit Risk Classification

## Overview of the Analysis
The purpose of this analysis is to create a logistic regression model that would predict credit loan risks.  The data was from historical lending activity that included a target "loan_status" column which determined whether a loan was healthy `0` or high-risk `1`.  The features of the model include loan size, interest rate, borrower income, debt to income, number of accounts, derogatory remarks, and total debt.  The model is created to predict the status of the loans so that the company can identify the creditworthiness of borrowers. A logistic regression model was used for its ability to classify binary outcomes which is useful for identifying cases of fraud or credit risk.  

The data was split into training and testing sets, then a logistic regression model was fit on the training data.  The predictions were made on the fitted model with test data and a confusion matrix and classification report was created to assess the reliability of the model. 

## Results

![Screenshot 2024-05-15 163325](https://github.com/imzxtingi/credit-risk-classification/assets/150073701/206c2884-4b9c-47dd-b402-220498b20fb9)

* Machine Learning Model 1: Logistic Regression
    * The healthy loans `0` had 100% precision, recall, and f1-score.  This shows that the model accurately predicted the outcome for healthy loans 100% of the time.
    * The high-risk loans `1` had 87% precision, 89% recall, and 88% f1-score.  Precision measures how many positive predictions are true positives.  Recall measures how many cases of positives were correctly predicted.  The f1-score is a weighted average of the precision and recall.  The model is not as accurate for high-risk loans as it was for healthy ones.  It is accurately predicting around 88% of high-risk loans.
    * The lower accurary for high-risk loans can be attributed to the imbalance of healthy loans to high-risk ones.  Generally, healthy loans outnumber high-risk ones.  The model supported 18759 cases for healthy loans `0` whereas it only supported 625 high-risk loans `1`.  This can cause the logistic regression model to be less accurate since it is being weighted more heavily by healthy loans.  

## Summary
The model did well to predict healthy loans and less accurately for high-risk loans.  While it is important to identify both, it is more beneficial to the lender to be able to identify when a loan will default, therefore accurately predicting high-risk loans `1` is crucial for the lending company.  With this model, the lender would be able to accurately identify all healthy loans, with decreased accuracy for high-risk ones. 

I would try to adjust the classes to help with the imbalance between healthy loans and high-risk ones to get a model that will better identify high-risk loans.  While the current model isn't terrible at predicting credit risk, it can be improved upon.  I would still cautiously recommend this model be used as it still has relatively high accuracy scores.  
