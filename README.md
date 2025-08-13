# Brent Oil Prices Time Series Analysis

## Overview

This project provides a full-stack solution for analyzing Brent oil prices, detecting structural changes, and visualizing results interactively. It combines Python-based data science (EDA, change point detection, modeling) with a Flask backend API and a React dashboard frontend.

---

## Project Structure

- **data/**: Raw and processed datasets (`BrentOilPrices.csv`, `oil_market_key_events.csv`)
- **notebook/**: Jupyter notebooks for EDA and change point analysis (`EDA.ipynb`, `changePointAnalysis.ipynb`, `BCPM.ipynb`)
- **src/**: Python modules for preprocessing, statistical analysis, and event annotation
- **backend/**: Flask API serving time series, change points, and event data
- **dashboard/**: React app for interactive visualization and exploration

---

## Key Features

### 1. Data Analysis & Modeling

- **Exploratory Data Analysis (EDA)**: Notebooks and scripts for trend, stationarity, and volatility analysis.
- **Change Point Detection**: Bayesian and classical (e.g., CUSUM, PELT) methods to identify structural breaks.
- **Event Annotation**: Major geopolitical and economic events are mapped to the time series for context.
- **Statistical Modeling**: ARIMA, GARCH, and other models for forecasting and volatility analysis.

### 2. Backend API (Flask)

- `/api/brent-oil-data`: Returns Brent oil price time series (dates, prices)
- `/api/change-points`: Returns detected change points
- `/api/events`: Returns key oil market events (date, description, type)

### 3. Interactive Dashboard (React)

- **Time Series Visualization**: Line chart of Brent oil prices with overlaid change points and event annotations.
- **Change Point Details**: Clickable change points show event descriptions and quantitative impacts.
- **Model Results**: Posterior distributions and parameter shifts visualized.
- **Interactive Controls**: Filter by date range and event type.
- **Responsive UI**: Built with React, Chart.js, and Bootstrap.

---

## How to Run

### 1. Data Preparation

- Place `BrentOilPrices.csv` and `oil_market_key_events.csv` in the `data/` directory.

### 2. Backend (Flask API)

```bash
cd backend
pip install -r requirements.txt  # Ensure Flask, pandas, etc. are installed
flask run
```

### 3. Frontend (React Dashboard)

```bash
cd dashboard
npm install
npm start
```

### 4. Notebooks

- Open and run notebooks in `notebook/` for EDA and modeling.

---

## Assumptions and Limitations

- Statistical correlation does not imply causation; interpret results with caution.
- Change point models identify structural breaks but may not capture all market dynamics.
- Data quality and event selection impact analysis validity.

---

## References

- [PyMC3 Documentation](https://docs.pymc.io/)
- [Time Series Analysis Texts]
- [Brent Oil Market Reports]

---

## Communication

- Results are communicated via interactive dashboards, notebooks, and reports.
