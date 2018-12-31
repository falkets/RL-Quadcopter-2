# Udacity's Capstone Project Proposal

Solving the Kaggle's challenge: New York City Taxi Trip Duration

## Domain Background

The challenge is to build and properly train a model that is capable of predicting the total duration of taxi trip in New York City. The model will be trained with a dataset provided by the NYC Taxi and Limousine Commission, the dataset includes pickup and drop-off time, pickup and drop-off coordinates and number of passengers among other variables.

## Problem Statement

The competition dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC). The data was sampled and cleaned for the purposes of the challenge. Based on each trip attributes, the goal is to predict the duration of each trip in the test set, also provided in the Challenge.

## Datasets and Inputs

Two datasets are provided by the Challenge, the **Train** dataset with 1,458,644 trip records and the **Test** dataset with 625,134 trip records. Both datasets are in CSV format and were originally published by the NYC Taxi and Limousine Commission (TLC).

### Data Fields

Regarding the data fileds, both datasets are constituted as follows:

* id - a unique identifier for each trip;
* vendor_id - a code indicating the provider associated with the trip record;
* pickup_datetime - date and time when the meter was engaged;
* dropoff_datetime - date and time when the meter was disengaged;
* passenger_count - the number of passengers in the vehicle (driver entered value);
* pickup_longitude - the longitude where the meter was engaged;
* pickup_latitude - the latitude where the meter was engaged;
* dropoff_longitude - the longitude where the meter was disengaged;
* dropoff_latitude - the latitude where the meter was disengaged;
* store_and_fwd_flag - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a connection to the server - Y=store and forward; N=not a store and forward trip;
* trip_duration - duration of the trip in seconds.

### The Target Variable

The challenge objective is to find values for trip_duration for each trip from the **Test** dataset starting from all the information known from the **Train** dataset.

In more technical words as the origin data is already cleaned and prepared for processing, the first step to be done is the Feature Engineering, i.e. to make the first preparation of each field, select the most relevant ones. After this step, starts the data modeling phase and the model evaluation and fine tunning.

## Solution Statement

The challenge will be solved using supervised learning methods, since the target variable is labeled in the **train** dataset. The first approach for the problem will be using ensemble regression model from scikit-learn to find the trip duration for the **test** dataset

## Benchmark Model

As the capstone project was taken from a Kaggle's challenge, the obvious choice for the benchmark is the winner team, called **L2F** who achieved the score of 0.28976. However, given they're probably a well experienced team, a more conservative benchmark would be to achieve a score bellow 0.5, i.e. be among the best 790 from the 1257 submissions, using the evaluation metric bellow.

## Evaluation Metrics

The same evalutation metric used to rank the competitors in the Kaggle competition will be used here, the metric will be the Root Mean Square Logarithmic Error (RMSLE), given by:

Where:

* ϵ is the RMSLE value (score);
* n is the total number of observations in the (public/private) data set;
* pi is your prediction of trip duration;
* ai is the actual trip duration for i;
* log(x) is the natural logarithm of x.

## Project Design

The data was provided already cleaned, then the first step is to do the data exploration and Feature Engineering, i.e. analyze all the fields provided, check and understand its distribution, transform all the needed feature values to a better representation and select the best features. The next step is to train and evaluate the Models using differente techniques and different parameters for each technique, comparing the performances with the evaluation metrics.