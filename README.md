📊 CGM Prediction

> 🩺 Continuous Glucose Monitoring & Meal Detection using Machine Learning

---

## 🧠 Project Summary

In this project, we develop an **online meal detection system** using Continuous Glucose Monitoring (CGM) data collected over \~6 months (at 5-minute intervals) from a single subject.
You’ll synchronize this sensor data with **meal ground truth logs** and implement **four different algorithms** to detect meal events in real-time.

---

## 🔍 Objective

📈 Detect meals continuously and accurately using physiological data from CGM sensors.

---

## 📋 Tasks Overview

| 🔢 Step | 📌 Task                                                        |
| ------- | -------------------------------------------------------------- |
| 1️⃣     | Parse CGM data and align meal timestamps with glucose readings |
| 2️⃣     | Implement and test four real-time meal detection algorithms    |
| 3️⃣     | Apply trained models to a **new patient**'s data               |
| 4️⃣     | Perform **execution time analysis** for all methods            |

---

## 🛠️ Algorithm Suite

### 🔁 1. Auto Regression-based Detection (SARIMA)

* 📐 **Design** SARIMA model on glucose time-series
* 🔧 **Instantiate** with parameter tuning
* 🧪 **Implement & Evaluate** performance
* 📊 Report training/testing accuracy

---

### 🧠 2. Model-Based Detection (RNN-GRU)

* 🧬 **Develop** GRU-based temporal pattern model
* ⚙️ **Instantiate** recurrent layers with optimal settings
* 🛠️ **Train/Test** with CGM + Meal events
* 📈 Evaluate and log accuracy

---

### 📉 3. Kalman Filter-based Detection

* 📘 **Define** Kalman filter framework
* 🔩 **Instantiate** state-space model
* 🧪 **Apply** to CGM signal dynamics
* 📊 Report detection metrics

---

### 🔄 4. RNN-Based Detection (TensorFlow, LSTM)

* 🧠 **Develop** LSTM model using TensorFlow/Keras
* 🔧 **Tune** layers, memory units
* 🏋️ **Train** on known subjects, **Test** on new data
* 📈 Log metrics (F1, Precision, Recall, Accuracy)

---

## 📁 Project Structure

```
cgm-prediction/
├── data/
│   ├── cgm_readings.csv
│   └── meal_ground_truth.csv
├── models/
│   ├── sarima_model.py
│   ├── gru_model.py
│   ├── kalman_filter.py
│   └── lstm_model.py
├── utils/
│   ├── parser.py
│   └── evaluation.py
├── patient_test/
│   └── new_patient_data.csv
├── results/
│   ├── predictions/
│   └── execution_times/
└── README.md
```

---

## 📊 Example Output (Meal Prediction)

| Time  | Glucose (mg/dL) | Predicted Meal |
| ----- | --------------- | -------------- |
| 08:15 | 95              | ❌              |
| 08:20 | 110             | ✅              |
| 08:25 | 145             | ✅              |
| 08:30 | 140             | ✅              |
| 08:35 | 130             | ❌              |

---

## ⏱️ Execution Time Analysis

Each model will be profiled for:

* 🕐 **Training Time**
* 🚀 **Inference Latency**
* 💡 **Scalability**

---

## 📦 Requirements

* Python 3.7+
* Pandas, NumPy
* scikit-learn
* TensorFlow / Keras
* statsmodels
* matplotlib
* tqdm

Install all dependencies:

```bash
pip install -r requirements.txt
```

---

## 🧪 Testing on New Patient

Use `patient_test/new_patient_data.csv` to evaluate generalization on unseen data.
