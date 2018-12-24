
# Udacity's Capstone Project Proposal
Solving the Kaggle's challenge: New York City Taxi Trip Duration}
   
## Domain Background

The challenge is to build and properly train a model that is capable of predicting the total duration of taxi trip in New York city starting from a dataset provided by the NYC Taxi and Limousine Commission, the dataset includes pickup and drop-off time, pickup and drop-off coordinates and number of passengers among other variables.

## Problem Statement

The competition dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC). The data was sampled and cleaned for the purposes of the challenge. 
Based on each trip attributes, the goal is to predict the duration of each trip in the test set, also provided in the Challenge.

## Datasets and Inputs

Two datasets are provided by the Challenge, the train dataset 1458644 trip records and the test dataset with 625134 trip records. Both datasets were provided with  the data was originally published by the NYC Taxi and Limousine Commission (TLC).

The data sets have the following data  fields:

* id - a unique identifier for each trip
* vendor_id - a code indicating the provider associated with the trip record
* pickup_datetime - date and time when the meter was engaged
* dropoff_datetime - date and time when the meter was disengaged
* passenger_count - the number of passengers in the vehicle (driver entered value)
* pickup_longitude - the longitude where the meter was engaged
* pickup_latitude - the latitude where the meter was engaged
* dropoff_longitude - the longitude where the meter was disengaged
* dropoff_latitude - the latitude where the meter was disengaged
* store_and_fwd_flag - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a connection to the server - Y=store and forward; N=not a store and forward trip
* trip_duration - duration of the trip in seconds

## Solution Statement


## Benchmark Model


## Evaluation Metrics


## Project Design


## Presentation


\end{document}
% \href{https://www.kaggle.com/c/nyc-taxi-trip-duration} {New York City Taxi Trip Duration}}


# Deep RL Quadcopter Controller

*Teach a Quadcopter How to Fly!*

In this project, you will design an agent to fly a quadcopter, and then train it using a reinforcement learning algorithm of your choice! 

## Project Instructions

1. Clone the repository and navigate to the downloaded folder.

```
git clone https://github.com/udacity/RL-Quadcopter-2.git
cd RL-Quadcopter-2
```

2. Create and activate a new environment.

```
conda create -n quadcop python=3.6 matplotlib numpy pandas
source activate quadcop
```

3. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `quadcop` environment. 
```
python -m ipykernel install --user --name quadcop --display-name "quadcop"
```

4. Open the notebook.
```
jupyter notebook Quadcopter_Project.ipynb
```

5. Before running code, change the kernel to match the `quadcop` environment by using the drop-down menu (**Kernel > Change kernel > quadcop**). Then, follow the instructions in the notebook.

6. You will likely need to install more pip packages to complete this project.  Please curate the list of packages needed to run your project in the `requirements.txt` file in the repository.