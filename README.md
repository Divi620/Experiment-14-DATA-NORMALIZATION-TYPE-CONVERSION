# EXP_14_Data-_Normalization_type_conversion
# Experiment 14: Data Normalization & Type Conversion

## Overview

This experiment focuses on **data preprocessing techniques**, specifically:

* **Data Normalization**: Scaling numerical data to a standard range.
* **Type Conversion**: Changing data types to ensure consistency and proper analysis.

These steps are essential in data analysis and machine learning to improve model performance and data quality.

---

## Objectives

* Understand the importance of data normalization.
* Apply different normalization techniques.
* Perform type conversion on dataset columns.
* Prepare clean and consistent data for analysis.

---

## Tools & Technologies

* Python 
* NumPy
* Pandas
* Scikit-learn

---

## Dataset

Use any sample dataset (CSV/Excel) containing:

* Numerical values (e.g., age, salary)
* Categorical/text data (e.g., gender, city)

Example:

```
Name, Age, Salary
Alice, 25, 50000
Bob, 30, 60000
Charlie, 35, 70000
```

---

## Steps Performed

### 1. Import Libraries

```python
import pandas as pd
from sklearn.preprocessing import MinMaxScaler, StandardScaler
```

---

### 2. Load Dataset

```python
df = pd.read_csv("data.csv")
print(df.head())
```

---

### 3. Data Type Conversion

Convert columns to appropriate types:

```python
df['Age'] = df['Age'].astype(int)
df['Salary'] = df['Salary'].astype(float)
```

---

### 4. Data Normalization

#### 🔹 Min-Max Normalization

Scales values between 0 and 1:

```python
scaler = MinMaxScaler()
df[['Age', 'Salary']] = scaler.fit_transform(df[['Age', 'Salary']])
```

#### 🔹 Standardization (Z-score)

Centers data around mean with unit variance:

```python
scaler = StandardScaler()
df[['Age', 'Salary']] = scaler.fit_transform(df[['Age', 'Salary']])
```

---

## Output

* Clean dataset with consistent data types.
* Normalized numerical values for better analysis.

---

## Results

* Successfully converted data types.
* Applied normalization techniques.
* Improved dataset quality and usability.

---

## Notes

* Always check for missing values before normalization.
* Choose normalization technique based on use case.
* Ensure categorical data is handled separately.

---

## Conclusion

Data normalization and type conversion are crucial preprocessing steps that:

* Enhance data consistency
* Improve model accuracy
* Reduce bias in machine learning models

---

## 🔗 References

* Scikit-learn Documentation
* Pandas Documentation

---



---
