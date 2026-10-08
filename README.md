# 🌾 Agriculture Production & Yield Forecasting Project

## 📌 Project Overview

This project analyzes agricultural crop production data and rainfall data to understand the relationship between weather conditions and crop productivity. The project uses Machine Learning models to forecast crop production and yield and compares model performance with and without rainfall information.

---

## 🎯 Objectives

- Clean and preprocess agricultural datasets.
- Perform Exploratory Data Analysis (EDA).
- Detect and handle outliers.
- Analyze correlations among variables.
- Merge crop and rainfall datasets.
- Build Machine Learning models:
  - Without rainfall data
  - With rainfall data
- Compare model performance.
- Forecast future agricultural production and yield.

---

## 📂 Datasets Used

### 1. Crop Dataset

Contains:

- State
- District
- Crop
- Season
- Year
- Area
- Production
- Yield

### 2. Rainfall Dataset

Contains:

- State
- Date
- Actual Rainfall
- Normal Rainfall
- Rainfall Deviation
- Rainfall Ratio

---

# 🔹 Step 1: Data Cleaning

The following cleaning operations were performed:

### Remove Duplicate Records

- Checked duplicate rows.
- Removed duplicate records.

### Handle Missing Values

- Identified missing values.
- Filled missing rainfall values using State-wise Median.
- Remaining missing values filled using overall Median.

### Data Consistency Checks

- Verified data types.
- Standardized State names.
- Checked unique values.

---

# 🔹 Step 2: Exploratory Data Analysis (EDA)

### Univariate Analysis

- Distribution of Area
- Distribution of Production
- Distribution of Yield

### Bivariate Analysis

- Area vs Production
- Area vs Yield
- Production vs Yield

### Visualizations

- Histograms
- Boxplots
- Scatterplots
- Correlation Heatmaps

---

# 🔹 Step 3: Outlier Analysis

Outliers were detected using the IQR Method.

### Formula

Q1 = 25th Percentile

Q3 = 75th Percentile

IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR

### Columns Checked

- Area
- Production
- Yield
- Actual Rainfall
- Normal Rainfall
- Rainfall Ratio

Outlier percentages were calculated before deciding whether removal was required.

---

# 🔹 Step 4: Correlation Analysis

Correlation analysis was performed to understand relationships between variables.

### Crop Dataset

- Area vs Production
- Area vs Yield
- Production vs Yield

### Rainfall Dataset

- Actual Rainfall vs Normal Rainfall
- Actual Rainfall vs Rainfall Ratio
- Normal Rainfall vs Rainfall Ratio

Highly correlated features were reviewed before model building.

---

# 🔹 Step 5: Feature Engineering

New features were created:

### Year_Number

Extracted from Crop_Year.

Example:

2008-09 → 2008

### Rainfall_Deviation

Rainfall_Deviation = Actual_Rainfall − Normal_Rainfall

### Rainfall_Ratio

Rainfall_Ratio = Actual_Rainfall / Normal_Rainfall

These features help Machine Learning models better understand rainfall conditions.

---

# 🔹 Step 6: Dataset Merging

Crop and Rainfall datasets were merged using:

- State
- Crop_Year

### Merge Type

Left Join

Result:

- Full Crop Dataset
- Weather Dataset (records having rainfall information)

---

# 🔹 Step 7: Model Building

## A. Models Without Rainfall Data

Features:

- State
- District
- Season
- Area
- Year_Number

Targets:

### Crop Prediction

Model:

- Random Forest Classifier

### Production Prediction

Model:

- Random Forest Regressor

### Yield Prediction

Model:

- Random Forest Regressor

---

## B. Models With Rainfall Data

Additional Features:

- Actual_Rainfall
- Normal_Rainfall
- Rainfall_Deviation
- Rainfall_Ratio

Targets:

### Crop Prediction

Model:

- Random Forest Classifier

### Production Prediction

Model:

- Random Forest Regressor

### Yield Prediction

Model:

- Random Forest Regressor

---

# 📊 Model Results

## Without Rainfall

- Crop Accuracy = 0.166
- Production R² = 0.937
- Yield R² = 0.696

## With Rainfall

- Crop Accuracy = 0.155
- Production R² = 0.939
- Yield R² = 0.917

### Observation

Rainfall information significantly improved Yield prediction performance.

---

# 🔮 Future Forecasting

Forecasts were generated for:

- 2027
- 2028
- 2029
- 2030
- 2031
- 2032

Predictions include:

- Expected Crop
- Expected Production
- Expected Yield

for different State–District combinations.

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab

---

# 📈 Machine Learning Algorithms Used

### Classification

- Random Forest Classifier

### Regression

- Random Forest Regressor

---

# 🚀 Future Improvements

- Add temperature dataset
- Add soil dataset
- Add fertilizer usage dataset
- Add market price forecasting
- Deep Learning models
- Time Series Forecasting

---

## 👨‍💻 Author

Samesh Kumar

Advanced Data Science & AI

Agriculture Production and Yield Forecasting Project
