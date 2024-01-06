# Space Travel Passenger Transport Prediction Model

## Overview
This repository features a machine learning model designed to predict whether passengers of a space travel company are likely to be transported. The model employs CatBoostClassifier, a machine learning algorithm known for handling categorical data effectively.

## Data
The model is trained and tested using two datasets:
- `train.csv`: Training data with passenger features and transportation status.
- `test.csv`: Testing data with passenger features.

## Features
The datasets include a mix of categorical and numerical features related to passengers. Features include HomePlanet, CryoSleep, Destination, Age, VIP status, and various service usages.

## Preprocessing
Key preprocessing steps are:
- Feature extraction from 'Cabin' to get 'Deck', 'Room', and 'Side'.
- Handling missing values:
  - Numerical features: Imputed with mean values.
  - Categorical features: Imputed with the most frequent values.
- Scaling numerical features using StandardScaler.
- Encoding categorical features using OneHotEncoder.
- Label encoding the target variable.

## Feature Engineering
The 'Cabin' feature is parsed into three separate features: 'Deck', 'Room', and 'Side', to extract more meaningful information.

## Model Training
The CatBoostClassifier model is trained on the preprocessed data. Key aspects of the model training include:
- Iterations: 5
- Learning rate: 0.1
- Loss function: CrossEntropy

## Prediction and Output
The model predicts the transportation status for the test data. Predictions are converted to binary format based on a specified threshold and exported to 'predictions1.csv'.

## Usage
To use the model:
1. Load the training and testing datasets.
2. Preprocess the data by handling missing values, encoding features, and scaling numerical features.
3. Train the CatBoostClassifier model using the training data.
4. Predict transportation status for the test data.
5. Export the predictions to 'predictions1.csv'.

## Dependencies
- pandas
- numpy
- scikit-learn
- catboost

## Note
This code is tailored for a specific scenario of predicting passenger transportation status in a space travel context and can be adapted for similar predictive modeling tasks.
