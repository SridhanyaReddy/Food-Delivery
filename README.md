# Food Delivery Time Prediction

## Project Overview

This project aims to predict the delivery time of food orders using Machine Learning. The dataset is explored and cleaned using Pandas to prepare it for model building.

---

## Weekly Progress

### Phase 1: Data Exploration & Cleaning (Week 1)
In the first notebook ([01_Data_Exploration.ipynb](file:///C:/Users/SRIDHANYA%20REDDY%20MAND/OneDrive/Desktop/Food%20Delivery/notebooks/01_Data_Exploration.ipynb)), the raw dataset was analyzed and cleaned:
* **Exploratory Data Analysis**: Inspected shapes, column types, and statistical properties.
* **Missing Value Imputation**: Handled missing values in `Delivery_person_Age` and `Delivery_person_Ratings` by imputing them with their respective medians.
* **Data Validation**: Verified that no duplicate records existed.
* **Data Export**: Saved the clean intermediate dataset as `cleaned_food_delivery.csv`.

### Phase 2: Baseline Model Training (Week 2)
In the second notebook ([02_Train_First_regression_model.ipynb](file:///C:/Users/SRIDHANYA%20REDDY%20MAND/OneDrive/Desktop/Food%20Delivery/notebooks/02_Train_First_regression_model.ipynb)), a baseline model was trained using the raw numerical features:
* **Target Extraction**: Cleaned `Time_taken(min)` string column to extract exact integer values (e.g., `(min) 24` -> `24`).
* **Feature Selection**: Isolated key numerical features:
  - `Delivery_person_Age`
  - `Delivery_person_Ratings`
  - `Restaurant_latitude`, `Restaurant_longitude`
  - `Delivery_location_latitude`, `Delivery_location_longitude`
  - `Vehicle_condition`
  - `multiple_deliveries` (imputed missing values using the median).
* **Train-Test Split**: Divided the dataset into training (80%) and testing (20%) sets using `random_state=42` for reproducibility.
* **Model Training**: Trained a baseline **Linear Regression** model.

---

## Evaluation Results

The performance of the baseline Linear Regression model on the test dataset (20%) is summarized below:

| Metric | Description | Baseline Value |
| :--- | :--- | :---: |
| **Mean Absolute Error (MAE)** | Average absolute deviation from actual time | **6.14 minutes** |
| **Mean Squared Error (MSE)** | Average squared deviation | **59.57** |
| **Root Mean Squared Error (RMSE)** | Standard deviation of residuals | **7.72 minutes** |
| **R² Score (Coefficient of Determination)** | Variance in target explained by the features | **0.3206 (32.1%)** |

### Key Observations
* **Average Error**: On average, the baseline model's predictions are off by **±6.14 minutes**.
* **Variance Explained**: The selected raw numerical features explain about **32.1%** of the variance in delivery times.
* **Interpretation**: Linear regression provides a reasonable starting baseline, but there is significant room for improvement since the model does not yet utilize categorical variables (like weather or traffic density) or engineered features (like distance).

---

## Setup and Installation

To run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/SridhanyaReddy/Food-Delivery.git
   cd "Food Delivery"
   ```

2. **Install the dependencies**:
   Make sure you have Python installed, then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Jupyter notebooks**:
   ```bash
   jupyter notebook
   ```
   Open and run the notebooks in sequence:
   * [01_Data_Exploration.ipynb](file:///C:/Users/SRIDHANYA%20REDDY%20MAND/OneDrive/Desktop/Food%20Delivery/notebooks/01_Data_Exploration.ipynb)
   * [02_Train_First_regression_model.ipynb](file:///C:/Users/SRIDHANYA%20REDDY%20MAND/OneDrive/Desktop/Food%20Delivery/notebooks/02_Train_First_regression_model.ipynb)
