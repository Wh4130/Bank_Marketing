# Bank_Marketing

This is Huang Lin, Chun's side project for machine learning. 
I used the data downloaded from https://archive.ics.uci.edu/ to practice a classification problem.

Please refer to [Bank_Marketing.ipynb](https://github.com/Wh4130/Bank_Marketing/blob/main/Bank_Marketing.ipynb) for the complete model.

# Predict whether a person will subscribe the term deposit program by the following features 
- age
- marital status
- education
- profession
- financial status (balance, default, loan, housing...)
- whether they received contact in the previous campaign
- the duration of the latest contact
and so on...

# Data Preprocessing
## Exploratory Data Analysis
### Analysis on dummies
I analyzed each dummy independent variable's distribution on the outcome variable.

Here is the graph.
![Features](https://github.com/Wh4130/Bank_Marketing/assets/90643963/08deb7dc-1bb7-4297-a381-8878dd70555b)
- job: **students** and **retired people** are more willing to subscribe a term deposit.
- education: people with **higher education** tend to subscribe a term deposit.
- default, housing, loan: people **without financial burden** tend to subscribe a term deposit.
- previous outcome: people who **subscribed in the previous** marketing campaign tend to subscribe a term deposit.

### One-hot encoding
As some variables like education, profession, and marital status are catagorical variables, we should transform them into dummies so that the computer can run the model for us.

If a variable has more than two values, I would seperate the variable into several dummies and eliminate one to aviod the problem of Collinearity.

### Feature Importance
![Feature_impo](https://github.com/Wh4130/Bank_Marketing/assets/90643963/3227b736-8f2a-4a48-941c-8fe2a13a4e80)

### Split the data set
Splitted the data set into three parts: Training set, validation set, and testing set.
- Training set (70%):
  The data set that used to train models
- Validation set (15%):
  The data set that used to compare the fitness or accuracy across models
- Testing set (15%):
  The data set that used to evaluate the fitness or accuracy of the final model.
 
### Feature Scaling
To aviod the situation that a model put different weight on different features, we have to standardize features.
Feature scaling is always conducted after data set splitting

### Modelling
- Logistic Regression
- K Nearest Neighbors
- Naive Bayes
- Decision Tree
- Random Forest

Finally, we found that Naive Bayesian Classifier is the most suitable model for this case. (With the least degree of overfitting)

GaussianNB()
-------------------------------
**confusion matrix**: 

[[5035  934]

[ 439  374]]

**accuracy** = 0.7975523444411678

**recall** = 0.46002460024600245

**precision** = 0.28593272171253825


