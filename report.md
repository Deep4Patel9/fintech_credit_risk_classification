# Credit_Risk_Classification_Report

## Overview of the Analysis

This anaylsis is used to identify potential high-risk(1) or healthy(0) loan applicants using their 
loan_size, interest_rate, income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt. The data was first split into training and testing data, then it was scaled using StandardScaler. Two LogisticRegression models were created one for the scaled training data and another for the oversampled(over sampling the high-risk(1) loans, in this case, to create a balance between the instances of healthy(0) and high-risk(1) loans) scaled training data. After creating and fitting the models with the data, the model was used to predict y values, in this case healthy(0) or high-risk(1) loans, for the scaled features testing data.

## Results

* Machine Learning Model 1 (Scaled Training Data):
  * The Accuracy Score was 98.9%.. The Precision with which it guesses 0 is 100%(although 10 high-risk loans were predicted as healthy loans) but the recall is 99%. We can see in the confusion matrix that 113 loans were falsely predicted as high-risk loans(1), while 1 is guessed with 84% precision and has a recall of 98%. We can see that some of the high-risk loans have been misidentified due to a lack of data. 



* Machine Learning Model 2 (Oversampled Scaled Training Data):
  * The Accuracy Score is 99.3%. The Precision with which it guesses 0 is 100%(although 4 high-risk loans were predicted as healthy loans) but the recall is 99%. We can see in the confusion matrix that 125 loans were falsely predicted as high-risk loans(1), while 1 is guessed with 83% precision and has a recall of 99%. We can see that althought the model still misidentified 4 loans as healthy it still let less through than the original model which let 10 loans pass. We can also see the the lg_rov model also identified more healthy loans as high-risk than the original model(125 compared to 113).

## Summary

For better predictions of high-risk values I would recommend using the oversampled LogisticRegression model it was able to predict more of the high-risk loan applicants than the original model although it had a higher recall as well since more people were being identified as high-risk. In that case of giving out loans it is better to identify more of the applicants who are high-risk.
