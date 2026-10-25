# 🏭 Manufacturing Predictive Maintenance System

An end-to-end Machine Learning project for predicting industrial machine failures using sensor data. The system analyzes operational parameters such as temperature, rotational speed, torque, and tool wear to identify potential failures before they occur, helping manufacturers reduce downtime and maintenance costs.

---

## 🚀 Project Overview

Predictive Maintenance is a critical Industry 4.0 application that enables organizations to anticipate equipment failures before they happen.

This project implements:

- Binary Failure Prediction (Failure / No Failure)
- Multi-Class Failure Classification (6 Failure Categories)
- Feature Engineering for Mechanical and Thermal Stress Analysis
- Random Forest and XGBoost Models
- Model Evaluation using Accuracy, F1 Score, Classification Reports, and Confusion Matrices
- Feature Importance Analysis

---

## 📊 Dataset

Dataset Used:
**AI4I 2020 Predictive Maintenance Dataset**

Features include:

- Air Temperature
- Process Temperature
- Rotational Speed (RPM)
- Torque
- Tool Wear
- Product Type

Target Variables:

### Binary Classification

| Class | Meaning |
|---------|---------|
| 0 | No Failure |
| 1 | Failure |

### Multi-Class Classification

| Class | Failure Type |
|---------|---------|
| 0 | Heat Dissipation Failure |
| 1 | No Failure |
| 2 | Overstrain Failure |
| 3 | Power Failure |
| 4 | Random Failure |
| 5 | Tool Wear Failure |

---

## 🛠 Feature Engineering

Additional domain-specific features were created:

### Temperature Difference

```python
Temp_Diff = Process Temperature - Air Temperature
```

Represents thermal imbalance within the machine.

### Mechanical Power

```python
Mechanical_Power = Torque × Rotational Speed
```

Captures machine workload.

### Thermal Stress

```python
Thermal_Stress = Process Temperature × Torque
```

Measures combined thermal and mechanical strain.

### Wear Rate

```python
Wear_Rate = Tool Wear / Rotational Speed
```

Estimates component degradation rate.

---

## 🤖 Models Implemented

### 1. Random Forest Classifier

Used for:

- Multi-Class Failure Prediction
- Feature Importance Analysis

Advantages:

- Robust to noise
- Handles non-linear relationships
- Easy interpretability

---

### 2. XGBoost Classifier

Used for:

- Binary Failure Prediction
- Multi-Class Failure Prediction

Advantages:

- Gradient Boosting
- Better handling of class imbalance
- High predictive performance

---

## 📈 Results

### Binary Classification (Failure Detection)

| Metric | Score |
|----------|----------|
| Accuracy | 97.85% |
| F1 Score | 0.75 |
| Recall (Failure Class) | 90% |

The binary model effectively identifies machine failures while maintaining high overall accuracy.

---

### Multi-Class Classification

| Metric | Score |
|----------|----------|
| Accuracy | 98% |
| Macro F1 Score | 0.65 |

Performance is strongest for:

- Heat Dissipation Failure
- Overstrain Failure
- Power Failure

Rare failure categories remain challenging due to severe class imbalance.

---

## 📊 Feature Importance

Top contributing factors:

1. Mechanical Power
2. Wear Torque
3. Rotational Speed
4. Temperature Difference
5. Thermal Stress

These variables provide the strongest signals for failure prediction.

---

## 🧪 Evaluation Metrics

The following metrics were used:

- Accuracy Score
- Precision
- Recall
- F1 Score
- Classification Report
- Confusion Matrix
- Feature Importance

---

## 💻 Technologies Used

### Programming

- Python

### Data Analysis

- Pandas
- NumPy

### Visualization

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-Learn
- XGBoost
- Random Forest

### Model Persistence

- Joblib
- Pickle

---

## 🎯 Business Impact

A predictive maintenance system can help organizations:

- Reduce unplanned downtime
- Improve equipment reliability
- Lower maintenance costs
- Increase operational efficiency
- Enable proactive maintenance scheduling


## Author : Ashmit Kumar Sahu
