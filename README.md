# PySpark Flight Delay Prediction

## Machine Learning at Scale @MIDS

#### Authors: <a href="https://www.linkedin.com/in/nicole-liu-2019/">Nicole Liu</a>, <a>Daphne Lin</a>, <a>Jun Park</a>, <a>Tanmay Mahapatra</a>

### Introduction

This is our team's final proejct for MIDS 261 implemented using <a href="https://databricks.com/">Databricks</a> PySpark.

### Project Summary

Our project aims to predict delays two hours prior to the scheduled departure time to classify a flight as delayed or not delayed. We use the airlines dataset sourced from the TransStats data collection provided by the U.S Department of Transportation, the weather dataset from the National Oceanic and Atmospheric Administration repository encompassing data from 2015 to 2019. From these datasets, we use a combination of flight data (e.g. origin airport, scheduled time) and weather data (e.g. temperature, wind speed, humidity), as well as new features around seasonality and average prior delays, to predict flight delays. We built three set of models - Logistic Regression, XGBoost and MLP neural network - for this binary classification task.

The primary metrics we optimized for are F-2 (F-beta where beta = 2) and recall since not correctly predicting a delay has significant financial consequences (e.g., hotel costs, missed connections, pilots over time restrictions). By prioritizing the identification of delayed flights, this study will provide actionable insights for enhancing operational efficiency and reducing costs in the airline industry.

We conducted various experiments on the three models and performed grid search on logistic regression and MLP NN model to find the best parameters. Our best model was logistic regression with 4 newly created features, 10 numerical features and 11 categorical features. It produced f2 of 0.61 and recall of 0.60 on the test set, using the 5 year airline and weather joined data.
