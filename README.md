### salarypredictionportfolio
Salary Prediction Project (Python)

# Purpose
The purpose of the project is to develop and deploy a salary prediction application to help HR or hiring managers to accurately benchmark their compensation strategy, a prerequisite to stay competitive without overpaying too much for talents. 

# Dataset
Three CSV files available: 1. Training data - features only 2. Training data - 3. Target variable - Salary. There are 1 million observation and 9 features in total.

Features
Years Experience: How many years of experience

Job Type: The position held (CEO, CFO, CTO, Vice President, Manager, Janitor, and senior or junior position)

College Degree: Doctoral, Masters, Bachelors, High School, or None

College Major: Biology, Business, Chemistry, Computer Science, Engineering, Literature, Math, Physics, or None

Industry: Auto, Education, Finance, Health, Oil, Service, or Web

Miles From Metropolis: How many miles away from a major city

Background
This notebook demonstrates the entire data science process of building a predictive model that can hypothetically used by HR to estimate perspective employees' compensation. The processes involving defining the problem, preprocessing data, EDA, developing model, and deploying into production have been divided into main sections. Salary range tends to vary, depending on many factors such as experiences, education, previous job title, etc. This predictive analysis aims to build a scalable and deployable model to predict salary. Here are the breakdown of my project.

Data Cleaning and Preprocessing, checking for collearity, outliers, missing data.

Exploratory data analysis to examine the distribution of the target variable and its correlation with categorical and numerical features.

Baseline Model and Compared Models built using linear regression, random forest, and gradient boosting.

Models tuning using parameters such as n_estimators, learning rate, tree depth,etc

Cross validation and select the best model with the lowest Mean Square Error (MSE).

Linear Regression : 380
Random Forest: 411
Gradient Boosting: 358 Gradient Boosting turns out to have the lowest MSE on the Cross Validation. Upon predicting on the test dataset, it achieves 358 on the final model.
Feature importance data visualization

Deploy and save the final model into production using Pipeline.
