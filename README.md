# Salary Prediction Project (Python) by Lin He
## salarypredictionportfolio

## Purpose
The purpose of the project is to develop and deploy a salary prediction application to help HR or hiring managers to accurately benchmark their compensation strategy, a prerequisite to stay competitive without overpaying too much for talents. Alternatively, a candidate can use this model to initialize salary negotiation. 

## Dataset
Three CSV files available: 1. Training data - features only 2. Training data - target (salary) only 3. Test data - features only.   
In total, there are 1 million rows in each of the csv file.

## Feature list
Years Experience: how many years of experience, ranging from 0 to 24.

Miles From Metropolis: how many miles away from a major city, ranging from 0 to 100.

Job Type: eight different types (CEO, CFO, CTO, VP, Manager, Janitor, Senior and Junior)

Degree: five kinds (Doctoral, Masters, Bachelors, High School and None)

Major: nine kinds (Biology, Business, Chemistry, Computer Science, Engineering, Literature, Math, Physics and None)

Industry: seven kinds (Auto, Education, Finance, Health, Oil, Service and Web)

## Steps
The notebook applies four steps - define, discover, develop and deploy
### 1. Define:
The problem is well defined in this case - predict salary based on available features as accurately as possible.

### 2. Discover:
This step includes loading data, counting, viewing stats and assessing data quality. The data set is of high quality, only 5 of zero salaries out of a million records.
An important element of the step is exploratory data analysis - slicing and dicing data, counting unique values, conducting correlation analysis to build business intuition. None of the findings were surprising other than janitors could make over 150k a year?

### 3. Develop:
Some of the features are correlated, therefore LASSO was chosen as the baseline model. LASSO's penalty function has a tedency of forcing insignificant coefficients to be zero, eliminating highly correlated variables. The baseline model is working well, with mean squared error (mse) of 391 - the goal here is to have mse below 360.
Three other models were developed to compare against LASSO. Decisition tree underperformed LASSO, random forest only slightly outperformed LASSO, and XGBoost (regression) outperformed LASSO by over 8%, reaching the goal of mse below 360.

### 4. Deploy
After selecting the best model - XGBoost, a pipeline was built to streamline the end to end process with predictions and feature importance outputs.

## Summary
This is a fun project with a large set of data available. An MSE of 359 is equivalent to an accuracy score of 76% - quite good considering how limited the feature list is. A couple areas for improvement: first, if the dataset has more features, for example, city name and more job types, it might improve the accuracy. Second, hyperparameter tuning, random search or grid search are good candidates for this.
