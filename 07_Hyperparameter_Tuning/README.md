# Hyperparameter Tuning
#### We use grid search and apply 5-fold cross validation on the training dataset for hyperparameter tuning. 

## 1. Optimal Hyperparameters for Random Forest Model
#### The values in column Values are the optimal parameters, and the values in column Range are the range of numbers we grid search through
| 4 Hyper Parameters  | Values             | Range              |
|---------------------|--------------------|--------------------|
| n_estimators        | 1000               | 100 - 1500         |
| max_depth           | 60                 | 60 - 100           |
| min_samples_split   | 14                 | 2 - 14             |
| min_samples_leaf     | 9                  | 1 - 10             |


## 2. Optimal Hyperparameters for XGBoost Model
#### The values in column Values are the optimal parameters, and the values in column Range are the range of numbers we grid search through <br> (Since the XGBoost Classifier has some issue when applied with the gridsearch() and RandomUnderSampler() function, we apply self-written algorithm to conduct the gridsearch rather than using the sklearn gridsearch() function.)

| 8 Hyper Parameters  | Values             | Range              |
|---------------------|--------------------|--------------------|
| eta                 | 0.15               | 0.05 - 0.50        |
| max_depth           | 6                  | 3 - 10             |
| min_child_weight    | 4                  | 1 - 10             |
| gamma               | 1.6                | 0 - 1.9            |
| colsample_bytree    | 0.9                | 0.1 - 0.9          |
| subsample           | 0.6                | 0.1 - 0.9          |
| reg_alpha           | 0.2                | 0.1 - 1.0          |
| reg_lambda          | 1                  | 0.1 - 1.0          |
