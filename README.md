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

The dataset used in this project contains synthetic data created for this project in partnership with Waze. The data consisted of around 15k Waze users who has either churned or retained (continued using the app). The features included information on a user, such as whether they churned or retained, the number of occurrences a user opens the app in the last month, the number of occurrences of driving at least 1 km during the last month, and so on. A few new features were engineered to be used for modeling, they are as follows:

* km_per_driving_day, the mean number of kilometers driven on each driving day in the last month for each user.
* percent_sessions_in_last_month, the percentage of each user's total sessions that were logged in their last month of use.
* professional_driver, a binary feature that is 1 for users who had 60 or more drives and drove on 15+ days in the last month.
* total_sessions_per_day, the mean number of sessions per day since onboarding.
* km_per_hour, the mean kilometers per hour driven in the last month.
* km_per_drive, the mean number of kilometers per drive made in the last month for each user.
* percent_of_sessions_to_favorite, the percentage of total sessions that were used to navigate to one on the users' favorite places.

## Modeling and Evaluation

An XGBoost model comprising 300 decision trees was used to determine feature importance in who would churn or not. The below plot shows that the mean number of kilometers driven on each driving day in the last month, the number of days since the user signed up for the app, and the percentage of each user's total sessions that were logged in their last month of use were the Top 3 most important factors in determining a user who will churn from a user who will retain. The overall model performed with 81.1% accuracy, 42.4% precision, and 18.1% recall. 
![Waze XGBoost Feature Importance Plot](https://github.com/chungchenran2/Waze_User_Churn_Prediction_Project/blob/main/Images/Waze_XGBoost_Feature_Importance_Plot.png)

## Conclusion

