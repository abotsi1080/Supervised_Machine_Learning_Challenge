# Supervised Machine Learning Homework - Prediction to the Machine Learning Dataset


## Initial Prediction
 There are two models involved in this study, a logistic regression and a random forests classifier. A quick study of the data set (the 2019loans.csv and the 2020Q1loans.csv), the data was cleaned before further analysis and prediction models applied. To have a better prediciton, one needs to understand what each of the two different models employed is this analysis are doing. I do have a little more description on each of the two models in the Evaluation of the Models below. I do however predict that the Random Forests Classifier model have will have the best prediction outcome compared to the Logistic Regression model.


## Evaluation of the Models
In the evaluation of the models utilized in the analysis, one needs to first of all understand the two models capabilities and their differences as well. 

The logistic regression take a path anlysis approach which uses a generalized linear equation to describe the diected dependencies among the set of variables in our data set. in this case, we focuse more on a number of statistical assumptions that must be met and overfitting becomes a concern just as well as outliers. The final model should be parsimonious and balanced and then can consider the the assessment of goodness of fit.

In the case of the random forest, the classification and predictions are based on a top-down induction approach by averaging many decision trees together. There are no statistical assumptions in this model and can handle multicolinearity. It is therefore robust to overfitting and outliers. The random inputs and random features tend to produce better results in the model.

In our case, it is very important to scale the data to give every datapoint a weight so as to make sure the entire dataset is robust and minimize outliers in the analysis steps.

## Results with the scaled data
With the unscalled data,the Logistic Regression model produced the results below:
    Training Data Score: 0.6547619047619048
    Testing Data Score: 0.5178647384091876
while the Random Forests model produced the results below:
    Training Score: 1.0
    Testing Score: 0.6399404508719694

With the scaled data, the Logistic Regression model produced the results below:
    Training Data Score: 0.7061576354679803
    Testing Data Score: 0.6599319438536793
While with the scaled data, the Random Forests model produced the results below:
    Training Score: 0.5
    Testing Score: 0.5
    
## Final Summary
Based on the results produced, it is clear that the Logistic Model in this case is the best predictor model in this analysis. Even with the scaled data, the Logistic Model predicted with 0.659 level of accuracy. In the credit world, I believe this level of accuracy is low and would prefer a model that will predict with a higher level of accuracy.
