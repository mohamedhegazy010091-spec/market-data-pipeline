# Market Data Pipeline (Stocks, Crypto & Forex)

## 📌 Project Description

This project demonstrates how to build a **simple, end-to-end market data pipeline** using Python.
The focus is on **data engineering fundamentals** rather than complex modeling or automation.

The pipeline covers the full lifecycle of market data:
from **data ingestion** to **cleaning, transformation, analysis, visualization, and reporting**.

This project is designed to show how raw financial data can be transformed into a clean,
structured, and analyzable format using clear and beginner-friendly logic.

---

## 🎯 Project Objective

The main objective of this project is to:

* Build a **foundational data pipeline**
* Apply consistent data structures across multiple asset classes
* Perform basic feature engineering and anomaly detection
* Produce clean analytical outputs suitable for further modeling or strategy development

---

## 📊 Data Sources & Assets

### Market Data Source

* Yahoo Finance (via `yfinance` Python library)

### Asset Classes Covered

**Equities & Indices**

* NIFTY 50
* Bank Nifty
* Selected Indian stocks

**Cryptocurrency**

* Bitcoin (BTC)
* Ethereum (ETH)

**Forex**

* EUR/USD
* USD/JPY

---

## 🧱 Pipeline Design

The project follows a **batch-based data pipeline architecture**:

### 1. Data Ingestion

* Historical market data downloaded programmatically
* Two-year rolling time window
* Unified download logic across assets

### 2. Data Structuring

All datasets are normalized into a single schema:

* Date
* Open
* High
* Low
* Close
* Volume
* Symbol
* Asset_Type

This ensures consistency and simplifies downstream analysis.

---

### 3. Data Cleaning & Validation

* Fixed index and header issues
* Converted date columns to proper datetime format
* Removed missing and inconsistent records
* Ensured consistent data types across datasets

---

### 4. Feature Engineering

Basic analytical features were added, including:

* Daily returns
* Moving averages
* RSI
* Volume-based metrics

These features serve as inputs for exploratory analysis and anomaly detection.

---

### 5. Anomaly Detection (Rule-Based)

Simple rule-based logic was used to detect unusual market behavior:

* Volume anomalies using a 3× average volume threshold
* Price spikes using daily return thresholds
* Combined anomalies (price + volume)

This approach demonstrates how anomalies can be flagged without machine learning.

---

### 6. Visualization

Clear and interpretable charts were generated:

* Price trends
* Technical indicators
* Volume anomaly highlighting

These visualizations help validate data quality and analytical results.

---

### 7. Outputs & Reporting

* Cleaned datasets ready for analysis
* Separate anomaly tables
* Visual outputs suitable for reporting or presentations

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* yFinance
* Jupyter Notebook

---
## 📁 Project Structure

```
market-data-pipeline/
│
├── Day_2_Stock_Data/
│   ├── Day_2_Stock_Data_Collection.ipynb
│   ├── BankNifty_1000_Sessions.csv
│   └── Sensex_1000_Sessions.csv
│
├── Day_3_Crypto_Forex_Data/
│   └── Day_3_Crypto_Forex_Data_Collection.ipynb
│
├── Day_4_Cleaned_Data/
│   └── Day_4_Data_Cleaning_&_Validation.ipynb
│
├── notebooks/
│   ├── Day_5_Basic_Technical_Analysis.ipynb
│   ├── Day_6_Anomaly_Detection_Prep.ipynb
│   ├── day1_api_connectivity.ipynb
│   └── banknifty_sensex_opening_data.ipynb
│
├── reports/
│   ├── Day_2_StockData_Verification_Report.pdf
│   └── Day_2_StockData_Verification_Report.pbix
│
├── data_exports/
│   └── Day_2_Stock_Data.rar
│
├── .gitignore
├── app.log
├── requirements.txt
└── README.md
```

---

### 📌 Folder Description

* **Day_2_Stock_Data/**
  Stock market data collection notebooks and exported CSV files.

* **Day_3_Crypto_Forex_Data/**
  Cryptocurrency and forex historical data collection.

* **Day_4_Cleaned_Data/**
  Cleaned and validated datasets with consistent structure.

* **notebooks/**
  Technical analysis, anomaly detection, and utility notebooks.

* **reports/**
  PDF and Power BI reports used for validation and documentation.

* **data_exports/**
  Archived data outputs for sharing or backup.

* **requirements.txt**
  Python dependencies required to run the project.

* **app.log**
  Execution logs generated during data processing.

---

## 🧠 Notes

* The project follows a **step-by-step data pipeline approach**
* Each folder represents a logical stage in the pipeline
* The structure prioritizes clarity and learning over automation

---

## 🎯 Purpose of This Structure

This layout is designed to clearly demonstrate how a simple
market data pipeline can be built incrementally, from raw data
collection to cleaned datasets, analysis, and reporting.


---

## ⚠️ Limitations

* Data sourced from public APIs (not exchange-grade)
* Pipeline is batch-based, not real-time
* Anomaly detection is threshold-based
* Designed for learning and foundational demonstration

---

## 🚀 Future Improvements

* Automate execution using scheduling tools
* Store data in a database or data lake
* Add statistical or ML-based anomaly detection
* Integrate real-time market feeds
* Extend pipeline monitoring and logging

---

## 👤 Author

**Mohamed Hegazy**
Data Analyst
