# BoomBikes_bike sharing_Case_Study
We need to build a multiple linear regression model to predict bike demand for BoomBikes, a bike-sharing service facing revenue challenges due to the Covid-19 pandemic. The company wants to understand which factors significantly influence bike demand and how well these factors explain the variations in demand. You will use a dataset containing various factors affecting bike usage across the American market. The model will help BoomBikes develop a business strategy to better meet future demand and enhance their market position post-pandemic. Your final submission should be a Jupyter notebook showcasing your model and findings.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
- Provide general information about your project here.
  Background of the Project
   BoomBikes, a bike-sharing company in the U.S., has faced significant revenue declines due to the COVID-19 pandemic. To adapt to the post-pandemic market and recover their financial stability, the company aims to better understand bike demand patterns once the lockdowns are lifted. They have gathered a comprehensive dataset on daily bike demands and various influencing factors, such as weather conditions and user behavior, to analyze these patterns.
   The objective is to develop a multiple linear regression model that predicts bike demand based on the collected data. This model will help BoomBikes identify the key variables affecting demand and assess how well these variables can explain variations in bike usage. By doing so, the company aims to optimize their business strategy, improve service offerings, and better align with customer expectations in a recovering market.
  Business Problem
   The primary business problem the project addresses is the need to forecast bike demand accurately in the post-pandemic scenario. Specifically, BoomBikes wants to:Identify Significant Variables: Determine which factors (e.g., weather conditions, day of the week, etc.) are most influential in predicting bike demand. Evaluate Model Effectiveness: Assess how well these factors explain variations in demand to gauge the model’s reliability.
   Optimize Business Strategy: Use the insights from the model to adjust operational strategies, enhance customer satisfaction, and potentially increase revenues.
   This analysis will provide BoomBikes with actionable insights into customer demand patterns, allowing them to tailor their services and strategic planning to better meet market needs and stay competitive.
  Dataset used 
   day.csv

## Conclusions
 1. We can conclude that cnt is highly dependent on the key varaibles like season_3, season_2, weathersit_3, yr and season_4 etc. coefficient of each X values with cnt is provided as below:
   yr              0.248308
   holiday        -0.082845
   weekday         0.049550
   windspeed      -0.178046
   season_2        0.255771
   season_3        0.313733
   season_4        0.228725
   weathersit_2   -0.088869
   weathersit_3   -0.293951

    We can see that the equation of our best fitted line is:
    cnt = 0.248308  \times  yr - 0.082845  \times  holiday + 0.049550 \times weekday - 0.178046 \times windspeed + 0.255771 \times season_2 + 0.313733 \times season_3 + 0.228725 \times season_4 - 0.088869 \times weathersit_2 - 0.293951 \times weathersit_3 + 0.259109
2. r2 score value bwtween y_test and y_pred is 0.7421.
3. Error term is normally distributed. 


## Technologies Used
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import MinMaxScaler
import statsmodels.api as sm

# Check for the VIF values of the feature variables. 
Features	VIF
windspeed	3.28
workingday	2.79
weekday	    2.76
yr	        1.93
season_2	1.74
season_3	1.71
season_4	1.64
weathersit_2	1.51
weathersit_3	1.08
holiday	    1.06


## Contact
Created by Pavan Andagi

<!-- ## License -->
[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}