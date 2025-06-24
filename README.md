#Avocado Retail Price Forecasting

This project aims to predict the **Average Retail Price of Avocados** using historical sales data. It applies data preprocessing, feature engineering, and machine learning models to identify patterns and optimize pricing strategy.


##  Dataset Overview

- Source: -[Hass Avocado Board (via Kaggle)](https://www.kaggle.com/datasets/neuromusic/avocado-prices)  # datset_source
- Features Include:
  - 'Total Volume', 'Small Bags', 'Large Bags', 'XLarge Bags', individual PLU codes (4046', '4225', '4770')
  - 'type': organic/conventional
  - 'region'
  - 'Date'

###  Step 1: Data Cleaning
- Removed irrelevant columns (e.g., 'S.No', 'XLarge Bags')
- Converted 'Date' to datetime format
- Extracted 'year' and 'month' as features

### Step 2: Feature Engineering
- Label encoded 'type'
- Frequency encoded 'region'
- Created final feature set with numerical columns

###  Step 3: Model Training
- Models used:
  - 'LinearRegression'
  - 'RandomForestRegressor'
  - Split data: 80% train, 20% test

### Step 4: Evaluation
  - Metrics used:
  - MAE (Mean Absolute Error)
  - RMSE (Root Mean Squared Error)

###  Step 5: Feature Importance
- Identified the most influential features using the Random Forest model
- Visualized using bar plots
- Key insight: 'type_encoded' was among the most important features

##  Outputs
-  'random_forest_model.pkl': Saved trained model
-  'feature_names.pkl': Feature list used for training

##  Future Scope
- Hyperparameter tuning
- Add time-series models (e.g., ARIMA, LSTM)
- Deploy as a web app for interactive forecasting


## How to run :
 -clone the repo 
 -create a virtual environment 
 -install dependencies > requirements.txt
 -run the notebook































































































































