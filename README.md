# 🌍 Analyzing the Impact of Urban Air Quality on Public Health
### A Data Mining & Machine Learning Approach (Group 09)

## 📌 Project Overview
Urban air pollution is a major public health concern linked to respiratory and cardiovascular diseases.  
This project predicts a **continuous Health_Risk_Score** using environmental and weather variables through **data mining + machine learning**.

## 🎯 Objectives
- Understand how air-quality/weather factors impact public health risk
- Build predictive models for **Health_Risk_Score**
- Compare models using **Average Squared Error (ASE)**
- Identify key drivers and provide actionable public-health recommendations

## 📊 Dataset
**Urban Air Quality and Health Impact Analysis** dataset with **46 variables** including:
- **Target:** `Health_Risk_Score` (continuous)
- **Predictors:** Heat Index, Humidity, Dew Point, Wind Speed, Pressure, UV Index, Solar Radiation, City, Conditions, etc.

## 🧹 Data Preparation
- Removed non-informative (all-zero) variables during import
- Handled missing values (class vars) using **Tree Surrogate Imputation**
- Detected outliers via box plots; applied imputation/transformation where needed
- Applied transformations for slightly skewed variables (where helpful for regression/NN)
- **Data Split:** 60% Train / 20% Validation / 20% Test

## 🤖 Models Implemented
1. **Linear Regression**
   - Baseline model
   - Stepwise selection to keep significant predictors
2. **Decision Tree**
   - Two tree structures tested
   - Model 2 preferred (three-way splits, more leaves)
3. **Random Forest**
   - Ensemble model to reduce overfitting and improve stability
4. **Auto Neural Network**
   - Captures non-linear relationships (less interpretable)

## 🏆 Model Comparison (ASE)
| Model | Validation ASE | Notes |
|------|----------------:|------|
| **Stepwise Linear Regression (Reg5)** | **~0.013** | ✅ Best accuracy + interpretability |
| Random Forest | ~0.021–0.025 | Strong performance, more complex |
| Decision Tree (Model 2) | ~0.0267 | Captures complex patterns |
| Decision Tree (Model 1) | ~0.0285 | Simpler tree |
| Auto Neural Network | ~0.45 | Higher error vs others |

## 🔍 Key Findings
- **Heat Index + Humidity/Dew** are major drivers of **Health_Risk_Score**
- **City** plays a role (geographic variation in health-risk profiles)
- Monitoring heat + moisture conditions can help manage urban health risk proactively

## 💡 Business / Policy Recommendations
- Enable **real-time public health alerts** during high-risk periods
- Use predictions to guide **resource allocation** (cooling centers, air purifiers)
- Run **targeted prevention campaigns** for vulnerable populations
- Support **urban planning** initiatives (green zones, zoning decisions)
- Help hospitals plan for increased demand during pollution spikes

## 🛠 Tools & Tech
- **SAS Enterprise Miner**
- Modeling: Linear Regression, Decision Tree, Random Forest, Auto Neural Network

## 🔮 Future Work
- Add real-time pollutant feeds + more cities
- Expand target outcomes (hospitalization/respiratory events)
- Deploy as an early-warning risk system for public health agencies

## 📄 Project Report
➡️ [View the full report (PDF)](docs/DSCI5240_FinalProject.pdf)

