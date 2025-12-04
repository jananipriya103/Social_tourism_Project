# **Tourism Booking Intent Prediction System**

A complete end-to-end Machine Learning application that predicts whether a user will **book** or **not book** on a digital tourism platform based on their behavioural interaction patterns. The system includes separate ML pipelines for **Laptop users** and **Mobile users**, optimized thresholds, and a fully interactive **Streamlit web app** for real-time predictions.

## 🚀 **Project Overview**

Tourism websites collect large volumes of user interaction data, but often fail to identify whether a user intends to complete a booking. This project develops a robust ML-based solution that:

* Predicts *booking intent* using user behaviour features
* Builds **separate ML models for Laptop and Mobile users**
* Uses optimized decision thresholds for higher F1-score and accuracy
* Provides a **Streamlit-based web interface** for real-time predictions
* Helps tourism platforms personalize offers, increase conversions, and reduce drop-offs

## 🎯 **Key Features**

### ✔ **Device-Specific ML Models**

Because user behaviour varies on different devices, the system builds:

* **Laptop Model → KNN (best performer)**
* **Mobile Model → XGBoost (best performer)**

Each model is optimized using ROC/PR analysis and Youden/precision-recall thresholds.

---

### ✔ **Optimized Prediction Thresholds**

Instead of using the default 0.5 threshold, the system computes:

* Best threshold for Laptop users → using Youden's J statistic
* Best threshold for Mobile users → using Precision-Recall F1 optimization

This improves classification performance, especially for imbalanced data.

---

### ✔ **Real-Time Prediction Web App (Streamlit)**

The Streamlit interface allows users to:

* Select device type (Laptop / Mobile)
* Enter 14 user behaviour features
* Generate booking intent probability
* View recommendation messages for conversion

The app loads PKL model files and performs all preprocessing automatically.


## 📊 **Tech Stack**

### **Machine Learning**

* KNN
* XGBoost
* Logistic Regression, Random Forest (evaluated)
* Threshold Optimization (ROC, PR Curve)

### **Preprocessing**

* Scaling (StandardScaler)
* SMOTE (for balancing)
* Manual encoding / numeric transformation

### **Interface**

* **Streamlit** for deployment
* **GitHub + Streamlit Cloud** for hosting
