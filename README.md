📊 Change Point Analysis and Statistical Modeling of Brent Oil Prices
Week 11 – Time Series Analysis Project

📌 Project Overview
This project focuses on analyzing Brent crude oil price movements using time series analysis and change point detection techniques.
The goal is to understand how major geopolitical events, economic shocks, and OPEC decisions relate to structural changes in oil prices over time.

Task 1 establishes the analytical foundation by exploring the data, defining the workflow, and preparing inputs for advanced modeling in later tasks.

🎯 Objective (Task 1)
The objective of Task 1 is to:

Define a clear data analysis workflow
Understand the statistical properties of Brent oil prices
Compile and align key global events with price movements
Establish assumptions, limitations, and communication strategies
Prepare the data for change point modeling
🗂️ Project Structure
. ├── data/ │ ├── raw/ # Original datasets (ignored by Git) │ └── processed/ # Cleaned and transformed data | └── events.csv # Key geopolitical & economic events ├── notebooks/ │ └── task1_eda.ipynb # Exploratory Data Analysis (Task 1) ├── docs/ │ ├── backend/ # Reserved for later tasks ├── frontend/ # Reserved for dashboard ├── README.md └── requirements.txt

🔁 Data Analysis Workflow
The workflow implemented in Task 1 includes:

Data Loading

Load historical Brent oil price data
Parse date fields and validate data types
Data Quality Checks

Check for missing values and duplicates
Verify date continuity and price validity
Exploratory Data Analysis (EDA)

Visualize price trends over time
Identify long-term trends and volatility clustering
Time Series Transformation

Compute log returns to stabilize variance
Prepare data for stationarity testing
Stationarity Testing

Apply Augmented Dickey-Fuller (ADF) test
Confirm stationarity of log returns
Volatility Analysis

Identify volatility clustering typical of financial time series
Event Overlay Analysis

Compile key geopolitical and economic events
Visualize events alongside price movements
Data Export

Save cleaned and transformed datasets for later modeling
📈 Time Series Properties Analysis
Trend
Raw Brent prices show long-term trends influenced by macroeconomic and political factors.
Non-stationarity is present in price levels.
Stationarity
Log returns were tested with the ADF test:
ADF Statistic: -16.43 p-value: 2.49e-29

✅ Result: Log returns are stationary and suitable for modeling.

Volatility
High and low volatility periods are clustered.
Supports the use of change point detection to capture regime changes.
🌍 Event Data Compilation
A structured dataset of major global events was created, including:

Geopolitical conflicts (e.g., Gulf War, Libya Civil War)
OPEC production decisions
Global economic crises (e.g., 2008 Financial Crisis)
Political upheavals (e.g., Arab Spring)
Each event contains:

Event name
Approximate start date
Event type
📁 Stored as: docs/events.csv
📊 Used to visually align events with price movements

🔍 Change Point Models – Conceptual Overview
Change point models identify structural breaks in time series data.
In Brent oil prices, they help detect:

Sudden shifts in average prices
Market regime changes
Structural breaks caused by geopolitical or economic events
Expected Outputs:

Change point (τ): Estimated time index of structural break
Segment parameters (μ₁, μ₂): Mean log returns before and after τ
Uncertainty: Credible intervals showing confidence in timing and magnitude
Limitations:

Detected change points may not perfectly align with known events
Correlation does not imply causation
⚠️ Assumptions and Limitations
Assumptions
Event start dates are approximate
Market reactions may be delayed
Log returns adequately capture price dynamics
Limitations
Correlation ≠ Causation: Temporal alignment does not prove causality
External factors (e.g., speculation, exchange rates) may influence prices
Sensitivity to noise and parameter choices
Daily prices may not capture intraday dynamics
📢 Communication Strategy
Results from Task 1 will be communicated via:

Technical reports for analysts and policymakers
Interactive dashboards for investors and energy companies
Visualizations highlighting change points and event associations
Narrative summaries translating statistical findings into actionable insights
✅ Task 1 Deliverables Status
Requirement	Status
Defined analysis workflow	✅ Completed
Event dataset (10–15 events)	✅ Completed
Trend analysis	✅ Completed
Stationarity testing	✅ Completed
Volatility analysis	✅ Completed
Change point model explanation	✅ Completed
Assumptions & limitations	✅ Completed
Communication channels	✅ Completed
🚀 Next Steps (Task 2 & Beyond)
Implement Bayesian change point detection models
Quantify regime shifts in oil prices
Evaluate event impact using probabilistic methods
Build interactive dashboards for stakeholders
