# Airline Delay Prediction & Big Data Analytics – AWS EMR + Hive + ML

This project analyzes U.S. flight delay patterns using Hive on AWS EMR and builds classification models to predict future delays. It combines big data querying, distributed processing, and machine learning on real-world airline data.

---

## ☁️ Big Data Setup on AWS EMR

- Launched EMR cluster with **Hive, Hadoop, Spark**, and **Jupyter**.
- Transferred `2003.csv`, `airports.csv`, and `carriers.csv` to EMR via `SCP` and `SSH`, then moved them into HDFS.
- Created Hive tables (`flights_2003`, `carriers`, `airports`) and validated schema and ingestion.

---

## 🔍 Hive Querying & Delay Analysis

- Queried cumulative delay time across airports and carriers using HiveQL.
- Identified **ORD**, **ATL**, and **EWR** as top delay-heavy airports.
- Found **Southwest Airlines (WN)** had the most total departure delay hours.
- Analyzed delay types: departure delays (558K hours) > arrival delays (382K hours).

---

## 🧪 Sampling & Feature Engineering

- Used `TABLESAMPLE` to randomly extract 30,000 records from Hive.
- Exported sample to local storage for cleaning in Excel and Python.
- Engineered predictive features: Month, Day, Carrier, Airport Code, and `Delayed` (target label).

---

## 🤖 ML Model Development

- Trained and compared multiple classifiers:
  - **SGD Classifier** (best generalization)
  - **Decision Tree**
  - **K-Nearest Neighbors (KNN)**
- Used `GridSearchCV` with cross-validation for hyperparameter tuning.
- Evaluated models using **Accuracy**, **F1-Score**, and full classification report.

---

## ✅ Outcomes

- Built a full-stack delay risk prediction pipeline from EMR setup to model evaluation.
- **SGD Classifier** provided the best generalization and training performance.
- Demonstrated scalable ML integration with distributed querying for aviation analytics.

---

## 🛠️ Skills Used

**Tools**: AWS EMR, Hive, Hadoop, HDFS, Python, Scikit-learn, SCP, SSH, Excel  
**Techniques**: HiveQL, Sampling, Aggregation, Feature Engineering, Classification Modeling, GridSearchCV  
**Models**: SGD Classifier, Decision Tree, KNN

---

## 📁 Files

- `FlightDelayPhase1` – Project Presentation
- `FlightDelayPhase2` - Project Presentation
- `Finals.ipynb` – Notebook with feature engineering and ML modeling  
- `README.md` – Project documentation
