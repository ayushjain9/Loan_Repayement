# Loan_Repayement

# Overview of DataSet
Lending Club is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface.

# Objective
Given historical data on loans given out with information on whether or not the borrower defaulted (charge-off), we build a model that can predict whether or nor a borrower will pay back their loan. This way in the future when we get a new potential customer we can assess whether or not they are likely to pay back the loan.

Classification metrics will be used when evaluating the performance of our model.

# Exploratoy Data Analysis
Data set is pretty imbalanced as expected where positive examples (“not paid fully”) are only 20%.


Installment and loan_amnt has perfect correlation

# Feature Engineering
* Missing data should be either removed or filled.
* Removing similar one of the column such as 'purpose' and 'title' have same description.
* Filled the missing value of mort_acc with mean of total_acc.
* Converting categorical variable to dummy variables.
* Column with zipcode and address converted trimmed to pincode and then to dummy variable.
* Issue date removed as we need to predict loan_status before issue of loan.

# Model Building
I split the training data and test data as 20% my test data. Also I have also normalized the data using MinMax Scalar function.

Model I tried:
* Bagging classifier using decison tree as base
* Random Forest classifier
* ANN

# Model performance
ANN gives higher accuracy score  which is 90%.

# Conclusion
There is no definitive guide of which algorithms to use in an imbalanced data situation. What may work on some data sets may not necessarily work on others. Therefore, always evaluate methods using cross validation to get a reliable estimates.
False Negatives are a lot more expensive than False Positives
