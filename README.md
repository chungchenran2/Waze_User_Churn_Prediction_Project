# Waze User Churn Prediction Project

## Overview

The goal of this project was to create a logistic regression, random forest, and XGBoost model to predict whether a user of the Waze app will churn or not. Churn quantifies the number of users who have uninstalled the Waze app or stopped using the app. This project utilized a dataset of Waze users who are either retained or churned. The random forest model performed with 81.7% accuracy, 44.5% precision, and 12.0% recall in determining which Waze users will churn. The XGBoost model performed with 81.2% accuracy, 42.3% precision, and 16.2% recall in determining which Waze users will churn. The XGBoost model was chosen as the champion model with the following performance on the test dataset: 81.1% accuracy, 42.4% precision, and 18.1% recall. Based on the XGBoost model, the driven distance per hour, number of days since onboarding, and percentage of each user's total sessions logged in their last month of use were most influential in determining which user will churn.

## Business Understanding

This project is part of a larger effort at Waze to increase growth. Typically, high retention rates indicate satisfied users who repeatedly use the Waze app over time. Developing a churn prediction model will help prevent churn, improve user retention, and grow Waze’s business. An accurate model can also help identify specific factors that contribute to churn and answer questions such as:

* Who are the users most likely to churn?
* Why do users churn?
* When do users churn?

For example, if Waze can identify a segment of users who are at high risk of churning, Waze can proactively engage these users with special offers to try and retain them. Otherwise, Waze may lose these users without knowing why.

The insights of this project will help Waze leadership optimize the company’s retention strategy, enhance user experience, and make data-driven decisions about product development.

## Data Understanding


## Modeling and Evaluation


## Conclusion

