# PM2.5 Concentration Prediction Project README

## Overview

This project focuses on predicting PM2.5 concentrations in the Sonia Vihar region of Delhi using machine learning techniques. The goal is to develop an accurate model that can forecast PM2.5 levels based on various environmental parameters and meteorological data.

## Dataset

The daily averaged PM2.5 concentration data and meteorological data were collected from the Sonia Vihar air monitoring station in the North-Eastern zone of Delhi. The dataset spans from January 2019 to May 2023 and includes the following parameters:

- PM2.5: Particulate Matter of size 2.5 μm or less.
- PM10: Particulate Matter of size 10 μm or less.
- NO: Nitric Oxide in μg/m³.
- NO2: Nitrogen Dioxide in μg/m³.
- NOx: Nitrogen Oxides, a mixture of NO and NO2 in ppb.
- SO2: Sulphur Dioxide in μg/m³.
- AT: Atmospheric Temperature in degree Celsius.
- RH: Relative Humidity in percentage.
- WS: Wind Speed in meters per second.
- RF: Rainfall in mm.

## Analysis Workflow

1. **Data Cleaning and Preprocessing:**
   - Removed time elements and handled missing observations.
   - Converted data to CSV format for analysis.

2. **Feature Selection:**
   - Identified key features influencing PM2.5 concentrations.

3. **Train-Test Split:**
   - Divided the dataset into training and testing sets, with a test size of 20%.

4. **Hyperparameter Tuning:**
   - Found the best hyperparameters for the Random Forest Regression model.

   Best Hyperparameters: {'max_depth': 6, 'max_features': 'auto', 'min_samples_leaf': 1, 'min_samples_split': 13, 'n_estimators': 107}

5. **Cross-Validation:**
   - Conducted five-fold cross-validation and calculated Mean Square Error (MSE) scores.

6. **Model Evaluation:**
   - Assessed model performance using MSE, Mean Absolute Error (MAE), and R-squared values.
   - Mean Squared Error : 515.5102998907139, Mean Absolute Error : 14.988880519480512, R-squared : 0.9232183793745715

7. **Results:**
   - The developed model demonstrated an R-squared value close to 1, indicating compatibility with the original dataset.

8. **Visualization:**
   - Plotted actual vs. predicted PM2.5 concentration values.

## Model Deployment

The model was fitted on the test dataset, and the predictions were assessed using various metrics.
