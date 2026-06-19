
# 7006SCN — Machine Learning and Big Data

### Coursework MAYJUL · NYC Yellow Taxi High-Tip Prediction

**Module:** 7006SCN Machine Learning and Big Data · Coventry University

**Module Leaders:** 

**Student Name:** NAGARAJU

**Student ID:** 16549283

**Submission**:

---

# Problem Statement

The aim of this project is to predict whether a New York City taxi trip will generate a high tip using large-scale taxi trip records. The problem is formulated as a binary classification task where trips with a tip amount greater than $5 are classified as High Tip (1), while all other trips are classified as Low Tip (0).

---

# Dataset

| Property | Value |
|-----------|---------|
| Dataset | NYC Yellow Taxi Trip Records |
| Source | NYC Taxi and Limousine Commission (TLC) |
| Official Dataset Page | https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page |
| Period | January 2024 – April 2024 |
| Records | 13,069,067 |
| Columns | 19 |
| Type | Big Data Classification |
| Target Variable | high_tip |
| Processing Framework | PySpark 4.0.2 |
| Licence | NYC Taxi and Limousine Commission (TLC) by technology providers authorized under the Taxicab & Livery Passenger Enhancement Programs (TPEP/LPEP) |

---

# CW Compliance Checklist

✅ Greater than 10 million rows

✅ Greater than 10 columns

✅ Classification problem

✅ Entire pipeline implemented using PySpark

✅ Real-world public dataset

✅ Suitable for distributed computing

✅ Machine Learning and Big Data workflow completed

✅ Tableau dashboard visualisation included

---

# Big Data Characteristics (5Vs)

### Volume

Over 13 million taxi trip records.

### Velocity

Continuous generation of transportation records.

### Variety

Contains numerical, categorical and temporal features.

### Veracity

Missing values handled through data preprocessing.

### Value

Provides insights into passenger tipping behaviour.

---

# Repository Structure

```text

7006SCN_N_16549283/
│
├── data/
│   └── README.md                         # Dataset download instructions
│
├── models/
│   ├── README.md                         # Model outputs description
│   ├── NYC_Taxi_Tableau_Data.xlsx
│   ├── feature_importance.csv
│   ├── model_metrics.csv
│   ├── scalability_metrics.csv
│   └── stability_metrics.csv
│
├── notebooks/
│   ├── Task1.ipynb                       # Problem & Dataset Description
│   ├── Task2.ipynb                       # Data Engineering
│   ├── Task3.ipynb                       # ML Model Portfolio
│   ├── Task4.ipynb                       # Distributed Computing
│   ├── Task5.ipynb                       # Model Evaluation & Stability
│   └── Task6.ipynb                       # Tableau Storytelling
│
├── outputs/
│   ├── Dashboard 1 (Data Quality).twb
│   ├── Dashboard 2 (Model metrics).twb
│   ├── Dashboard 3 (Feature importance).twb
│   ├── Dashboard 4 (Scalability Analysis).twb
│   └── README.md
│
├── task1-dataset/
│   ├── README.md
│   └── Task1.ipynb
│
├── task2-engineering/
│   ├── README.md
│   └── Task2.ipynb
│
├── task3-models/
│   ├── README.md
│   └── Task3.ipynb
│
├── task4-distributed/
│   ├── README.md
│   └── Task4.ipynb
│
├── task5-evaluation/
│   ├── README.md
│   └── Task5.ipynb
│
├── task6-tableau/
│   ├── README.md
│   └── Task6.ipynb
│
└── README.md                             # Main project documentation

```

# Running Order

Run the notebooks sequentially as each task builds upon the outputs from the previous stage.

```text
Task1.ipynb  → Dataset Understanding & Problem Definition

Task2.ipynb  → Data Cleaning, Feature Engineering & Pipeline Construction

Task3.ipynb  → Machine Learning Model Development

Task4.ipynb  → Distributed Computing & Scalability Analysis

Task5.ipynb  → Model Evaluation, Stability Analysis & Explainability

Task6.ipynb  → Tableau Dashboard Preparation & Storytelling
```

---

# Task Overview

| Task   | Description                                                  |
| ------ | ------------------------------------------------------------ |
| Task 1 | Problem Definition and Dataset Description                   |
| Task 2 | Data Cleaning, Feature Engineering and Pipeline Construction |
| Task 3 | Machine Learning Model Development                           |
| Task 4 | Distributed Computing and Scalability Analysis               |
| Task 5 | Model Evaluation, Stability Analysis and Explainability      |
| Task 6 | Tableau Dashboard Development and Storytelling               |

---

# Machine Learning Models

Four machine learning algorithms were implemented and evaluated using PySpark.

| Model                        | Hyperparameters              |
| ---------------------------- | ---------------------------- |
| Logistic Regression          | Default configuration        |
| Decision Tree                | maxDepth = 10                |
| Random Forest                | numTrees = 50, maxDepth = 10 |
| Gradient Boosted Trees (GBT) | maxDepth = 8, maxIter = 20   |

---

# Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| Logistic Regression | 0.8799   | 0.8724    | 0.8799 | 0.8679   | 0.9295  |
| Decision Tree       | 0.9307   | 0.9320    | 0.9307 | 0.9313   | 0.9558  |
| Random Forest       | 0.9305   | 0.9315    | 0.9305 | 0.9310   | 0.9556  |
| GBT                 | 0.9314   | 0.9323    | 0.9314 | 0.9318   | 0.9584  |

### Best Model

Gradient Boosted Trees (GBT) achieved the best overall performance with:

* Accuracy: 93.14%
* F1 Score: 0.9318
* ROC-AUC: 0.9584

---

# Distributed Computing Results

| Experiment            | Execution Time (Seconds) |
| --------------------- | ------------------------ |
| Without Cache         | 4.063                    |
| With Cache            | 1.559                    |
| Repartitioned Dataset | 4.612                    |

Caching improved performance by approximately **61.6%**.

---

# Explainability

Model explainability was performed using **LIME**.

Important factors influencing predictions included:

* Fare Amount
* Trip Duration
* Trip Distance
* Payment Type
* Pickup and Drop-off Locations

---

# Tableau Dashboards

The project includes four Tableau dashboards:

1. Data Quality Dashboard
2. Model Metrics Comparison Dashboard
3. Feature Importance Dashboard
4. Scalability Analysis Dashboard

---

# Technologies Used

* Python
* PySpark 4.0.2
* Pandas
* NumPy
* Matplotlib
* LIME
* Tableau

---

# Author

**NAGARAJU**

Student ID: **16549283**

Coventry University

7006SCN – Machine Learning and Big Data

---

# Ethical Note

The NYC Yellow Taxi Trip Records dataset is publicly available through the New York City Taxi and Limousine Commission (TLC). The dataset contains operational trip information and does not include personally identifiable information (PII). All data processing, machine learning modelling, scalability experiments, and visualisations were conducted solely for academic purposes.

The project complies with Coventry University academic integrity requirements and ethical data usage principles. Model outputs should be interpreted as analytical results only and must not be used for operational, financial, or regulatory decision-making without further validation.

```
```
