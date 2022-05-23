# Alphabet Soup Charity Report

## Overview
The purpose of this analysis is to identify if our neural network model can utilize charity data collected by Alphabet Soup and predict the success of the charity with at least 75% confidence.

## Data Preprocessing
* The target of our model is the binary value “IS_SUCCESSFUL” which was included in the alphabet soup data set. 
* The features of our model included the application type, affiliation, classification, use case, organization category, activity status, income amount, and a more generically defined special considerations column.
* We removed the employer identification number and the name of the company, as these values are strictly arbitrary and unique. Our model is not considering opinion on the name of the charity in our analysis since that data is unavailable.

## Compiling, Training and Evaluating the Model
* For our model, we trained a neural network with 2 hidden layers test with 20, 50 and 100 neurons to allow for more comparisons between the 40+ features in the cleaned data using fewer epochs and determine a range of neurons in each hidden layer and compare how they impacted results.
* We were not able to achieve a target model performance of 75% with this model while including active charities that may be successful in the future, with our closest performance reaching 72.66% accuracy. If we limit to only closed charities our model returns 100% performance, although the majority of the classifications and affiliations are lost. This makes predictions on those more newly used categorizations potentially useless. 
* To increase the model performance, we attempted to remove less impactful columns such as Alphabet Soup’s classification column and by running over more epochs. 

## Summary of Results:
Our deep learning model returned an expected accuracy of 72.66%. While not at our goal of 75%, as a predictive model it can more often than not be utilized to determine the success of a charity. 
Because we had such a large number of features after separating the classifications into their binary subparts, more neurons over a larger number of epochs may be able to reach this goal. However, the returns on each epoch were very small, and accuracy rose very slowly in all tests.
 
For future data collection, age of a charity may also be useful to collect, as most of the charities that were marked as unsuccessful after removal of those that had no contributors and were not started were charities that were still open and could be successful by the end of their campaign. 
