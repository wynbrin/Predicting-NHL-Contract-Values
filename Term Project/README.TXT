Predicting NHL Player Contract Value

Program Description: 

The goal of this project is to ingest National Hockey League (NHL) player contract & performance data to train predictive models that can be effective in predicting the overall value of a player given their performance.

The program pulls contract and performance data from PuckPedia.com and creates a merged data table containing the following fields: games_played, toi, gf_percentage, xgf_percentage, g60, p60, and total_contract_value. Total_contract_value is identified as the dependent variable to be predicted while the other fields are identified as the dependent variables to inform the predictive models.

Four different continuous regression models were trained to achieve this goal: Linear Regression, K Nearest Neighbors Regression, Decision Tree Regressor, and Random Forest Regressor. Prior to model training, the test data was normalized and Principle Component Analysis was performed for feature engineering. 




Challenges:
Sample Size was smaller than ideal with only about 4,500 records due to information availability constraints with PuckPedia.

A summary of the required scripts is provided below:

1. NHL Contract Estimator.ipynb

A. Purpose
To ingest & merge contract and performance datasets, pre-process the training set, and build/optimize predictive models

B. Required directory locations:
    /Data

C. Required Packages:
from sklearn.pipeline import Pipeline
from sklearn.model_selection import train_test_split
from sklearn.decomposition import PCA
from sklearn.linear_model import LinearRegression
from sklearn.neighbors import KNeighborsRegressor
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_squared_error, mean_absolute_error , r2_score
from sklearn.preprocessing import StandardScaler
Matplotlib
Numpy
Pandas

2. exploratory analysis

A. Purpose
To explore the impact of each individual feature used for model training & optimize model performance

B. Required directory locations:
    /Data

C. Required Packages:
import pandas as pd
import scipy.stats
import numpy as np
import matplotlib.pyplot as plt
Import os
from sklearn.decomposition import PCA
from sklearn.ensemble import RandomForestRegressor
from sklearn.linear_model import LinearRegression
from sklearn.neighbors import KNeighborsRegressor
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import RandomForestRegressor
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error, mean_absolute_error , r2_score
