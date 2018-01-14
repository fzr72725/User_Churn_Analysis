# User Churn Analysis
User retention is always one of the most important problem a customer services
organization faces. This project is aiming to model the trend of users' churn,
and discover importance features that indicates a user's possibility of churning.
The dataset consist users who signed up for a company's service in January 2014. The data was pulled on July 1, 2014; a user is considered retained if they were “active” (i.e. took a trip) in the preceding 30 days (from the day the data was pulled). In other words, a
user is "active" if they have taken a trip since June 1, 2014.

## Motivation
Because the end goal is to understand **what factors are
the best predictors for retention**, and offer suggestions to operationalize
those insights to help Company X, the focus of the project is not only to build a
predictive model that minimizes error, but also a model that is interpretable.

## Data Set
### General Description

|Variable  |  Definition  |
| --- | --- |
|city| city this user signed up in phone: primary device for this user|
|signup_date| date of account registration; in the form `YYYYMMDD`|
|last_trip_date| the last time this user completed a trip; in the form `YYYYMMDD`|
|avg_dist| the average distance (in miles) per trip taken in the first 30 days after signup|
|avg_rating_by_driver| the rider’s average rating over all of their trips|
|avg_rating_of_driver| the rider’s average rating of their drivers over all of their trips|
|surge_pct| the percent of trips taken with surge multiplier > 1|
|avg_surge| The average surge multiplier over all of this user’s trips|
|trips_in_first_30_days| the number of trips this user took in the first 30 days after signing up|
|luxury_car_user| TRUE if the user took a luxury car in their first 30 days; FALSE otherwise|
|weekday_pct| the percent of the user’s trips occurring during a weekday|


## Process
### Pre-Processing
- Build pipeline for upcoming modeling
- Generate data label(target) based on the 'churn' definition
- Feature selection

### Model Development
- LogisticRegression
- Random Forest
- GridSearch to tune hyperparameters
- Partial Dependence Plots
