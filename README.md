#  Food Delivery Time Prediction

## Project Overview

This project aims to predict the delivery time of food orders using Machine Learning. The dataset is explored and cleaned using Pandas to prepare it for model building.

---

## Features (Input Variables)

The model uses the following features to predict delivery time:

- Delivery Person Age
- Delivery Person Ratings
- Restaurant Location
- Delivery Location
- Order Date
- Order Time
- Pickup Time
- Weather Conditions
- Road Traffic Density
- Vehicle Condition
- Type of Order
- Type of Vehicle
- Multiple Deliveries
- Festival
- City

---

## Label (Target Variable)

- **Time_taken(min)**

---

## Weekly Progress

### Week 1: Data Exploration & Cleaning
- Loaded the dataset using Pandas
- Explored columns, data shapes, and types
- Checked for and handled missing values (imputed Age and Ratings using medians)
- Verified duplicates and saved the cleaned dataset to `data/processed/cleaned_food_delivery.csv`

### Week 2: Baseline Model Training
- Cleaned and prepared string columns: `Time_taken(min)` (extracted numeric values) and `multiple_deliveries` (imputed missing string values with median)
- Selected 8 baseline numerical features
- Split dataset using `train_test_split()` (80% Train, 20% Test, `random_state=42`)
- Trained a **Linear Regression** model on training data
- Evaluated performance on test data:
  - **Mean Absolute Error (MAE)**: 6.14 minutes
  - **Mean Squared Error (MSE)**: 59.57
  - **Root Mean Squared Error (RMSE)**: 7.72 minutes
  - **R² Score**: 0.3206

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn (Linear Regression, Train-Test Split, Evaluation Metrics)
- Jupyter Notebook
- VS Code

---

## Dataset

Food Delivery Dataset containing information about delivery personnel, restaurant and delivery locations, weather conditions, traffic density, vehicle details, and delivery time.