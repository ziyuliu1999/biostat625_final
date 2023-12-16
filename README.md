# Group 13 625 final report: Seoul Bike Sharing Demand Prediction

## Introduction

Bike-sharing is widely regarded as an environmental-friendly transportation option and is considered to be one of the remedies for both air pollution and traffic congestion(Zhang et al. 2021). However, increasing the utilization rate of shared bikes remains a challenge. Although many studies have focused on the impact of subjective factors on bike leasing(Kaplan et al. 2015), there has been limited research on objective factors. This study aims to explore these objective factors. Seoul was chosen as the research focus due to its data being highly representative as an international metropolis. Our analysis will encompass the rental patterns and factors influencing bike usage over a one-year period. This study will provide important guidance for the bike-sharing industry, aiding in the effective allocation of bicycles and the attraction of customers.


## Data:

This data set comes from Kaggle: https://www.kaggle.com/datasets/joebeachcapital/seoul-bike-sharing/ data, which contains the number of bikes rented per hour every day in Seoul from 12/01/2017 to 11/30/2018, as well as weather information (Temperature, Humidity, Wind speed, Visibility, Dew point temperature, Solar radiation, Snowfall, Rainfall).

We exclude Solar Radiation and Rainfall, Snowfall variables due to too many zeros. For the rainfall and snowfall, they also closely related with the humidity and temperature. And Dew point temperature and Visibility are removed because of their high-correlation with other covariates, for example temperature.


## Model used:


*item Linear Regression
*item Poisson Generalized Linear Regression
*item Negative Binomial Generalized Linear Regression
*item K-Nearest Neighbor
*item Random Forest
*item Kernel regression with multiple variables



