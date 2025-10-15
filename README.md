# Air Pollution Forecasting Prototype 🌍

### Short-Term Forecast of Gaseous Air Pollutants (O₃ and NO₂)
This repository hosts a prototype system for forecasting hourly O₃ and NO₂ concentrations in Delhi using reanalysis meteorological data and satellite-derived trace gases.

---

## 🚀 Objective
Develop an AI/ML-based pipeline for short-term (24–48 hr) surface ozone and NO₂ forecasting using harmonized satellite and reanalysis data.

---

## 🧩 Workflow Overview
1. **Data Preprocessing**
   - Align temporal & spatial data (satellite, meteorology, ground truth)
   - Fill missing satellite data with physics-informed interpolation
   - Compute HCHO/NO₂ ratio and classify photochemical regimes

2. **Feature Engineering**
   - Interaction terms (e.g., O₃×Temp, NO₂×Wind)
   - Regime flags and satellite-derived features

3. **Model Prototype**
   - Baseline: Random Forest Regressor for O₃ and NO₂
   - Future work: Hybrid Quantum + Neural (VQC + LSTM)

---

## 📊 Dataset
- **Source:** Sentinel-5P, ERA5/MERRA-2, CPCB
- **Temporal Coverage:** 2019–2024
- **Resolution:** Hourly
- **Variables:** O₃, NO₂, meteorology, HCHO, NO₂ (satellite)

---

## 🧠 Future Work
- Integrate LSTM and VQC models for time-series learning  
- Deploy via Streamlit dashboard for interactive forecasts

---

## 🛠️ Run Prototype
```bash
pip install -r requirements.txt
jupyter notebook notebooks/03_model_prototype.ipynb