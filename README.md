# Flight Delay Time Prediction Using Ensemble Learning

## Overview
This repository contains the solution for **Assignment 1** of the **Deep Learning (Fall 2024)** course. The task focuses on predicting flight delay times using an **ensemble learning** approach. The models were implemented from scratch using only **Pandas** and **NumPy**—with no external machine learning libraries like Scikit-learn allowed.

The ensemble model combines three machine learning algorithms: 
1. **Support Vector Machine (SVM)** (with multiple kernels)
2. **Decision Trees**
3. **Logistic Regression**

The main objective is to accurately predict delays in departure times, based on flight data from 2023-2024, gathered for flights departing from Lahore (LHE), Karachi (KHI), and Islamabad (ISB) airports.

## Dataset
The dataset used for this project includes information related to:
- Departure and estimated departure times
- Delay times (in minutes)
- Arrival details (destination, time, etc.)
- Airline and flight-specific information

### Target Variable
The primary target variable is `delay_time` (departure delay in minutes), which is **binned into 8 distinct categories** for classification purposes.

## Models
The following models have been implemented from scratch:
1. **Multi-Kernel Support Vector Machine (SVM)**: 
   - Supports multiple kernels like Linear, Polynomial, and RBF.
2. **Decision Tree Classifier**: 
   - Constructs a tree to classify the binned delay times.
3. **Logistic Regression**: 
   - Implements binary classification using gradient descent and sigmoid activation.

### Ensemble Learning
The models are combined using an ensemble learning technique. You can experiment with bagging or boosting approaches. Our final approach included:
- Cross-validation for evaluating model performance.
- F1-Score and Accuracy as the evaluation metrics.

### Model Performance
- **Accuracy**: The model achieved an **accuracy of 99%** on the flight delay dataset.
- **F1-Score**: The ensemble model obtained an **F1-Score of 93%**.

## Features & Preprocessing
Key steps in data preprocessing:
- **Feature Selection**: Selecting relevant columns such as departure time, destination, and flight details. New features like `time_of_day` or `destination_code` were derived for improved performance.
- **Data Cleaning**: Handling missing or incorrect data, and filtering for only active flights (where `status == active`).

## Evaluation Metrics
- **Accuracy**: Overall correct predictions over total predictions.
- **F1-Score**: A harmonic mean between precision and recall to evaluate performance under imbalanced classes.

## Deliverables
This repository includes the following:
- Jupyter Notebooks implementing the models and combining them into an ensemble.
- A detailed report discussing:
  - The selected features
  - The ensemble method (e.g., stacking, bagging, boosting)
  - The performance metrics (accuracy, F1-score) of the ensemble.

## Bonus Achievements
- Implementation of more than three different types of models in the ensemble.
- Achieving an accuracy score of over **93%** on the flight delay dataset.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Flight-Delay-Prediction-Ensemble.git
