# Brent Oil Prices Time Series Analysis

## Project Objectives

This project aims to analyze Brent oil prices using advanced time series techniques to extract statistically valid insights relevant to business objectives. The analysis is structured into the following sub-objectives:

- **Defining the data analysis workflow**
- **Understanding the model and data**
- **Extracting statistically valid insights in relation to the business objective**

## Task 1: Laying the Foundation for Analysis

### Defining the Data Analysis Workflow
- Outline the steps and processes for analyzing Brent oil prices data.
- Research and compile major geopolitical events, OPEC decisions, and economic shocks relevant to the oil market. A structured dataset of 10-15 key events with start dates is included.
- State assumptions and limitations, including the distinction between statistical correlation and causal impact.
- Identify main media channels and formats for communicating results to stakeholders.

### Understanding the Model and Data
- Review key references to understand the concepts and models used.
- Analyze time series properties (trend, stationarity) and discuss their impact on modeling choices.
- Explain the purpose of change point models for identifying structural breaks in price data.
- Describe expected outputs of change point analysis (e.g., change dates, new parameter values) and limitations.

## Task 2: Change Point Modeling and Insight Generation

### Part 2.1: Core Analysis
- Implement Bayesian Change Point detection using PyMC3 to identify structural breaks in Brent oil prices.
- Interpret model output to determine significant change dates (e.g., changes in mean price or volatility).
- Compare detected change points with key events and hypothesize causal relationships.
- Quantify the impact of major change points, e.g., "Following the OPEC production cut announcement around [Date], the average daily price shifted from $X to $Y, an increase of Z%."

### Part 2.2: Advanced Extensions (Optional)
- Discuss incorporating other data sources (GDP, inflation, exchange rates) for a comprehensive model.
- Mention advanced models (VAR, Markov-Switching) for further insights into oil price dynamics.

### Suggested Workflow for Task 2
- **Data Preparation and EDA:**
  - Load and preprocess data, convert dates, plot price series, and analyze log returns for stationarity and volatility clustering.
- **Bayesian Change Point Model (PyMC3):**
  - Define switch point (tau) and "before/after" parameters.
  - Use switch function to model parameter changes.
  - Define likelihood and run MCMC sampling.
- **Interpreting Output:**
  - Check model convergence (r_hat, trace plots).
  - Plot posterior distribution of change point.
  - Quantify impact using posterior distributions of parameters.

## Task 3: Interactive Dashboard for Data Analysis Results

Build a dashboard application using Flask (backend) and React (frontend) to visualize analysis results and help stakeholders explore the impact of events on Brent oil prices.

### Key Components
- **Backend (Flask):**
  - Serve analysis results via APIs.
  - Handle requests for datasets, model outputs, and metrics.
  - (Optional) Integrate real-time data sources.
- **Frontend (React):**
  - User-friendly interface for displaying results.
  - Interactive visualizations (Recharts, React Chart.js 2, D3.js).
  - Features: filters, date ranges, event highlights, comparisons, and responsive design.

### Key Features
- Present historical trends, forecasts, and event correlations.
- Visualize how specific events influenced prices (event highlights).
- Enable filtering, date selection, and drill-down for deeper insights.
- Display key indicators (volatility, average price changes around events).

## Assumptions and Limitations
- Statistical correlation does not imply causation; results should be interpreted with caution.
- Change point models identify structural breaks but may not capture all market dynamics.
- Data quality and event selection impact analysis validity.

## References
- [PyMC3 Documentation](https://docs.pymc.io/)
- [Time Series Analysis Texts]
- [Brent Oil Market Reports]

## Communication Channels
- Results will be communicated via interactive dashboards, reports, and presentations tailored to stakeholders.

---

For more details, see the `notebook/EDA.ipynb` and `data/` directory for datasets and exploratory analysis.
