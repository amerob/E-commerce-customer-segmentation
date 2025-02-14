# E-Commerce Customer Segmentation


> ![3d_plot](https://github.com/user-attachments/assets/2ff3ded1-5d81-4a1e-96d1-511c8a444d80)

## Overview

The project segments e-commerce customers using RFM Analysis (Recency, Frequency, Monetary) and K-Means clustering to enable targeted marketing strategies.

- [Download the Dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II)

<a href="https://archive.ics.uci.edu/ml/datasets/Online+Retail+II" target="_blank" style="display:inline-block;padding:10px 20px;background-color:#4CAF50;color:white;text-align:center;border-radius:5px;text-decoration:none;"> Download the Dataset </a>


## Key Features

- **🔄 Data Pipeline**: From raw data cleaning to interactive dashboards.
- **📊 RFM Analysis**:
  - **🕒 Recency**: Days since last purchase
  - **🔁 Frequency**: Unique transactions
  - **💰 Monetary**: Total spending
- **🚫 Outlier Handling**: IQR-based removal of extreme spenders/frequent buyers.

## Pipeline

- **📥 Load & Explore**  
   - Import dataset; perform initial EDA.
   - Identify issues: missing IDs, negative quantities, inconsistent codes.

- **🧹 Clean Data**
    - Convert Invoice/StockCode to strings; apply regex filters.
    - Remove records with missing Customer IDs and zero-priced items.

- **🛠️ Feature Engineering**  
    - Aggregate Customer-Level Features.

- **📊 Visualize & Remove Outliers**  
    - Plot distributions; remove outliers using IQR.

- **🔄 Transform & Cluster**
    - Standardize features.
    - Run KMeans (k=2–12); select optimal k (e.g., k=4) via inertia/silhouette scores.

- **🔍 Interpret & Dashboard**  
    - Label clusters (Retain, Re-Engage, Nurture, Reward).
    - Visualize clusters; build interactive dashboard with Plotly Dash.

## Requirements

- **🐍 Python 3.7+**
- Required packages (listed in `requirements.txt`):
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`
  - `plotly`
  - `dash`
  - `openpyxl`

## Installation

Clone the repository and install the dependencies:

- Clone the repository

  ```bash
  git clone https://github.com/amerob/E-commerce-customer-segmentation.git
  cd E-commerce-customer-segmentation
  ```

- Create and activate a virtual environment

  ```bash
  python3 -m venv env
  source env/bin/activate  # Linux/Mac
  env\Scripts\activate     # Windows
  ```

- Install dependencies

  ```bash
  pip install -r requirements.txt
  ```
