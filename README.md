# Electricity-Load-Forecasting-Model
This project focuses on developing an hourly load forecasting model using historical system load and weather data from 2004–2006.

Objective of the project is to predict hourly SYSLoad for January 2007 using data-driven time-series machine-learning Random Forecast and ANN models.

## Approach
- Clean and preprocess the dataset
- Engineer useful temporal and categorical features
- Perform exploratory analysis to understand demand patterns
- Develop and Compare two models:
- Random Forest Regressor
- Artificial Neural Network (ANN)
- Select the best model and generate forecasts for Jan 2007

## Key variables
- SYSLoad → Target variable
- dry_bulb → Dry bulb temperature (°C)
- dew_pnt → Dew point temperature (°C)
- hour → Hour of the day (0–23)
- date → Calendar date
- working_day → Derived (0 = working day, 1 = weekend/holiday)
- day_of_week → Monday=0 … Sunday=6

## Basic cleaning steps
- Converted Date column into proper datetime format
- Renamed columns and standardized names for consistent processing
- Dropped duplicate records from the dataset
- Removed rows containing missing values
- Removed num_date column (redundant) 
- Filtered out the single record where date > 2006-12-31

## Feature Engineering
- Created working_day feature using holiday list
- Derived day_of_week (0 = Monday … 6 = Sunday)
- Generated dummy variables for day-of-week categories
- Prepared dataset for model training using encoded and structured predictors<img width="2060" height="438" alt="image" src="https://github.com/user-attachments/assets/2f980948-836b-4eae-b61d-b7fe33aa739d" />








