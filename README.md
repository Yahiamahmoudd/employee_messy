# Employee Data Cleaning & Preprocessing 📊🧹

This repository contains a Python-based data cleaning and preprocessing pipeline designed to handle "messy" human resources (HR) datasets. The project utilizes libraries such as **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn** to transform raw, inconsistent data into a structured and clean format suitable for data analysis, dashboards, and machine learning models.

## 🛠️ Features & Data Cleaning Steps

1. **Exploratory Data Analysis (EDA):**
   - Assessed the dataset shape ($25,000$ rows) and inspected structural information (`df.info()`, `df.head()`).
   - Identified and analyzed the percentage of missing values across all columns.

2. **Text Standardization & Formatting:**
   - Standardized column names by capitalizing them (e.g., `employee_id` ➔ `Employee_id`).
   - Cleaned categorical data in the `Department` column: handled case inconsistencies, grouped duplicates (e.g., changing 'Tech' to 'Technology', and 'Human resources' to 'Hr'), and capitalized department values.

3. **Handling Missing Values:**
   - Missing data in essential columns like `Department` and `Employee_id` were imputed using `.fillna('Unknown')`.

4. **Numerical Data Conversion & Cleaning:**
   - Stripped special symbols like currency signs (`$`) and multiplier abbreviations (`k` for thousands) from the `Salary` attribute.
   - Fixed decimal separators and converted variables to proper data types (`float`).

5. **Outliers Detection & Removal:**
   - Implemented the **Interquartile Range (IQR)** method to filter out extreme anomalies and un-realistic entries in financial metrics (e.g., accidental multi-million entries).
   - Visualized the adjusted values using **Boxplots** (`matplotlib`).

## 📊 Dataset Overview (Post-Cleaning)
The pipeline manages the following employee features:
- **Employee_id**: Unique identifier for staff.
- **Department**: Assigned corporate unit (Technology, Finance, Sales, Hr, It, Unknown).
- **Salary**: Numeric annual or monthly compensation.
- **Years_experience**: Total professional history.
- **Performance_score**: Evaluation metric (Numeric/Categorical variables).
- **Promotion_last_5years**: Historical career advancement indicators.
- **Work_hours_per_week**: Standard weekly workload hours.

## 🚀 Technologies Used
- **Python 3**
- **Pandas** & **NumPy** (Data Wrangling)
- **Matplotlib** & **Seaborn** (Statistical Data Visualization)
- **Google Colab / Jupyter Notebooks**

## 📂 Project Structure
- `Employee_Data_Cleaning.ipynb` - The main interactive notebook containing the cleaning workflow and visualizations.
- `employee_messy.csv` - Raw source file containing inconsistencies and missing rows.

---
*Developed as part of data analysis portfolio projects focusing on data quality and robust pipeline engineering.*
