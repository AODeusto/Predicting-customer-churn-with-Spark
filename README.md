# Predicting customer churn with Spark

## Motivation

Fin in this repository an approach to predict customer churn using Spark. The code has been developed in local mode with a subset of the data for efficiency purposes. Although the whole dataset (12GB) could be analyzed on a single machine, spark code allows us to develop an extensible framework scalable to bigger volumes of data to be run within a cluster hosted by a cloud provider.

The analysis has been performed using simulated data from a music provider called **Sparkify**

## Required libraries

- Python 3.6
- PySpark
- Pandas
- Numpy
- Matplotlib

## Files

- Sparkify.ipynb: this is the Spark notebook which contains all the code for this analysis. In order to run it, pyspark, pandas, matplotlib, seaborn and datetime have to be installed
- Sparkify.html: an HTML version of the notebook
- mini_sparkify_event_data.json: this is the log data that we use in this example. It contains information about 226 distinct users, with actions as detailed as giving a thumbs up to a song or changing the settings of the account
- mini_sparkify_event_data.json: subset of the whole dataset to perform the analysis smoothly on a local machine.


## Notes

The analysis was splitted in the following steps:
- **Preprocessing and cleaning** the dataset.
- **EDA (Exploratory Data Analysis)**: Data exploration to get familiar with data
- **Feature engineering**: Turning the oiginal "events" dataset in one ready for MLearning, containing one instance for each user with some developed features and his/her churning label feature.
- **Modelling**: trying three different classifiers to fit and predict based on data. The best resultant model from our approach is the Logistic Regression model, with a fairly good performance in train and test sets, regarding both accuracy and F1 Score.  
- **Features Importance and further improvements**. 

