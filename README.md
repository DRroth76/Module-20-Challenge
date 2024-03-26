The file with the code is entitled "credit_risk_dr" in the Starter_Code folder.

The analysis performed here looks at the risk of loans from a peer-to-peer lending services company. A model was created that can find the trustworthiness of borrowers. The information found in the data included the size of the loan, the interest rate, the income of the borrower, the debt-to-income ratio, the number of accounts, the number of derogatory marks, and the total debt, as well as the loan status (where 0 is a healthy loan and 1 is a high-risk loan). The process starts with importing modules and reading the csv file with the lending information, and to create a DataFrame. The value of "y" is equal to the "loan_status" column, which as was mentioned before, returns a value of either 0 or 1. The value of "X" is equal to all of the columns save the "loan_status" column, which is dropped for this variable. Next using the train_test_split module, the X and y trains and the X and y tests were activated. The input features (X values) and target variables (y values) are randomly split between what is trained (used for the analysis) and what is tested (used for evaluating the model). Next the LogisticRegression method, which is used to conduct regression analysis, was activated and is what the variable "classifier" is set equal to. Then the "fit" method was applied to the X and y trains. This takes the data and learns what it needs and adjusts parameters to improve the accuracy of predictions for future data. The predict_proba is applied to the X test values, which returns an array of sample values, where each row contains values that add up to 1, and correspond to the likelihood that each value in the sample will belong to either class. Next a confusion matrix was created, where rows equal the classes themselves, and the columns represent predicted classes. Finally the classification report provides insight into the effectiveness of the machine learning model.
- Precision (Healthy Loan) - 1.00
- Precision (High Risk Loan) - 0.84
- Recall (Healthy Loan) - 0.99
- Recall (High Risk Loan) - 0.94
- F1 Score (Healthy Loan) - 1.00
- F1 Score (High Risk Loan) - 0.89
- Support (Healthy Loan) - 18765
- Support (High Risk Loan) - 619
- Accuracy - 0.99
- Macro Average (Precision) - 0.92
- Macro Average (Recall) - 0.97
- Macro Average (F1 Score) - 0.94
- Weighted Average (Precision) - 0.99
- Weighted Average (Recall) - 0.99
- Weighted Average (F1 Score) - 0.99

I would recommend this model. For a lending services company, I would deem it of more value to know which loans are the high risk types. While these are not nearly as frequent as a healthy loan, it would be of great benefit to the company to be able to predict the high risk loans and make decisions about them. It would be greater value to minimize the number of high risk loans that are inaccurately seen as healthy rather than vice versa, if there is to be some inaccuracy at all. This model found that 94% of the high risk loans had been accurately predicted as such, whereas 84% of the high risk predictions actually were. Ideally, all precisions and recalls would be equal to 1.00. However, it would seem more acceptable that 16% of predicted high risk loans turned out to be pleasant surprises and 6% of high risk loans being predicted as healthy, than if those numbers were reversed.
