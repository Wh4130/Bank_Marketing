# Bank_Marketing

This is Huang Lin, Chun's side project for machine learning. 
I used the data downloaded from https://archive.ics.uci.edu/ to practice a classification problem.

Please refer to Bank_Marketing.ipynb for the complete model.

## Predict whether a person will subscribe the term deposit program by the following features 
- age
- marital status
- education
- profession
- whether they received contact in the previous campaign
- the duration of the latest contact
and so on...

## Data Preprocessing
### Exploratory Data Analysis


### One-hot encoding
As some variables like education, profession, and marital status are catagorical variables, we should transform them into dummies so that the computer can run the model for us.

If a variable has more than two values, I would seperate the variable into several dummies and eliminate one to aviod the problem of Collinearity.

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
- Support Vector Machine
- Kernel SVM
  -   linear
  -   poly
  -   rbf
  -   sigmoid
- Naive Bayes
- Decision Tree
- Random Forest





