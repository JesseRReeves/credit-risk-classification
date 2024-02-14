The purpose of this analysis was to train and evaluate a model based on loan risk.  The financial information used was of historical lending activity from a peer-to-peer lending services company.  This dataset was used to build a model that can identify the creditworthiness of borrowers, based on healthy loans, and high-risk loans.

Here within our dataset we had multiple variables:

- Size of Loan
- Interest Rate
- Borrower's Income
- Debt to Income Ratio
- Number of Accounts
- Derogatory Marks
- Total Debt
- Loan Status
The Loan Status had a '0', representing a healthy loan, and a '1' representing a high-risk loan.

The Stages of the Machine Learning Process:

1. Read the csv data into a pandas DataFrame.
2. Set the loan_status column as y.
3. Separate the X variable, making sure to drop the loan_status column.
4. Split the data into training and testing datasets by using train_test_split
5. Fit a logistic regression model by using the training data (X_train and y_train)
6. Validate the model using the testing data.
7. Save the predictions on the testing data labels by using the testing feature data (X_test and the fitted model.)
8. Calculate the Accuracy Score
9. Generate a confusion matrix to evaluate the model's performance.
10. Print the classification report.

Various methods used:

- train_test_split: splitting our data into train and test.  This is to avoid poor performance.  
- Logistic Regression: Used to predict the probable outcome of a borrower being a healthy, or high-risk asset.
- Accuracy Score: Confirms the accuracy of our logistic regression model.
- Confusion Matrix:  Shows the performance of our classification model.
- Classification Report: Displays all the information in an organized fashion.

Results:

* Balanced Accuracy Score: The Average of recall.  (1.00 + .95)/2 = .975 or 97.5% accuracy
* Precision Scores: Measures the number of correct positive predictions made. For healthy loans, this was 1.00, or 100%.  For high-risk loans, this was .87, or 87%.
* Recall Scores: Shows us the true positive rate.  For healthy loans, this was 1.00, or 100%.  For high-risk loans, this was .95 or 95%.
* F1-score: Measures the quality of a classification model.  Calculated harmony of precision and recall.  For healthy loans this was 1.00, or 100%.  For high-risk loans, this was .91, or 91%.

Summary
To summarize, our logistic regression model seems to have done a great job at predicting the creditworthiness of borrowers.  When it comes to healthy loans, our testing data sets came back with an accuracy score of .9939.  Across the precision, recall, and f1-score columns, healthy loans were predicted at 1.00(Precision Scores), the true positive rate was 1.00(Recall Scores), and the quality of the classification model was 1.00(f1-Score).  When the high-risk loan scores were calculated, what was obtained was a precision score(correct positive predictions) of .87, recall(true positive rate) of .95, and the f1-score(quality of the model) of .91.  This shows that our model is able to capture most of the positive data points, and our quality is very high.  The precision score is what worries me.  It is more important to be able to predict the high-risk loans for any lending company.  Yet our model predicts 87% of these loans correctly.  In my opinion, our logistic model works well, however before I would recommend this model, I would want to try a few more different models to see if they can predict more than 87% of the high-risk loans.

