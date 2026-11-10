# 🏥 Insurance Cost Prediction

<p align="center">
  <b>Machine Learning Project for Predicting Medical Insurance Costs</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Machine%20Learning-Regression-orange?style=for-the-badge" alt="Machine Learning">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status">
</p>

---

## 📌 Overview

**Insurance Cost Prediction** is a Machine Learning project that analyzes personal and demographic information to predict an individual's **medical insurance cost**.

The project uses a real-world style insurance dataset and explores how factors such as **age, BMI, smoking status, number of children, gender, and region** influence insurance charges.

The complete workflow is implemented in a Jupyter Notebook, covering:

- 📊 Data exploration
- 🧹 Data preprocessing
- 🔍 Exploratory Data Analysis (EDA)
- 📈 Data visualization
- 🧠 Machine Learning model development
- 📏 Model evaluation
- 💰 Insurance cost prediction

---

## 🎯 Project Objective

The primary objective of this project is to build a Machine Learning model capable of estimating medical insurance charges based on an individual's characteristics.

### Input Features

| Feature | Description |
|---|---|
| 👤 `age` | Age of the individual |
| ⚧️ `sex` | Gender |
| ⚖️ `bmi` | Body Mass Index |
| 👶 `children` | Number of dependents/children |
| 🚬 `smoker` | Smoking status |
| 🌎 `region` | Residential region |

### 🎯 Target

**`charges`** — Estimated medical insurance cost.

---

## 🧠 Machine Learning Workflow

```text
              📂 Dataset
                  │
                  ▼
          🔍 Data Exploration
                  │
                  ▼
          🧹 Data Preprocessing
                  │
                  ▼
       📊 Exploratory Data Analysis
                  │
                  ▼
         🔧 Feature Engineering
                  │
                  ▼
        🧠 Model Training
                  │
                  ▼
         📏 Model Evaluation
                  │
                  ▼
        💰 Cost Prediction
```

---

## 📊 Dataset

The project uses an insurance dataset containing demographic, lifestyle, and medical-related attributes.

The dataset includes:

- Age
- Gender
- BMI
- Number of children
- Smoking status
- Region
- Medical insurance charges

The dataset is included in this repository as:

```text
insurance.csv
```

---

## 🔎 Exploratory Data Analysis

The notebook investigates relationships between the input variables and insurance charges.

Some of the major analysis areas include:

- 📈 Age vs. insurance charges
- ⚖️ BMI vs. insurance charges
- 🚬 Smoking status vs. insurance charges
- 👶 Number of children vs. insurance charges
- 🌎 Region-wise insurance charges
- ⚧️ Gender-wise insurance charges
- 🔗 Correlation between numerical features

These visualizations help identify important patterns and relationships within the dataset.

---

## 🧹 Data Preprocessing

Before training the Machine Learning model, the dataset is prepared through several preprocessing steps.

Typical preprocessing includes:

- Handling categorical variables
- Encoding categorical features
- Preparing numerical features
- Separating input features and target
- Splitting the dataset into training and testing sets

---

## 🤖 Machine Learning

This project focuses on **Regression**, because the target variable `charges` represents a continuous numerical value.

The model learns the relationship between the individual's characteristics and their medical insurance cost.

### Prediction Example

```text
Age:              30
BMI:              27.5
Children:          2
Smoker:           No
Region:           Southeast
Sex:              Male

              ↓

       🤖 ML Model

              ↓

Estimated Insurance Cost
```

---

## 📏 Model Evaluation

The model's performance can be evaluated using common regression metrics such as:

- **MAE — Mean Absolute Error**
- **MSE — Mean Squared Error**
- **RMSE — Root Mean Squared Error**
- **R² Score — Coefficient of Determination**

These metrics help determine how accurately the model predicts insurance charges.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Programming language |
| 📊 **Pandas** | Data manipulation |
| 🔢 **NumPy** | Numerical computing |
| 📈 **Matplotlib** | Data visualization |
| 🎨 **Seaborn** | Statistical visualization |
| 🧠 **Scikit-learn** | Machine Learning |
| 📓 **Jupyter Notebook** | Development & experimentation |

---

## 📁 Project Structure

```text
insurance_model/
│
├── 📄 insurance.csv
│
├── 📓 insurance.ipynb
│
└── 📄 README.md
```

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/fahimshahariar56/insurance_model.git
```

### 2️⃣ Navigate to the Project

```bash
cd insurance_model
```

### 3️⃣ Create a Virtual Environment

```bash
python -m venv venv
```

### 4️⃣ Activate the Environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

### 5️⃣ Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 6️⃣ Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
insurance.ipynb
```

---

## 📈 Key Insights

The analysis demonstrates that several factors can have a significant relationship with medical insurance costs.

In particular:

- 🚬 **Smoking status** can strongly influence insurance charges.
- 👤 **Age** can affect expected medical expenses.
- ⚖️ **BMI** may contribute to differences in insurance costs.
- 👶 **Number of children** can have an impact on overall charges.
- 🌎 **Region** may also contribute to variation in insurance costs.

> **Note:** These relationships represent patterns learned from the dataset and should not be interpreted as medical, financial, or insurance advice.

---

## ⚠️ Limitations

This project is intended for **educational and Machine Learning practice purposes**.

The predictions should not be considered actual insurance quotes.

Real-world insurance pricing can depend on many additional factors, including:

- Medical history
- Policy coverage
- Claim history
- Insurance provider rules
- Local regulations
- Additional demographic and financial information

---

## 🔮 Future Improvements

Potential improvements for this project include:

- [ ] 🔬 Advanced feature engineering
- [ ] 🤖 Compare multiple regression algorithms
- [ ] ⚙️ Hyperparameter tuning
- [ ] 📊 Cross-validation
- [ ] 📈 Advanced model evaluation
- [ ] 🧠 Explainable AI with SHAP
- [ ] 🌐 Build a prediction API using FastAPI
- [ ] 🖥️ Create an interactive frontend
- [ ] 🚀 Deploy the model as a web application
- [ ] 🐳 Add Docker support
- [ ] 🔄 Create an automated ML pipeline

---

## 🎓 Learning Outcomes

Through this project, the following Machine Learning concepts are practiced:

- Data preprocessing
- Exploratory Data Analysis
- Feature analysis
- Categorical encoding
- Regression
- Model training
- Model evaluation
- Data visualization
- Prediction workflow

---

## 👨‍💻 Author

### Fahim Shahariar

**CSE Student | Software Engineering & Machine Learning Enthusiast**

🔗 GitHub:  
https://github.com/fahimshahariar56

---

## ⭐ Support

If you find this project useful or interesting, consider giving the repository a ⭐.

---

<p align="center">
  <b>Built with 🐍 Python & 🤖 Machine Learning</b>
</p>