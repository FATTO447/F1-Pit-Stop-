# 🏎️ Formula 1 Pit Stop Strategy Engine

An advanced, end-to-end race simulation and strategy dashboard designed to predict the optimal pit stop windows in Formula 1 racing. By combining historical data, predictive modeling, and live telemetry, this project bridges the gap between complex sports analytics and intuitive web design.

https://pit-stop-predictor--hollaftta.replit.app/

---

## 🚀 Project Overview

In Formula 1, tire degradation and pit stop timing dictate the boundary between winning and losing. A wrong call under pressure can ruin an entire weekend. This project implements a hybrid architecture that models tire wear under various track conditions, simulates thousands of race scenarios, and visualizes live telemetry dynamically.

### 🌟 Key Features
* **Predictive Strategy Modeling:** Uses Machine Learning to forecast tire degradation based on compound types (Soft, Medium, Hard) and track temperatures.
* **Monte Carlo Simulations:** Runs **10,000 simulations** per request to calculate the probability distribution of the safest and most efficient pit windows.
* **Dynamic Telemetry Track Mapping:** Dynamically fetches actual $X, Y$ coordinates and speed traces using the `FastF1` API, rendering a dark-mode neon track map that displays driver breaking/acceleration zones.
* **Interactive Dark-Theme UI:** A seamless frontend built with custom HTML/CSS/JS that updates instantly without full page reloads.

---

## 🛠️ Tech Stack & Architecture

### Backend & Data Science
* **Python:** Core programming language.
* **XGBoost:** For predictive tire degradation and stint length classification.
* **FastF1 API:** For extracting real-time and historical telemetry data, speed traces, and lap times.
* **Matplotlib / Seaborn:** For generating the custom speed-coded track layouts and Monte Carlo distribution histograms.

### Frontend
* **HTML5 & CSS3:** For a high-fidelity, custom dark race-wall theme.
* **JavaScript (Fetch API):** Handles dynamic asynchronous backend requests for real-time calculation and visualization rendering.

---

## 📊 How It Works (Pipeline)

1. **Data Ingestion & Cleaning:** Historical race data (2018–2025) is extracted, filtered, and cleaned via specialized processing notebooks.
2. **Feature Engineering:** Stint lengths, compound age, track status, and environmental variables are structured into high-value features.
3. **Simulation:** The backend feeds the user's real-time dashboard inputs (Tire age, target track, driver) into the XGBoost model and wraps it in a Monte Carlo loop.
4. **Dynamic Output:** Results are compiled into a structural JSON object, feeding the frontend with the exact pit window lap, confidence metrics, and custom matplotlib visualizations.

---

## 🔮 Future Roadmap (Active Learning)
As part of my continuous deep-dive into **Deep Learning**, I am currently expanding this engine with the following introductory features:
* **Tyre Compound Selection:** Integrating a multi-class classification model to suggest the next optimal tire compound based on remaining race laps and track position.
* **1D-CNN Telemetry Analysis:** Implementing basic Convolutional Neural Networks to analyze raw continuous telemetry streams to identify subtle vehicle performance drops.

---
