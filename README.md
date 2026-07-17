# Beta-Bank-project


### Project description
Beta Bank customers are leaving: little by little, they are being chipped away every month. The bankers have figured out that it’s cheaper to save the existing customers rather than to attract new ones.

We need to predict whether a customer will leave the bank soon. You have the data on clients’ past behavior and termination of contracts with the bank.

Build a model with the `maximum possible F1 score`. To pass the review, you need an `F1 score of at least 0.59 `for the test dataset.

Additionally, measure the   `AUC-ROC metric` and `compare it with the F1 score.`

#### Project instructions

1- Download and prepare the data. Make sure that you explain the logic you follow during preparation.
2- Examine the balance of classes. Train the model without taking into account the imbalance. Briefly describe your findings.

3- Improve the quality of the model. Make sure you use at least two approaches to fixing class imbalance. Use training and validation sets to find the best model and the best set of parameters. Briefly describe your findings.
4- Perform the final testing.
##### Data description
The data can be found in the/datasets/Churn.csv file. Download the dataset.

**Features**

`RowNumber` — data string index
`CustomerId` — unique customer identifier
`Surname` — surname
`CreditScore` — credit score
`Geography` — country of residence
`Gender` — gender
`Age` — age
`Tenure` — length of service for customer
`Balance` — account balance
`NumOfProducts` — number of banking products used by the customer
`HasCrCard` — customer has a credit card (1 - yes; 0 - no)
`IsActiveMember` — customer’s activeness (1 - yes; 0 - no)
`EstimatedSalary` — estimated salary

**Target**

Exited — сustomer has left (1 - yes; 0 - no)