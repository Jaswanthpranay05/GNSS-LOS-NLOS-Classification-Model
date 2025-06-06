# 📡 GNSS LOS/NLOS Signal Classification using Machine Learning

This project aims to accurately classify Global Navigation Satellite System (GNSS) signals as **Line-of-Sight (LOS)** or **Non-Line-of-Sight (NLOS)** using machine learning techniques. We use real-world GNSS features such as SNR, Elevation, and Azimuth, and train an XGBoost model to distinguish between LOS and NLOS conditions with high accuracy.

## 📖 Table of Contents
1. [Introduction](#introduction)
2. [Libraries and Tools](#libraries-and-tools)
3. [Methodology](#methodology)
4. [Model: XGBoost](#model-xgboost)
5. [Results](#results)
6. [Insights & Evaluation](#insights--evaluation)
7. [Future Enhancements](#future-enhancements)
8. [Conclusion](#conclusion)

## Introduction

Global Navigation Satellite Systems (GNSS) such as GPS, NavIC, Galileo, and GLONASS are essential for precise positioning and navigation. However, accuracy is heavily influenced by whether the satellite signal is received as:

- **LOS (Line of Sight)** – direct and accurate
- **NLOS (Non-Line of Sight)** – obstructed, reflected, or scattered leading to errors

Correct classification of these signals is crucial in improving GNSS-based applications like autonomous vehicles and smart navigation systems.

## Libraries and Tools

| Library        | Purpose                                      |
|----------------|----------------------------------------------|
| Pandas         | Data loading and preprocessing               |
| NumPy          | Numerical computations                       |
| Matplotlib     | Data and confusion matrix visualization      |
| Seaborn        | Enhanced heatmap visuals                     |
| Scikit-learn   | Preprocessing and model evaluation           |
| XGBoost        | Gradient boosting classifier                 |
| OS             | File management for exports                  |

## 📊 Methodology

### ✅ Step-by-Step Pipeline:
1. **Data Collection** – Separate datasets for LOS and NLOS with signal parameters.
2. **Data Preprocessing**
   - Removal of non-essential columns (e.g., PRN)
   - Label encoding (0 = LOS, 1 = NLOS)
   - Feature scaling using `StandardScaler`
3. **Feature Selection**
   - **SNR**, **Elevation**, **Azimuth** chosen for their relevance to signal quality
4. **Model Training**
   - XGBoost Classifier trained on 80% of the data
5. **Model Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1-Score
   - Confusion matrix visualized and saved
6. **Results Export**
   - Evaluation results and confusion matrix saved to CSV

## ⚙️ Model: XGBoost

XGBoost (Extreme Gradient Boosting) is used due to:
- High performance on tabular data
- Ability to handle missing/non-linear patterns
- In-built regularization to reduce overfitting

## Results

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 1.00  |
| Precision | 1.00  |
| Recall    | 1.00  |
| F1-Score  | 1.00  |
