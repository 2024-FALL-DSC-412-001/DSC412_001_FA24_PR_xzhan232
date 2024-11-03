# DSC412-project

This repository contains any code and files for the DSC412 project.

The project proposal and plan are in DSC412_001_FA24_PR_sfeng9.pdf

# Demand Forecasting with Big Data

## Project Overview
This project focuses on creating a robust demand forecasting model for a retail store chain. Using five years of sales data, which includes information on 10 different stores and 50 different products, we aim to predict future sales and provide insights that can aid in inventory optimization, cost reduction, and improved customer satisfaction.

The project uses various techniques and models for time series analysis, feature engineering, and data visualization to develop accurate demand forecasts.

## Table of Contents
- [DSC412-project](#dsc412-project)
- [Demand Forecasting with Big Data](#demand-forecasting-with-big-data)
  - [Project Overview](#project-overview)
  - [Table of Contents](#table-of-contents)
  - [Dataset](#dataset)
  - [Project Goals](#project-goals)
  - [Data Processing](#data-processing)
  - [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Modeling Approach](#modeling-approach)
  - [Results and Evaluation](#results-and-evaluation)
- [Getting Started Instruction](#getting-started-instruction)
- [Citation:](#citation)

## Dataset
The dataset covers sales data for 10 stores and 50 products over five years (2013-2017). Key columns include:
- `date`: Date of sales record.
- `store`: Unique identifier for each store.
- `item`: Unique identifier for each item.
- `sales`: Quantity of items sold on a given date.
  
## Project Goals
- Develop a 3-month demand forecasting model for each product across all stores.
- Aggregate the data weekly to build a demand forecasting model specifically for 2017.
- Provide actionable insights into sales trends, seasonal patterns, and store-product performance.

## Data Processing
- **Loading and Merging Data**: Combined training and testing datasets.
- **Feature Engineering**: Created new features based on date (e.g., day of the week, month) to capture seasonality and store-specific trends.
- **Encoding**: Encoded categorical variables (e.g., store, item) for model compatibility.

## Exploratory Data Analysis
Various exploratory data analysis (EDA) techniques were applied to understand the dataset and identify key patterns:
- **Sales Over Time**: Visualized sales trends to capture seasonality and other patterns.
- **Correlation Analysis**: Examined correlations between variables, using heatmaps for visualization.
- **Pairplot**: Generated scatterplots to analyze relationships between store, item, and sales.
- **Statistics by Store-Product Breakdown**: Aggregated sales statistics for each store-product pair to understand average sales, variability, and performance.

## Modeling Approach
The project implemented several time series forecasting models:
1. **LightGBM**: A gradient boosting model for predicting sales based on engineered features.
2. **Exponential Smoothing Models**: Single, Double, and Triple Exponential Smoothing models to capture trends and seasonality.
3. **ARIMA**: A classic time series model for sales prediction, particularly for cases with trend and seasonality.
4. **SARIMA**: A seasonal version of ARIMA, specifically tuned for 2017 demand forecasting.

## Results and Evaluation
Each model was evaluated based on forecasting accuracy by comparing predicted and actual sales values for 2017. The models were fine-tuned, and performance metrics were compared to determine the best approach for different scenarios.

# Getting Started Instruction

You can run your tests in terminal by doing the following:

Make sure your terminal is in this directory. You can confirm that is true by typing `pwd` in terminal.

Create a virtual environment with

`python -m venv ./.venv`

Then activate it in terminal:

Windows: `.\.venv\Scripts\activate`

Mac: `source ./.venv/bin/activate`

Linux: `source ./.venv/bin/activate`

You should see `.venv` appear in the terminal on the left side of teh command line.

Then run `pip install -r requirements.txt` in terminal

# Citation: 

Kaggle. (n.d.). Demand forecasting - kernels only. from https://www.kaggle.com/competitions/demand-forecasting-kernels-only
