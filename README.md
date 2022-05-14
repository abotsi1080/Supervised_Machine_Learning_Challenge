# Supervised Machine Learning Homework - Predicting Credit Risk

In this project, I built a machine learning model that attempted to predict whether a loan from LendingClub will become high risk or not. 

## Background

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

I used this data to create machine learning models to classify the risk level of given loans. Specifically, I also compared the Logistic Regression model and Random Forest Classifier.

### Retrieve the data

Inside the `Generator` folder in `Resources`, there is a [GenerateData.ipynb](/Resources/Generator/GenerateData.ipynb) notebook that downloaded the data from LendingClub and output two CSVs: 

* `2019loans.csv`
* `2020Q1loans.csv`

I used an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

## Preprocessing: Convert categorical data to numeric

I created a training set from the 2019 loans using `pd.get_dummies()` to convert the categorical data to numeric columns. Similarly, I created a testing set from the 2020 loans, also using `pd.get_dummies()`. There were categories in the 2019 loans that did not exist in the testing set. I used coding to fill in the missing categories in the testing set so that when I fit a model to the training set and try to score it on the testing set as is, I would not get an error. 

## Consider the models

I created and compared two models on this data: a logistic regression, and a random forests classifier. Before creating, fitting, and scoring the models, I made a prediction as to which model would perform better. I predicted that the Logistic Model would be the best model to predict with the highest accuracy on the unscaled data but however predicted that the with scaled data, the Random Forests Classifier model would be the best predicting model with the highest level of accuracy. Detail information can be seen in the summary prediction below.
![Summary Prediction](Summary_Prediction.md)

## Fit a LogisticRegression model and RandomForestClassifier model

I created a LogisticRegression model, fitted it to the data, and printed the model's score. I performed the same for a Random Forest Classifier. 

## Revisit the Preprocessing: Scale the data

The data going into these models was never scaled originally, an important step in preprocessing. I used the `StandardScaler` to scale the training and testing sets. Before re-fitting the LogisticRegression and Random Forest Classifier models on the scaled data, I made another prediction about how as described in the "Consider the models" above.

I fitted and scored the Logistic Regression and Random Forest Classifier models on the scaled data. The summary report is provided in the summary prediction below.
![Summary Prediction](Summary_Prediction.md)
