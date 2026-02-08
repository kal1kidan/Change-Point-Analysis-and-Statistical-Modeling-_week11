# 📊 Change Point Analysis and Statistical Modeling of Brent Oil Prices

**10 Academy – Artificial Intelligence Mastery**
**Week 11: Time Series Analysis Challenge**
📅 *04 Feb – 10 Feb 2026*

---

## 📌 Project Overview

This project analyzes **Brent crude oil price dynamics** using **time series analysis** and **Bayesian change point detection** to identify structural breaks and relate them to major geopolitical, economic, and policy-driven events.

The analysis is conducted in the context of **Birhan Energies**, a data-driven energy consultancy, to support **investors, policymakers, and energy companies** in understanding market instability and making informed decisions.

**Task 1** lays the analytical foundation by:

* Defining a clear, reproducible data analysis workflow
* Exploring statistical properties of the data
* Compiling and aligning major global events with price movements
* Documenting assumptions, limitations, and communication strategies

---

## 🎯 Objectives

### Overall Project Goals

* Identify key political and economic events impacting Brent oil prices
* Quantify regime shifts using Bayesian change point models
* Translate statistical findings into actionable insights

### Task 1 Objectives

* Define and document the full data analysis workflow
* Perform exploratory and statistical analysis of Brent oil prices
* Prepare data for Bayesian change point modeling
* Compile a structured event dataset (10–15 key events)
* Clearly state assumptions, limitations, and communication channels

---

## 🗂️ Repository Structure

```
.
├── data/
│   ├── raw/                # Original datasets (ignored by Git)
│   └── processed/          # Cleaned and transformed data
│
├── docs/
│   ├── workflow.md         # Explicit Task 1 analysis workflow
│   ├── assumptions.md     # Assumptions & limitations
│   └── events.csv         # Tabular geopolitical & economic events
│
├── notebooks/
│   └── task1_eda.ipynb     # Exploratory Data Analysis (Task 1)
│
├── src/
│   ├── data_loader.py     # Modular data loading & validation
│   ├── preprocessing.py  # Transformations & feature engineering
│   └── utils.py           # Shared utilities & error handling
│
├── backend/               # Flask backend (Task 3)
├── frontend/              # React dashboard (Task 3)
│
├── requirements.txt
└── README.md
```

✔️ **Addresses feedback**: explicit workflow documentation, tabular event dataset, and modular Python code with basic error handling.

---

## 🔁 Data Analysis Workflow (Task 1)

The workflow is fully documented in **`docs/workflow.md`** and implemented as follows:

### 1. Data Loading

* Load historical Brent oil price data
* Parse dates and enforce correct data types
* Validate schema and date continuity

### 2. Data Quality Checks

* Detect missing values and duplicates
* Verify price validity (non-negative, realistic ranges)

### 3. Exploratory Data Analysis (EDA)

* Visualize long-term price trends
* Identify volatility clustering and shocks

### 4. Time Series Transformation

* Compute log returns to stabilize variance
* Prepare data for stationarity testing

### 5. Stationarity Testing

* Apply Augmented Dickey-Fuller (ADF) test
* Confirm suitability for statistical modeling

### 6. Volatility Analysis

* Examine clustering behavior typical of financial time series

### 7. Event Overlay Analysis

* Align geopolitical and economic events with price movements
* Visualize temporal correspondence

### 8. Data Export

* Save cleaned and transformed datasets for modeling and dashboards

---

## 📈 Time Series Properties Analysis

### Trend

* Raw Brent prices exhibit strong long-term trends
* Influenced by macroeconomic conditions, conflicts, and policy shifts
* Non-stationary in price levels

### Stationarity

ADF test applied to log returns:

* **ADF Statistic:** -16.43
* **p-value:** 2.49e-29

✅ Log returns are stationary and suitable for Bayesian modeling.

### Volatility

* Clear volatility clustering observed
* Supports regime-based and change point modeling approaches

---

## 🌍 Event Data Compilation

A structured dataset of major global events was manually researched and compiled.

### Event Categories

* Geopolitical conflicts (e.g., Gulf War, Libya Civil War)
* OPEC production decisions
* Global economic crises (e.g., 2008 Financial Crisis)
* Political upheavals (e.g., Arab Spring)
* Sanctions and policy shifts

### Event Fields

* Event name
* Approximate start date
* Event type/category

📁 **Stored at:** `docs/events.csv`
📊 **Used for:** Visual alignment and hypothesis generation (not causal proof)

---

## 🔍 Change Point Modeling – Conceptual Overview

Change point models identify **structural breaks** in time series data.

In this project, they are used to detect:

* Shifts in mean price behavior
* Market regime changes
* Structural breaks potentially associated with major events

### Expected Outputs

* **τ (tau):** Estimated timing of regime change
* **μ₁, μ₂:** Mean log returns before and after the change
* **Uncertainty:** Credible intervals for timing and magnitude

### Limitations

* Change points may not align exactly with known events
* Temporal correlation ≠ causal impact
* Results are sensitive to model assumptions

---

## ⚠️ Assumptions and Limitations

### Assumptions

* Event start dates are approximate
* Market reactions may be delayed
* Log returns sufficiently capture price dynamics

### Limitations

* Correlation does not imply causation
* External drivers (speculation, FX rates) are not modeled
* Daily prices miss intraday dynamics
* Noise and model priors affect detection sensitivity

📄 Full discussion available in **`docs/assumptions.md`**

---

## 📢 Communication Strategy

Results are communicated through:

* **Technical reports** for analysts and policymakers
* **Interactive dashboards** for investors and energy firms
* **Visual narratives** highlighting regime shifts
* **Plain-language summaries** translating Bayesian results into insights

---

## ✅ Task 1 Deliverables Status

| Requirement                    | Status      |
| ------------------------------ | ----------- |
| Defined analysis workflow      | ✅ Completed |
| Workflow documentation         | ✅ Completed |
| Event dataset (10–15 events)   | ✅ Completed |
| Trend analysis                 | ✅ Completed |
| Stationarity testing           | ✅ Completed |
| Volatility analysis            | ✅ Completed |
| Change point model explanation | ✅ Completed |
| Assumptions & limitations      | ✅ Completed |
| Modular Python code            | ✅ Completed |
| Communication strategy         | ✅ Completed |

---

## 🚀 Next Steps (Task 2 & 3)

### Task 2

* Implement Bayesian change point detection using PyMC
* Quantify regime shifts with posterior distributions
* Associate detected changes with plausible events

### Task 3

* Develop Flask APIs to serve analysis outputs
* Build React dashboards with interactive event overlays
* Enable filtering, drill-downs, and stakeholder exploration

---

## 📚 References

Key references on data science workflows, Bayesian inference, and change point detection are listed in the challenge documentation and were actively used to guide this work.

---
