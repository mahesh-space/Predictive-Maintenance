# Predictive Maintenance of Industrial Machinery

## Overview
This project implements a **predictive maintenance system** that forecasts potential machinery failures using historical sensor data. Built during the **IBM SkillsBuild X Edunet Internship**, it leverages **IBM Cloud AutoAI** to automate model training, optimization, and deployment.

---

## Problem Statement
Industrial machines frequently face unexpected failures, leading to costly downtime and production losses. Traditional preventive maintenance either **over-maintains** machines (increasing costs) or **under-maintains** them (causing breakdowns).  
**Goal:** Predict failure types before they occur using sensor data like temperature, torque, and rotational speed.

---

## Proposed Solution
- Use **historical sensor data** from Kaggle’s Predictive Maintenance dataset.
- Train an **AutoAI classification model** to predict failure type.
- Deploy the best model as a **REST API** using IBM Watson Machine Learning.
- Provide actionable insights for maintenance teams to reduce downtime and costs.

---

## Dataset
- **Source:** [Kaggle Predictive Maintenance Classification Dataset](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification)  
- **Features:**
  - Air temperature (K)  
  - Process temperature (K)  
  - Rotational speed (rpm)  
  - Torque (Nm)  
  - Tool wear (min)  
- **Target:** Failure Type (multi-class: Heat Dissipation, Tool Wear, Power Failure, etc.)

---

## Technologies Used
- **IBM Cloud Services:**
  - Watson Studio (AutoAI)
  - Watson Machine Learning
  - Cloud Object Storage
- **Programming:** Python (for optional EDA & API testing)
- **Deployment:** REST API Endpoint via WML

---

## Project Workflow
1. Upload dataset to **IBM Cloud Object Storage**.
2. Create an **AutoAI experiment** in Watson Studio.
3. Select **classification task** and target column (`Failure Type`).
4. AutoAI generates multiple pipelines; select **highest accuracy** (99.5%).
5. Save and deploy the best pipeline using **Watson Machine Learning**.
6. Test the API with sample JSON sensor data for predictions.

---

## Results
- **Best Model:** Batched Tree Ensemble Classifier (Snap Random Forest)  
- **Accuracy (Cross Validation):** 99.5%  
- Confusion matrix and leaderboard screenshots included in the presentation.

---

## Future Enhancements
- Integrate **real-time IoT sensor streaming** for continuous predictions.
- Add **explainable AI (SHAP)** for feature importance.
- Expand model for **multiple machine types** and **predict remaining useful life (RUL)**.

---

## Acknowledgment
Special thanks to **Edunet Foundation** and **IBM SkillsBuild** for providing this internship opportunity, which helped in gaining hands-on skills in AI, cloud deployment, and project execution.

---

## Author
**Mahesh Gurjar**  
National Institute of Electronics and Information Technology, Ajmer – CSE
