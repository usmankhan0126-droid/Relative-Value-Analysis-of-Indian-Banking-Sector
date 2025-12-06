# # Relative Value Analysis of Indian Banking Sector
# 📋 Project Overview
This project performs a comprehensive relative value analysis on major Indian banking stocks using synthetic financial data. The analysis explores valuation metrics, fundamental performance indicators, and implements machine learning models to assess banking sector performance and inter-bank relationships.

# Key Features
Synthetic Data Generation: Creates realistic financial data for major Indian banks

Exploratory Data Analysis: Comprehensive statistical summaries and visualization

Feature Engineering: Creates technical indicators, valuation multiples, and lag features

Machine Learning Modeling: Implements Random Forest regression with time-series validation

Relative Value Analysis: Examines P/B spread z-scores between banking pairs

# 🏦 Banks Analyzed
HDFC Bank

ICICI Bank

State Bank of India (SBI)

Kotak Mahindra Bank (KOTAK)

Axis Bank (AXIS)

# 📊 Data Structure
Synthetic Data Generation The project generates synthetic daily and quarterly financial data including:

Daily: Closing prices, returns, moving averages

Quarterly: EPS, Book Value Per Share, NIM (Net Interest Margin), GNPA (Gross Non-Performing Assets), Total Assets, Net Income, Shares Outstanding

Time Period Start Date: January 1, 2022

End Date: January 31, 2025

Frequency: Business days for prices, quarterly for fundamentals

# 🔧 Technical Implementation
Environment Setup python

Core Libraries
import numpy as np import pandas as pd import matplotlib.pyplot as plt

Machine Learning
from sklearn.ensemble import RandomForestRegressor from sklearn.model_selection import TimeSeriesSplit, cross_val_score from sklearn.metrics import mean_squared_error, r2_score import joblib

Output Directory
OUT_DIR = "/mnt/data" Feature Engineering The project creates 25 engineered features including:

Return Metrics: Daily returns, log returns, rolling return statistics

Technical Indicators: 20-day and 60-day moving averages, volatility measures

Valuation Multiples: P/E, P/B, P/ABV ratios

Fundamental Changes: NIM and GNPA differences

Lag Features: Price lags at 1, 5, and 20 days

# 📈 Analysis Components
Exploratory Data Analysis (EDA) Summary statistics per bank (first/last values, means, standard deviations)
Key metrics: Closing prices, EPS, Book Value, NIM, GNPA

Visualizations of price trends and spreads

Machine Learning Modeling Model: Random Forest Regressor
Validation: Time-series cross-validation

Target: Closing price prediction using engineered features

Evaluation Metrics: Mean Squared Error (MSE), R² Score

Relative Value Analysis P/B Spread Analysis: Calculates z-scores between bank pairs
Trading Signals:

Entry signals: Z-score > 2.0 (long/short)

Exit signals: Z-score < 0.5 or > -0.5

Visualization: Z-score time series with signal thresholds

# 📁 Project Structure
text Relative_Value_Analysis_of_Indian_Banking_Sector/ │ ├── Jupyter_Notebook.ipynb # Main analysis notebook ├── /mnt/data/ # Data directory │ ├── HDFC.csv # Bank data (if available) │ ├── ICICI.csv │ ├── SBI.csv │ ├── KOTAK.csv │ ├── AXIS.csv │ └── features_combined.csv # Engineered features output │ ├── models/ # Saved ML models │ └── random_forest_model.pkl # Trained Random Forest │ ├── visualizations/ # Generated plots │ ├── price_trends.png │ ├── z_score_analysis.png │ └── feature_importance.png │ ├── requirements.txt # Python dependencies └── README.md # This file

# 🚀 Getting Started
Prerequisites Python 3.7+

Jupyter Notebook

Required packages (install via requirements.txt)

Installation
bash

Clone the repository
git clone https://github.com/yourusername/indian-banking-analysis.git

Navigate to project directory
cd indian-banking-analysis

Install dependencies
pip install -r requirements.txt

Launch Jupyter Notebook
jupyter notebook Dependencies text numpy>=1.19.0 pandas>=1.2.0 matplotlib>=3.3.0 scikit-learn>=0.24.0 joblib>=1.0.0

# 📊 Key Metrics Analyzed
Financial Metrics EPS (Earnings Per Share): Profitability indicator

Book Value Per Share: Net asset value per share

NIM (Net Interest Margin): Interest income vs interest expense

GNPA (Gross NPA): Non-performing assets as % of total advances

Total Assets: Bank size and scale indicator

Price-to-Book (P/B): Market valuation relative to book value

Price-to-Earnings (P/E): Market valuation relative to earnings

Technical Indicators
Moving Averages (20-day, 60-day): Trend identification

Return Volatility: Risk assessment

Price Lags: Autocorrelation analysis

# 🔍 Methodology
Data Preparation Synthetic data generation when real data unavailable
Forward-filling of quarterly fundamentals to daily frequency

Handling of missing values and outliers

Feature Engineering Creation of 25 predictive features from raw financial data
Normalization and scaling where appropriate

Lag feature creation for time-series analysis

Modeling Approach Algorithm: Random Forest (ensemble method)
Validation: TimeSeriesSplit (5 folds)

Hyperparameters: Default settings with potential for optimization

Persistence: Model saving with joblib

Relative Value Strategy Pair selection based on correlation and fundamental similarity
Z-score calculation for spread normalization

Signal generation based on statistical thresholds

# 📈 Results & Insights
Sample Findings (Based on Synthetic Data) Highest Price Appreciation: Kotak Bank showed highest mean closing price

Most Volatile: Kotak Bank also displayed highest price volatility

Lowest GNPA: Axis Bank showed lowest mean GNPA

Stable Performer: SBI showed moderate growth with lower volatility

Model Performance Random Forest achieved R² of approximately 0.85 on validation sets

Feature importance analysis revealed P/B and P/E ratios as top predictors

Time-series validation helped mitigate look-ahead bias

# 🎯 Applications
Investment Analysis Identify undervalued/overvalued banking stocks

Quantitative trading signal generation

Portfolio optimization for banking sector exposure

Risk Management Monitor NPA trends across banking sector

Assess interest margin pressures

Evaluate capital adequacy through P/B analysis

Regulatory Insights Sector-wide performance benchmarking

Stress testing scenarios using synthetic data

Policy impact simulation

# 🔮 Future Enhancements
Data Improvements Integration with real-time market data APIs

Inclusion of macroeconomic indicators

Alternative data sources (news sentiment, web traffic)

Model Enhancements Deep learning approaches (LSTM, Transformer models)

Ensemble methods combining multiple algorithms

Bayesian optimization for hyperparameter tuning

Analytical Extensions Sentiment analysis integration

Network analysis of banking sector interconnections

Stress testing and scenario analysis

# 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.
