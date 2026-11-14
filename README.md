# Financial Fraud Detection Platform

An end-to-end financial transaction fraud detection project combining Machine Learning, Deep Learning and an interactive prediction dashboard.

The project explores different approaches to identifying potentially fraudulent transactions using transaction-level features, predictive models and classification performance metrics.

## Overview

Financial fraud detection is a challenging classification problem, particularly because fraudulent transactions represent only a small proportion of total transactions.

This project explores several modeling approaches to address this challenge:

- Machine Learning with XGBoost
- Deep Learning with a Multi-Layer Perceptron (MLP)
- Graph-based learning with GraphSAGE
- A hybrid Graph Neural Network and XGBoost approach

An interactive Streamlit application provides a way to submit transaction information and obtain a fraud-risk prediction.

## Key Features

- Transaction preprocessing and feature transformation
- Multiple fraud detection modeling approaches
- Fraud probability estimation
- Risk-level classification
- Model prediction artifacts
- Interactive Streamlit dashboard
- Evaluation using classification metrics

## Technology Stack

| Category | Technologies |
|---|---|
| Programming | Python |
| Machine Learning | Scikit-learn, XGBoost |
| Deep Learning | PyTorch |
| Data Processing | NumPy, Pandas |
| Visualization | Matplotlib |
| Dashboard | Streamlit |
| API | FastAPI |
| Testing | Pytest |

## Project Architecture

```text
financial-fraud-detection/
│
├── app/
│   └── streamlit_app.py
│
├── artifacts/
│   ├── models/
│   └── predictions/
│
├── src/
│   └── fraud_detection/
│       ├── models/
│       │   ├── gnn.py
│       │   ├── hybrid.py
│       │   ├── mlp.py
│       │   └── xgboost_model.py
│       │
│       ├── constants.py
│       ├── data.py
│       ├── inference.py
│       ├── metrics.py
│       ├── pipeline.py
│       └── preprocessing.py
│
├── requirements.txt
├── requirements-dev.txt
└── README.md
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/AmineBounja/Fraud-detection-prediction.git
cd Fraud-detection-prediction
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## Running the Dashboard

Start the Streamlit application:

```bash
streamlit run app/streamlit_app.py
```

Open the local address displayed in your terminal, usually:

```text
http://localhost:8501
```

The dashboard allows users to enter transaction characteristics and obtain a fraud prediction with an estimated risk level.

## Model Evaluation

The project uses several evaluation metrics relevant to imbalanced classification:

| Metric | Purpose |
|---|---|
| Precision | Measures how many predicted fraud cases are actually fraudulent |
| Recall | Measures how many actual fraud cases are detected |
| F1-score | Balances precision and recall |
| ROC-AUC | Measures ranking performance across classification thresholds |
| PR-AUC | Evaluates precision-recall performance |

Accuracy alone is insufficient for fraud detection because a model can achieve high accuracy while failing to identify fraudulent transactions.

## Dataset

The repository includes a synthetic transaction dataset designed for experimentation.

The sample contains approximately 8,000 transactions, with a fraud proportion of approximately 3.19%.

**Important:** Results obtained from synthetic data should not be interpreted as proof of performance on real banking transactions.

## Current Implementation

The Streamlit application uses the available XGBoost inference artifacts to generate transaction predictions.

Other model implementations and artifacts are included in the repository for exploration and comparison.

## Project Scope

This repository is used as a technical learning and experimentation project focused on financial fraud detection, predictive modeling and model deployment.

The implementation is based on an existing open-source project and is being studied and adapted.

## Reference

Original project:

https://github.com/C-Healin/financial-fraud-detection-deep-learning

Original authorship and project history are retained through the Git repository history.

## License

Please refer to the original repository's license before redistributing or modifying its code.
