# 🚗 Used Cars Pricing MLOps Pipeline

This repository contains an end-to-end MLOps pipeline for predicting used car prices, designed for an automobile dealership in Las Vegas. The pipeline automates data preparation, model training, evaluation, registration, and CI/CD deployment using Azure Machine Learning and GitHub Actions.

---

## 📌 Problem Statement

Problem Statement:
An automobile dealership in Los Vegas specializes in selling luxury and non-luxury vehicles. They cater to diverse customer preferences with varying vehicle specifications, such as mileage, engine capacity, and seating capacity. However, the dealership faces significant challenges in maintaining consistency and efficiency across its pricing strategy due to reliance on manual processes and disconnected systems. Pricing evaluations are prone to errors, updates are delayed, and scaling operations are difficult as demand grows. These inefficiencies impact revenue and customer trust. Recognizing the need for a reliable and scalable solution, the dealership is seeking to implement a unified system that ensures seamless integration of data-driven pricing decisions, adaptability to changing market conditions, and operational efficiency.

---

## 🎯 Objective

The dealership has hired you as an MLOps Engineer to design and implement an MLOps pipeline that automates the pricing workflow. This pipeline will encompass data cleaning, preprocessing, transformation, model building, training, evaluation, and registration with CI/CD capabilities to ensure continuous integration and delivery. Your role is to overcome challenges such as integrating disparate data sources, maintaining consistent model performance, and enabling scalable, automated updates to meet evolving business needs. The expected outcomes are a robust, automated system that improves pricing accuracy, operational efficiency, and scalability, driving increased profitability and customer satisfaction.

---

## 📊 Dataset Description

| Feature             | Description                                      |
|---------------------|--------------------------------------------------|
| Segment             | Luxury or non-luxury vehicle classification      |
| Kilometers_Driven   | Total kilometers driven                          |
| Mileage             | Fuel efficiency (km/l)                           |
| Engine              | Engine capacity (cc)                             |
| Power               | Engine power (BHP)                               |
| Seats               | Number of seats                                  |
| Price               | Vehicle price in lakhs (₹100,000 units)          |

---

## 🧪 Pipeline Components

1. **Data Preparation** (`prepare.py`)  
   - Reads raw CSV  
   - Splits into train/test  
   - Writes outputs and diagnostics

2. **Model Training** (`train_model.py`)  
   - Trains Random Forest Regressor  
   - Logs MSE in MLflow  
   - Saves model as MLflow artifact

3. **Model Registration** (`model_register.py`)  
   - Loads best model  
   - Registers in MLflow registry

4. **End-to-End Workflow** (`pipeline_definition.py`)  
   - Assembles all steps into a unified pipeline  
   - Executes in AzureML Studio

---

## ⚙️ Technologies Used

- Azure Machine Learning  
- MLflow  
- GitHub Actions  
- Python (pandas, scikit-learn)  
- YAML for CI/CD workflows

---

## 🚀 How to Run

1. Clone the repo  
2. Configure AzureML workspace  
3. Run `prepare.py` locally or via AzureML  
4. Submit training and registration jobs  
5. Trigger GitHub Actions workflow for CI/CD

---

## 📂 Folder Structure

