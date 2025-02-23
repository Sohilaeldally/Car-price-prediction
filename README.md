# Car Price Prediction


## Overview  
This project focuses on cleaning and analyzing a car dataset to ensure data quality before applying machine learning models. The dataset contains various attributes related to car specifications, including brand, type, year of manufacturing, fuel type, and more. The goal is to clean the dataset, extract useful insights, and apply predictive modeling.  

## Data Cleaning  

Data cleaning was performed to handle missing values, remove inconsistencies, and standardize column values. Below are the key cleaning steps applied:  

### 1. Handling Inconsistent Strings  

- Standardized **Brand** names by converting text to lowercase and removing unnecessary words (e.g., `'i love'`, `'is the best'`).  
- Cleaned **Type** by removing prefixes like `'woow '` and standardizing type names.  
- Adjusted **VehicleModel** by removing special characters and unwanted phrases.  

### 2. Numeric Data Cleaning  

- **Manufacturing Year**: Removed non-numeric characters and filtered unrealistic values (below `1800` or above `2024`).  
- **Cylinder Count**: Converted to integers while handling missing values.  
- **Odometer**: Extracted numeric values and converted them into a proper format.  
- **Capacity**: Removed suffixes like `' Turbo'` and converted to float.  
- **Airbags**: Ensured valid values (`0-12`) and replaced invalid numbers with `NaN`.  

### 3. Categorical Data Standardization  

- Standardized **fuel** values (e.g., `'others' → 'other'`, `'hyb' → 'Electric Hybrid'`).  
- Cleaned **type of gear** column by converting text to lowercase and removing extra spaces.  
- Converted **Duty** column to numeric, ensuring only valid numbers remained.  

## Exploratory Data Analysis (EDA) Insights  

### Key Findings  

- Most cars in the dataset were manufactured between **2000 and 2023**, with a peak around **2015-2018**.  
- **SUVs** and **Sedans** were the most common car types, while **electric and hybrid cars** made up a small fraction.  
- The distribution of **odometer** readings showed a wide range, with some outliers having exceptionally high mileage.  
- There was a strong correlation between **engine capacity** and **cylinder count**, which aligns with expected automotive standards.  

## Model Implementation  

### **Price Prediction Model**  

- **Features Used**: Manufacturing Year, Brand, Vehicle Type, Odometer, Fuel Type, Airbags, Capacity, Gear Type.  
- **Algorithms Tried**: Linear Regression, Random Forest, XGBoost.  
- **Best Model**: XGBoost with **MAE of `6455.239682`** and **R² of `0.435644`**.  
 

## How to Run  

### **Setup the Environment**  
```bash
pip install -r requirements.txt
