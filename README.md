# Covid_dataset-ML
# COVID Status Prediction App

A machine learning-based web application that predicts a patient's COVID-19 status (Healthy or Diseased) based on clinical and laboratory data. The app is built using Streamlit and powered by a tuned Random Forest model.

**Live App**: [Click here to open]([https://your-streamlit-app-link.streamlit.app](https://cociddataset-ml-sxem7mjegy7wwkegybgavb.streamlit.app/))

---

## Project Overview

This project demonstrates a full machine learning workflow, from data preprocessing and feature engineering to model training, evaluation, and deployment.

The model uses 14 clinical features and 1 engineered feature (`inflammation_index`) to predict the COVID-19 status of a patient.

---

## Features

- Interactive web interface for user input
- Trained Random Forest classifier with optimized hyperparameters
- Feature scaling using `StandardScaler`
- One engineered feature: Inflammation Index (mean of CRP, Ferritin, and LDH)
- Live deployment via Streamlit Cloud

---

## Technologies Used

- Python  
- Streamlit  
- scikit-learn  
- pandas  
- numpy  
- joblib  

---

## Input Features

The model expects the following features as input:

- `age` – Patient's age in years
- `temperature` – Body temperature in degrees Celsius
- `heart_rate` – Heart rate in beats per minute (bpm)
- `respiratory_rate` – Breaths per minute
- `oxygen_saturation` – Blood oxygen saturation percentage
- `wbc_count` – White blood cell count
- `rbc_count` – Red blood cell count
- `hemoglobin` – Hemoglobin level
- `platelet_count` – Platelet count
- `d_dimer` – D-dimer level
- `crp` – C-reactive protein level
- `ferritin` – Ferritin level
- `ldh` – Lactate dehydrogenase level
- `alt` – Alanine transaminase level
- `inflammation_index` – Engineered feature computed as the mean of `crp`, `ferritin`, and `ldh`

---
## File Structure

.
├── app.py                          # Streamlit web application
├── random_forest_covid_model.pkl  # Trained Random Forest model
├── scaler.pkl                     # StandardScaler used for input scaling
├── requirements.txt               # Project dependencies
└── README.md                      # Project documentation

---

## Limitations

- The model was trained on a limited dataset and is intended for educational purposes only.
- Performance may vary on real-world or clinical data.
- Not intended for medical or diagnostic use.

---

## Future Enhancements

- Add batch prediction support via CSV upload.
- Improve visualizations and model explainability (e.g., SHAP).
- Include model confidence intervals and uncertainty estimates.

