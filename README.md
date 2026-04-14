# 🔋 EV Battery Thermal Runaway Prediction using Machine Learning

## 📌 Overview
This project focuses on analyzing Electric Vehicle (EV) battery charging data to predict **battery safety events** and **thermal runaway probability** using Machine Learning models.

Thermal runaway is a hazardous condition in EV batteries that can lead to overheating or failure. This project leverages data-driven techniques to identify patterns and build predictive models that enhance battery safety monitoring.

---

## 📂 Dataset
The dataset represents EV battery charging behavior and system conditions during different charging stages.

- **Source:** Kaggle  
- **Path:** `/kaggle/input/ev-battery-charging-and-thermal-runaway-dataset`

The dataset contains both numerical and categorical features related to battery health and system conditions.

---

## 📊 Dataset Details

**Features used in the project:**
- Voltage (V)
- Current (A)
- Temperature (°C)
- State of Charge (SOC %)
- Charging Stage
- BMS Status
- Moisture Detected
- Event Flag (Normal / Warning / Alarm)
- Thermal Runaway Probability (TR_Probability)

**Removed Columns:**
- Timestamp
- Notes

---

## ⚙️ Data Handling
- Loaded dataset using Pandas DataFrame
- Removed irrelevant columns
- Checked for missing values
- Applied Label Encoding on categorical features:
  - ChargerID
  - CellID
  - ChargingStage
  - BMS_Status
  - MoistureDetected
  - EventFlag

### 📊 Exploratory Data Analysis (EDA)
- Boxplots for:
  - Temperature
  - Current
  - Voltage
- Correlation heatmap to analyze relationships

### 🚨 Outlier Detection
- Used IQR (Interquartile Range) method
- Detected outliers in:
  - Temperature
  - Current
  - Voltage

---

## 🤖 Model

### 🔹 Classification Model
- **Algorithm:** Random Forest Classifier
- **Target:** EventFlag
- **Purpose:** Predict battery safety condition

---

### 🔹 Regression Model
- **Algorithm:** Random Forest Regressor
- **Target:** TR_Probability
- **Purpose:** Predict thermal runaway probability

---

## 📈 Performance

### 🔹 Classification Metrics
- Accuracy: High (based on test data)
- Precision, Recall, F1-score evaluated
- Confusion Matrix used for performance analysis

### 🔹 Regression Metrics
- R² Score: Strong model fit
- MAE (Mean Absolute Error): Low
- RMSE (Root Mean Squared Error): Low

---

## 🔑 Key Points
- Temperature is the most critical factor affecting battery safety
- Voltage and current significantly influence risk levels
- Random Forest performs well for both tasks
- Proper preprocessing improves model performance
- Can be extended to real-time EV monitoring systems

---

## 🛠 Tech Stack
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## 👩‍💻 Author
**Shreyasi Rawat**

---
