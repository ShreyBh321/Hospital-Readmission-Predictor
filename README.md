
## 🏥 Healthcare Predictive Analytics: Hospital Readmission Analysis

### 📌 Project Overview

This project focuses on analyzing and predicting **hospital readmissions** using a combination of **SQL, Exploratory Data Analysis (EDA), and Machine Learning**.

The goal is to identify **high-risk patients** and provide **actionable insights** to reduce readmission rates and improve patient care.

---

## 🎯 Business Problem

Hospital readmissions within 30 days are:

* Costly for healthcare providers
* Indicators of poor post-discharge care
* A key metric for hospital performance

👉 This project aims to:

* Predict **which patients are likely to be readmitted**
* Identify **key drivers of readmission**
* Help stakeholders take **preventive actions**

---

## 📊 Dataset Description

The dataset contains **100,000+ patient records** with both **numerical and categorical features**:

### 🔹 Key Features:

* **Demographics:** age, gender, race
* **Hospital Utilization:**

  * `time_in_hospital`
  * `number_inpatient`
  * `number_emergency`
* **Medical Data:**

  * `diag_1`, `diag_2`, `diag_3`
  * `A1Cresult`, `max_glu_serum`
* **Medications:** insulin, metformin, etc.
* **Target Variable:** `readmitted` (<30, >30, NO)

---

## 🧠 Project Pipeline

```
Data Cleaning → Feature Engineering → Encoding → EDA → SQL Analysis → Model Building → Evaluation → Dashboard
```

---

## 🔍 Exploratory Data Analysis (EDA)

### Key Insights:

* Patients with **more inpatient visits** have higher readmission risk
* **Longer hospital stays** increase probability of readmission
* **Medication changes (insulin)** indicate unstable conditions
* Higher number of medications → increased risk

---

## 🗄️ SQL Analysis

SQL was used to identify **high-risk patient segments** and derive business insights.

### 🔥 Key Findings:

* Frequent inpatient visits → **highest risk**
* Longer hospital stays → **higher readmission**
* Insulin changes → **critical risk indicator**
* Certain diagnoses → **higher readmission rates**

---

## 🤖 Machine Learning Model

### Models Used:

* Logistic Regression (Baseline)
* Random Forest (Final Model)

### Why Random Forest?

* Handles **non-linear relationships**
* Works well with **mixed data types**
* Provides **feature importance**

---

## ⚖️ Handling Class Imbalance

* Used `class_weight = 'balanced'`
* Adjusted threshold to **0.3**

👉 Result:

* Recall improved from **13% → 74% 🚀**

---

## 📈 Model Performance

| Metric    | Value               |
| --------- | ------------------- |
| Accuracy  | ~56%                |
| Recall    | **~74% (Priority)** |
| Precision | ~43%                |
| ROC-AUC   | ~65%                |

---

## 📊 Key Features Driving Readmission

* `number_inpatient`
* `time_in_hospital`
* `num_medications`
* `insulin`
* `A1Cresult`

---

### Key Components:

* KPI Cards (Total Patients, Readmission Rate)
* Readmission by Age Group
* Hospital Utilization Analysis
* Medication Impact (Insulin)
* High-Risk Patient Segmentation

---

## 🚨 High-Risk Patient Definition

Patients with:

* `number_inpatient > 2`
* `time_in_hospital > 5`
* Insulin changes (Up/Down)

👉 These patients require **immediate intervention**

---

## 💡 Business Impact

* Identify **high-risk patients early**
* Improve **discharge planning**
* Reduce **hospital costs**
* Enhance **patient care quality**

---

## 🤖 Use of AI Tools

AI tools were used to:

* Accelerate data preprocessing
* Suggest optimal ML models
* Improve debugging and efficiency
* Assist in dashboard design

---
