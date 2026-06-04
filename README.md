# Mortgage Loan Origination Analysis and Prediction

## Overview

This project analyzes HMDA mortgage loan application data. The goal is to prepare and explore the data, analyze loan origination patterns, build a simple interactive dashboard, and train classification models to predict whether a loan application is successfully originated.

The project consists of one Jupyter Notebook file

* `Mortgage loan origination prediction.ipynb`

that is split into three parts:

* `Part 1 (ETL)`: data loading, cleaning, target creation, and preparation for analysis
* `Part 2 (EDA)`: target distribution, numeric/categorical analysis, state-level patterns, disparity analysis, feature selection, correlation analysis, and Dash dashboard
* `Part 3 (Modeling)`: classification models, threshold tuning, baseline comparison, and final evaluation

## Data

The project uses publicly available Home Mortgage Disclosure Act (HMDA) mortgage application data from the Consumer Financial Protection Bureau (CFPB) available at https://www.consumerfinance.gov/data-research/hmda/historic-data/¶ .

The binary target variable is `loan_success`:

* `1`: loan originated
* `0`: loan not originated

## Methods

Main steps:

* Loaded and cleaned HMDA mortgage application data
* Created a binary loan origination target
* Prepared categorical and numerical variables for analysis
* Explored target distribution and class imbalance
* Analyzed numeric distributions by loan success
* Compared loan success rates across states and applicant groups
* Built a simple interactive Plotly Dash dashboard
* Applied KBest feature selection
* Built preprocessing pipelines for categorical and numeric features
* Trained classification models using GridSearchCV
* Tuned classification thresholds on a validation set
* Compared models against a naive baseline
* Evaluated models using ROC-AUC, PR-AUC, log-loss, accuracy, precision, recall, and F1-score

## Key Notes

The disparity analysis is descriptive only. Differences in loan success rates across applicant groups should not be interpreted as proof of discrimination, because the analysis does not control for all relevant factors such as income, loan amount, geography, loan purpose, and property characteristics.

The dashboard is intended as a simple interactive exploration tool.

## Tools

Python, pandas, NumPy, matplotlib, seaborn, Dash, Plotly, scikit-learn, XGBoost, Jupyter Notebook.

## Folder structure

* Data
  * Processed data
  * Raw data
* Figures
* Notebooks
  * Mortgage loan origination.ipynb
* requirements.txt

## How to Run

Install the required packages:

    pip install -r requirements.txt

The notebook can be accessed via Jupyter Notebook.

    Mortgage loan origination.ipynb

To run the Dash dashboard locally, execute the dashboard cell or script and open:

    http://127.0.0.1:8051/

## Status

Part 1 and Part 2 are completed. Part 3 is still in progress.
