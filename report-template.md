# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### GANESH CHOWDHARY PINNAMANENI

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I had to assign the values of the predictior to the "count" column of the submission DataFrame / replaced the existing values in the "count" column with the predicted values.

### What was the top ranked model that performed?
WeightedEnsemble_L3
## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Through EDA I found that "Season" and "Weather" column were presented as int64 data type while they were supposed to be categorical
Extracted year, month, and day as separate features from "datetime" column adding new features to my dataset
Extract new time-based features "hour_of_day" from the "datetime"
Through EDA I found high correlation between "atemp" and "temp" columns and I decided to drop "atemp" to avoid multicollinearity

### How much better did your model preform after adding additional features and why do you think that is?
There was a substantial increase in model perfomance.

This is because the new feature provide additional information or insights about the target variable, leading to better predictions. Also the new feature may be correlated with the target variable, meaning it has a strong relationship or influence on the target.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Little better than the previous model

### If you were given more time with this dataset, where do you think you would spend more time?
Exploratory data analysis and feature creation making notes on how different feature's interact with the model.
and also in Tunning of Hyperparameters
### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

| Model Name    | Hyperparameters Modified  | Kaggle Score |
| ------------- | :-----------------------: | ------------ |
| initial       | DEFAULT                   | 1.81151      |
| add_features  |   DEFAULT                 | 0.51204      |
| hpo           |  NN ,GBM,CAT,RF           | 0.54099      |

### Create a line plot showing the top model score for the three (or more) training runs during the project.
![top_model_performance.png](https://github.com/Ganesh2409/Predict_Bike_Sharing_Demand_Udacity_project1/blob/main/top_model_performance.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.
![kaggle_scores.png](https://github.com/Ganesh2409/Predict_Bike_Sharing_Demand_Udacity_project1/blob/main/kaggle_scores.png)

## Summary
This project equipped me with practical skills in using AutoGluon for tabular prediction tasks, enhanced my understanding of data preparation and analysis, and provided valuable experience in participating in Kaggle competitions and sharing my work with the data science community.
