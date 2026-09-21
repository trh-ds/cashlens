\# CashLens



\## Overview

CashLens is an ML + GenAI credit-readiness copilot for Indian MSMEs.

It analyzes bank/UPI transaction data and GST information to generate:

\- 90-day cash-flow forecasts

\- Credit-readiness scores

\- Transaction categories

\- Anomaly flags

\- Explainable ML insights



\## Problem

Small businesses often struggle to demonstrate their financial health

and creditworthiness to lenders. CashLens converts transaction and GST

data into actionable financial insights.



\## Key Features

\- 90-day cash-flow forecasting

\- Credit-readiness scoring

\- Transaction categorization

\- Anomaly detection

\- SHAP-based explainability

\- AI-generated financial explanations

\- GST reconciliation

\- Lender-ready credit summary



\## Architecture



\[architecture diagram will go here]



Data Flow:



Data Upload / Sandbox

&#x20;       ↓

Data Processing

&#x20;       ↓

Feature Engineering

&#x20;       ↓

ML Pipeline

&#x20;       ↓

Forecast + Credit Score + Anomalies

&#x20;       ↓

SHAP Explainability

&#x20;       ↓

LangGraph Agent

&#x20;       ↓

Dashboard / Credit Memo



\## Tech Stack



\### Frontend

\- Next.js

\- React

\- TypeScript

\- Tailwind CSS



\### Backend

\- FastAPI

\- Python



\### Machine Learning

\- LightGBM / XGBoost

\- Prophet

\- Pandas

\- Scikit-learn

\- SHAP



\### AI / Agent

\- LangGraph

\- Ollama / Hosted LLM



\### Database

\- Supabase PostgreSQL

\- pgvector



\### Deployment

\- Docker

\- Vercel

\- Cloud container



\## ML Pipeline



\### 1. Cash-Flow Forecasting

LightGBM with lag and rolling-window features to forecast

30/60/90-day net cash inflow.



\### 2. Credit-Readiness Scoring

Gradient boosting model using financial behaviour features

to estimate repayment readiness.



\### 3. Transaction Categorization

Classification of bank/UPI transaction narrations into

spending categories.



\### 4. Anomaly Detection

Isolation Forest / statistical methods to identify

unusual transactions and potential statement anomalies.



\### 5. Explainability

SHAP is used to explain the factors influencing the

credit-readiness prediction.



\## Project Structure



```text

CashLens/

│

├── frontend/

├── backend/

├── ml/

├── agent/

├── data/

├── docs/

├── README.md

└── docker-compose.yml

