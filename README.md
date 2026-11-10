# 🏥 Insurance Cost Prediction

<p align="center">
  <b>Machine Learning Project for Medical Insurance Cost Prediction</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/EDA-Completed-success?style=flat-square" alt="EDA">
  <img src="https://img.shields.io/badge/Feature%20Engineering-Completed-success?style=flat-square" alt="Feature Engineering">
  <img src="https://img.shields.io/badge/Feature%20Selection-Chi--Square-blue?style=flat-square" alt="Feature Selection">
</p>

---

## 📌 Overview

**Insurance Cost Prediction** is a Machine Learning project focused on analyzing personal, demographic, and lifestyle-related information to understand and predict **medical insurance charges**.

The project follows a complete data-analysis and preprocessing workflow, starting from raw insurance data and progressing through:

- 📊 Exploratory Data Analysis (EDA)
- 🧹 Data cleaning and preprocessing
- 🔤 Categorical feature encoding
- ⚖️ Feature scaling
- 🧬 Feature engineering
- 🔗 Pearson correlation analysis
- 🧪 Chi-Square feature selection
- 🎯 Final feature preparation for Machine Learning

---

## 🎯 Project Objective

The main objective of this project is to prepare insurance data for a Machine Learning regression problem where:

> **`charges`** is the target variable representing medical insurance cost.

The project investigates which features have meaningful relationships with insurance charges and prepares a refined feature set for predictive modeling.

---

## 📊 Dataset

The dataset contains **1,338 records and 7 original features**.

### Original Features

| Feature | Description |
|---|---|
| 👤 `age` | Age of the individual |
| ⚧️ `sex` | Gender |
| ⚖️ `bmi` | Body Mass Index |
| 👶 `children` | Number of children/dependents |
| 🚬 `smoker` | Smoking status |
| 🌎 `region` | Residential region |
| 💰 `charges` | Medical insurance charges |

### Dataset Statistics

| Statistic | Age | BMI | Children | Charges |
|---|---:|---:|---:|---:|
| Mean | 39.21 | 30.66 | 1.09 | 13,270.42 |
| Minimum | 18 | 15.96 | 0 | 1,121.87 |
| Median | 39 | 30.40 | 1 | 9,382.03 |
| Maximum | 64 | 53.13 | 5 | 63,770.43 |

The dataset contains **no missing values** across the seven original columns.

---

## 🔍 Exploratory Data Analysis

The project performs exploratory analysis to understand the distribution and characteristics of the dataset.

The analysis includes:

- 👶 Children distribution
- ⚧️ Gender distribution
- 🚬 Smoker distribution
- 🌎 Region distribution
- 📈 Numerical feature statistics
- 🔗 Feature-to-target relationships
- 📊 Correlation analysis

The original dataset contains **676 male** and **662 female** records.

Regional distribution:

| Region | Records |
|---|---:|
| Southeast | 364 |
| Southwest | 325 |
| Northwest | 325 |
| Northeast | 324 |



---

## 🧹 Data Preprocessing

The categorical variables are transformed into numerical representations to make the dataset suitable for Machine Learning algorithms.

### Gender Encoding

The `sex` feature is converted into a binary representation:

```text
female → 1
male   → 0
```

### Smoking Encoding

The `smoker` feature is also converted into a binary representation:

```text
yes → 1
no  → 0
```



---

## 🧬 Feature Engineering

A new feature called:

```text
bmi_category
```

is created from the original `bmi` feature.

The BMI values are grouped into categories such as:

- 🟢 Normal
- 🟡 Overweight
- 🔴 Obese

This creates an additional categorical representation of BMI.

The categorical BMI feature is then transformed using one-hot encoding.

Example generated features:

```text
bmi_category_Normal
bmi_category_Overweight
bmi_category_Obese
```



---

## ⚖️ Feature Scaling

Numerical features such as:

- `age`
- `bmi`
- `children`

are standardized during preprocessing.

The transformed values are represented on a standardized scale, making the numerical features more suitable for subsequent Machine Learning processing.

---

## 🔗 Correlation Analysis

Pearson correlation is used to examine the relationship between the processed features and the target variable `charges`.

### Top Correlated Features

| Feature | Pearson Correlation |
|---|---:|
| 🚬 `is_smoker` | **0.787251** |
| 👤 `age` | **0.299009** |
| 🔴 `bmi_category_Obese` | **0.199533** |
| ⚖️ `bmi` | **0.196188** |
| 🌎 `region_southeast` | **0.073981** |
| 👶 `children` | **0.067999** |

The strongest correlation with insurance charges is observed for **`is_smoker`**, with a Pearson correlation of approximately **0.787**.

---

## 🧪 Chi-Square Feature Selection

Chi-Square testing is used to evaluate the relationship between categorical features and the target.

The analysis uses a significance level of:

```text
α = 0.05
```

### Selected Features

Features with statistically significant results include:

| Feature | Chi-Square | p-value | Decision |
|---|---:|---:|---|
| 🚬 `is_smoker` | 854.020268 | 0.000000 | Keep |
| 🌎 `region_southeast` | 15.208814 | 0.001647 | Keep |
| ⚧️ `is_female` | 9.532132 | 0.022992 | Keep |
| 🔴 `bmi_category_Obese` | 8.510101 | 0.036566 | Keep |

Features such as `region_southwest`, `region_northwest`, and the other BMI categories did not meet the selected significance threshold.

---

## ⭐ Final Feature Set

After preprocessing and feature selection, the final dataset contains the following features:

```text
age
is_female
bmi
children
is_smoker
region_southeast
bmi_category_Obese
charges
```

The final feature matrix therefore contains **7 input features plus the target variable `charges`**.

### Feature Pipeline

```text
Raw Dataset
     │
     ▼
Data Cleaning
     │
     ▼
Categorical Encoding
     │
     ▼
Feature Engineering
     │
     ├── BMI Category
     │
     ▼
One-Hot Encoding
     │
     ▼
Feature Scaling
     │
     ▼
Pearson Correlation
     │
     ▼
Chi-Square Feature Selection
     │
     ▼
Final Feature Set
```

---

## 🤖 Machine Learning Problem

This project is structured as a **Supervised Machine Learning Regression** problem.

### Input

Personal and lifestyle-related features:

```text
age
sex
bmi
children
smoker
region
```

### Target

```text
charges
```

The objective is to learn the relationship between the input features and medical insurance charges.

---

## 🛠️ Technologies & Libraries

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Programming |
| 🐼 **Pandas** | Data manipulation & analysis |
| 🔢 **NumPy** | Numerical computing |
| 📊 **Matplotlib** | Data visualization |
| 🎨 **Seaborn** | Statistical visualization |
| 🤖 **Scikit-learn** | Data preprocessing & ML |
| 📓 **Jupyter Notebook** | Development & experimentation |

---

## 📁 Project Structure

```text
insurance_model/
│
├── 📄 insurance.csv
├── 📓 insurance.ipynb
└── 📄 README.md
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/fahimshahariar56/insurance_model.git
```

### 2. Navigate to the Project

```bash
cd insurance_model
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

### 5. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 6. Start Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
insurance.ipynb
```

---

## 📚 Key Learning Outcomes

This project demonstrates practical understanding of:

- ✅ Data loading and inspection
- ✅ DataFrame analysis
- ✅ Missing-value checking
- ✅ Exploratory Data Analysis
- ✅ Categorical encoding
- ✅ Feature engineering
- ✅ One-hot encoding
- ✅ Feature scaling
- ✅ Pearson correlation
- ✅ Chi-Square statistical testing
- ✅ Feature selection
- ✅ Preparing data for regression

---

## 🔮 Future Improvements

Possible future improvements include:

- [ ] 🤖 Train multiple regression models
- [ ] 📊 Compare model performance
- [ ] ⚙️ Hyperparameter tuning
- [ ] 🔁 Cross-validation
- [ ] 📏 Add MAE, MSE, RMSE and R² evaluation
- [ ] 🧠 Add SHAP-based model explainability
- [ ] 🌐 Build a FastAPI prediction service
- [ ] 🖥️ Build an interactive web interface
- [ ] 🐳 Dockerize the application
- [ ] 🚀 Deploy the complete ML application

---

## ⚠️ Disclaimer

This project is created for **educational and Machine Learning practice purposes**.

The predicted insurance charges should not be considered real insurance quotes, medical advice, or financial advice.

---

## 👨‍💻 Author

### Fahim Shahariar

**CSE Student | Software Engineering & Machine Learning Enthusiast**

🔗 GitHub:  
https://github.com/fahimshahariar56

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

<p align="center">
  <b>Built with 🐍 Python • 📊 Data Science • 🤖 Machine Learning</b>
</p>