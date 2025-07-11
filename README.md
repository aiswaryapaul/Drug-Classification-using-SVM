# 💊 Drug Classification using Support Vector Machine (SVM)

This project aims to predict which **drug** a patient should be prescribed based on features like age, sex, blood pressure, cholesterol, and sodium-to-potassium ratio using a **Support Vector Machine (SVM)** classifier.

## 📊 Dataset Overview

- **Features**: Age, Sex, BP (Blood Pressure), Cholesterol, Na_to_K (Sodium to Potassium ratio)
- **Target**: Drug (DrugA, DrugB, DrugC, DrugX, DrugY)
- **Size**: 200 records

## 🔍 Exploratory Data Analysis (EDA)

1. **Null Values**:  
   - Checked using `df.isnull().sum()` → No missing values found ✅

2. **Duplicates**:  
   - Checked using `df.duplicated().sum()` → Removed any duplicates

3. **Outliers**:  
   - Visualized numerical features like `Age` and `Na_to_K` using boxplots

## 🧪 Data Preprocessing

- **Label Encoding** for categorical features:
  - `Sex`, `BP`, `Cholesterol`, and `Drug` encoded using `LabelEncoder`

- **Feature-Target Split**:
  ```python
  X = df.drop('Drug', axis=1)
  y = df['Drug']
