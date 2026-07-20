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

### General machine-learning workflow

1. Understand the problem
First identify:
What do you want to predict?
Is it classification or regression?
Which metric will measure success?
**For Beta Bank:**

*Target: whether a customer leaves*
*Problem: binary classification*
*mportant metrics: F1 score and ROC-AUC*

2. Explore the data

*Understand every column:*

Numerical or categorical?
Which column is the target?
Are the classes balanced?
Are any columns irrelevant?
Are there unusual values or distributions?
3. Clean the data
Handle:
    Missing values
    Duplicate rows
    Incorrect data types
    Impossible or unusual values
    Irrelevant identification columns

`Customer names and customer IDs usually do not help the model.`

**4.** Separate features and target
Features: information used to make predictions
Target: the result you want to predict

**5.** Split the data

Usually divide the data into:

Training set: teaches the model
Validation set: compares models and settings
Test set: evaluates the final model

A common split is 60% training, 20% validation, and 20% test.

**6.** Encode categorical features

Machine-learning models need numbers, so convert categories such as:

* Gender
* Country
* Account type

Common methods:

One-hot encoding: best for categories without an order, such as country
Ordinal encoding: used only when categories have a meaningful order, such as low, medium, and high

7. Standardize numerical features
Standardization puts numerical features on a similar scale.
For example:
Salary may be between 0 and 200,000
Number of products may be between 1 and 4
Scaling prevents large numbers from having too much influence.
It is especially important for:
Logistic Regression
K-Nearest Neighbors
Support Vector Machines
Neural networks
It is generally unnecessary for Decision Trees and Random Forests.
Split data → OHE encoding → standardize numerical columns → train Logistic Regression

10. Train several models
Start with a simple model and then try more complex models:
Logistic Regression
Decision Tree
Random Forest
Gradient Boosting

11. Evaluate and compare models
Choose metrics based on the business problem.

For imbalanced classification:
Precision: When the model predicts a customer will leave, how often is it correct?
Recall: How many customers who actually leave does the model find?
F1 score: Balance between precision and recall
ROC-AUC: How well the model separates the two classes

*`Do not rely only on accuracy when the classes are imbalanced.`*

12. Tune hyperparameters
Adjust model settings to improve performance—for example:
Tree depth
Number of trees
Minimum samples needed for a split

Use the validation set or cross-validation during tuning.

13. Test the final model

Select the best model and evaluate it once on the untouched test set.
This gives a more realistic estimate of how it will perform on new data.

14. Interpret the model
Determine:

Which features are most important?
Does the result make business sense?
Are there possible biases?
What kinds of mistakes does the model make?
15. Communicate the conclusion

Explain:

The problem
How the data was prepared
Which models were tested
Which model performed best
Its final metrics
How the business could use its predictions

The short order to remember is:

Understand → Explore → Clean → Split → Encode → Standardize → Balance → Train → Evaluate → Tune → Test → Explain
Standardization is important for:

Distance-based models (KNN, K-means)
Linear models (Logistic Regression, Linear Regression)
Gradient descent-based models (Neural Networks)
Standardization does NOT matter for:

Tree-based models (Random Forest, Decision Trees, Gradient Boostin)