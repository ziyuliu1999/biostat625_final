# Group 13 625 final report: Seoul Bike Sharing Demand Prediction

## Introduction

Bike-sharing is widely regarded as an environmental-friendly transportation option and is considered to be one of the remedies for both air pollution and traffic congestion(Zhang et al. 2021). However, increasing the utilization rate of shared bikes remains a challenge. Although many studies have focused on the impact of subjective factors on bike leasing(Kaplan et al. 2015), there has been limited research on objective factors. This study aims to explore these objective factors. Seoul was chosen as the research focus due to its data being highly representative as an international metropolis. Our analysis will encompass the rental patterns and factors influencing bike usage over a one-year period. This study will provide important guidance for the bike-sharing industry, aiding in the effective allocation of bicycles and the attraction of customers.


## Data:

This data set comes from Kaggle: https://www.kaggle.com/datasets/joebeachcapital/seoul-bike-sharing/ data, which contains the number of bikes rented per hour every day in Seoul from 12/01/2017 to 11/30/2018, as well as weather information (Temperature, Humidity, Wind speed, Visibility, Dew point temperature, Solar radiation, Snowfall, Rainfall).

We exclude Solar Radiation and Rainfall, Snowfall variables due to too many zeros. For the rainfall and snowfall, they also closely related with the humidity and temperature. And Dew point temperature and Visibility are removed because of their high-correlation with other covariates, for example temperature.


## Model used:


* Linear Regression

* Poisson Generalized Linear Regression

* Negative Binomial Generalized Linear Regression

* K-Nearest Neighbor

* Random Forest

* Kernel regression with multiple variables

## Tune parameter

Use cross-validation and MSE as the metrics to compare

## Computation challenge:

In our project, we will predict the hour-specific rental counts, which means that we need to fit 24 timesfor each model. Besides that, cross-validation is also a time-consuming process. So, to conquer the timechallenge we will meet, we used the multi-core parallel to complete the project. Firstly, we wrote a democode with the five hyperparameters for RF and KNN from 0 a.m. to 5 a.m. We run the code both withand without using the parallel. The code without using parallel spent 17.18 seconds, and the code used theparallel spent 3.73 seconds. The parallel enhances the speed significantly. So, for the project, we used theparallel to conquer the computational challenge we met. The device we used is 12-core and 18G memory

## Results

We can see that KNN has the best performance when k= 11, the RF has the best performance when the number of trees is 210, and the kernel regression has thebest performance when the number of initial points is 3. So, in the following model comparison, we will usethose optimal values to fit in those models.

After we fitting all those models, the kNN and Kernel regression model has the best performance and we used linear regression to interpret the result.

For more details, you are welcome to read the biostat625_final.pdf in the github.
