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
- Prepared dataset for model training using encoded and structured predictors

## Modeling
Two data-driven models were developed and compared: Random Forecast Regressor and Artificial Neural Network (ANN).

### Random Forecast Regressor
- Training–Validation Split: 80% training data (2004–mid 2006) and 20% validation data (mid 2006–end of 2006). Chronological split to maintain time-series order. 
- Finding the best hyperparameters for a Random Forest model: Random Search
- Feature Selection: Random Feature Elimination with Corss-Validations (RFECV)

### ANN
- Training–Validation Split: 80% training data (2004–mid 2006) and 20% validation data (mid 2006–end of 2006). Chronological split to maintain time-series order.
- Processing: Applied StandardScaler to all predictor variables. Scaled target variable sys_load for stable optimization.

## Conclusion
ANN demonstrated superior performance by achieving a lower RMSE and a higher R² on validation data. Owing to its stronger ability to capture complex nonlinear relationships, the ANN model was selected as the final forecasting model and used to generate accurate hourly load predictions for January 2007. 








- 












