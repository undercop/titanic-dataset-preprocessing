# 🚢 Titanic Data Cleaning & Analysis with Pandas

This project performs **data cleaning and exploratory analysis** on the famous Titanic dataset using Python and Pandas. It covers identifying and handling missing values, removing duplicates, summarizing statistics, and visualizing key patterns in the data.

---

## 📊 Dataset Used

**Source:** [Kaggle - Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)  
**Rows:** 891  
**Columns:** 12  

Main features:
- `Survived` (target)
- `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`
- `Name`, `Ticket`, `Cabin` (text-based/non-numeric)

---

## 🧹 What Was Done

### 🔍 1. **Data Exploration**
- Loaded the dataset using `pandas.read_csv()`
- Checked column types, non-null counts, and basic statistics using:
  ```python
  df.info(), df.describe(), df.isnull().sum()

  ### 🧼 2. Data Cleaning

- **Missing Values:**
  - Filled missing `Age` values with the **median**
  - Filled missing `Embarked` values with the **mode**
  - Dropped `Cabin` due to excessive missing values (~77%)

- **Duplicates:**
  - Checked for duplicates using `df.duplicated().sum()`
  - No duplicate rows were found

---

### 🔍 3. Data Types & Feature Overview

- Identified column types (numeric vs categorical)
- Checked unique values in features like `Pclass`, `Sex`, `Embarked`

---

## 📈 Visualizations (Optional)

- Used `seaborn` and `matplotlib` to visualize:
  - Survival distribution
  - Class and gender-wise survival rates
  - Age and fare distributions

---

## 🧠 Key Learnings

- How to identify and handle missing and duplicate data
- Choosing **median** for numeric imputation and **mode** for categorical
- The importance of `df[col] = df[col].fillna(...)` over `inplace=True` to avoid future warnings
- Basic EDA skills using Pandas and plotting libraries

---

## 🛠️ Tech Stack

- Python 3.8+
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## ▶️ How to Run

1. Clone the repository and navigate to the folder:
   ```bash
   git clone <repo-url>
   cd titanic-data-cleaning

