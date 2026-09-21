\# CashLens — ML \& Data



This folder contains the machine learning and data pipeline for CashLens, a GST and cash-flow credit-readiness copilot for Indian MSMEs.



\## ML Responsibilities



The ML module is responsible for:



1\. Cash-flow forecasting

2\. Credit-readiness scoring

3\. Transaction categorization

4\. Anomaly detection

5\. SHAP-based model explainability



\## ML Pipeline



```text

Raw Financial Data

&#x20;       ↓

Data Cleaning \& Preprocessing

&#x20;       ↓

Feature Engineering

&#x20;       ↓

ML Models

&#x20;       ↓

Forecast + Credit Score + Categories + Anomalies

&#x20;       ↓

SHAP Explainability

&#x20;       ↓

Structured Output for GenAI Agent

```



\## Models



\### 1. Cash-Flow Forecasting



\* Primary model: LightGBM

\* Baseline: Prophet

\* Forecast horizon: 30, 60 and 90 days

\* Evaluation: MAPE, sMAPE and directional accuracy



\### 2. Credit-Readiness Scoring



\* Models: LightGBM / XGBoost

\* Output: probability-based credit-readiness score

\* Evaluation: ROC-AUC, PR-AUC, F1 and calibration



\### 3. Transaction Categorization



\* Classification of bank/UPI transaction descriptions into spending categories

\* Evaluation: Macro-F1



\### 4. Anomaly Detection



\* Isolation Forest

\* Statistical z-score based detection



\### 5. Explainability



\* SHAP-based explanation of credit-readiness predictions

\* Important factors are passed as structured data to the GenAI layer



\## Data



Development and demonstration will use synthetic, sandbox and permitted public datasets. Real production financial data is not used.



\## Folder Structure



```text

ml/

├── data/

├── notebooks/

├── src/

│   ├── preprocessing/

│   ├── features/

│   ├── forecasting/

│   ├── scoring/

│   ├── categorization/

│   ├── anomaly\_detection/

│   └── explainability/

├── models/

├── evaluation/

├── requirements.txt

└── README.md

```



