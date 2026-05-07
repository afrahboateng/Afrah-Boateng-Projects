# 🌊 Hydrology ML: River Forecasting Project

This project builds a repeatable machine learning pipeline for river discharge forecasting using USGS hydrology data and nearby airport weather data (NOAA / METAR).

The goal is to compare how well models generalize across major river systems.

This project includes 

1. a code that builds and tunes a deep learning model
2. deploys the model on data given user inputs
3. returns a dashboard with forecasted streamflow

*Next Step: Get datasets a new river based on info below and current code and plug it into the website!

To Launch the Website:
1. Open terminal to where the water_dashboard.py lives
   cd "/Users/afrahboateng/Documents/DATASCI 207 Applied Machine Learning/Water Project/Coninuation"
2. Activate your environment: conda activate water_dashboard
3. Run streamlit: streamlit run water_dashboard.py
   You should see a link like Local URL: http://localhost:8501 and it should automatically open in your browser


---

# 📍 River + Airport Dataset Pairs

## Colorado River (USA)
Major western U.S. river system.

Used for drought and reservoir analysis.

USGS gauges:
- Lees Ferry
- Glen Canyon Dam

Nearby airports:
- Las Vegas (LAS)
- Phoenix (PHX)

---

## Mississippi River (USA)
Largest river system in North America.

High flood variability and large discharge range.

USGS gauges:
- St. Louis
- Baton Rouge

Nearby airport:
- St. Louis (STL)

---

## Hudson River (USA)
Urban + tidal river system.

Strong sensitivity to rainfall and city runoff.

USGS gauges:
- Albany
- Poughkeepsie

Nearby airports:
- JFK
- LGA
- Newark (EWR)

---

## River Thames (UK)
Major urban river system through London.

Strong rainfall-runoff and tidal effects.

USGS-equivalent gauges:
- Kingston
- Teddington

Nearby airport:
- Heathrow (LHR)

---

## Rhine River (Europe)
Large alpine and industrial river system.

Mix of snowmelt and regulated flow.

USGS-equivalent gauges:
- Cologne
- Basel

Nearby airport:
- Frankfurt (FRA)

---

# ⚙️ Pipeline Overview

- USGS river discharge data
- NOAA / METAR airport weather data
- Time-aligned hourly datasets
- Feature engineering:
  - lagged flow values
  - rolling rainfall sums
  - temperature and humidity lags

---

# 🤖 Models

- Baseline persistence model
- LSTM time series model
- GRU time series model

---

# 📊 Evaluation

- RMSE / MAE
- Error histograms
- Box plots of residuals
- Baseline vs neural network comparison

---

# 🎯 Objective

Build a reusable forecasting system.

Compare model performance across multiple river basins.

Understand how geography and climate affect prediction accuracy.

Test whether one model generalizes across all rivers or needs basin-specific tuning.
