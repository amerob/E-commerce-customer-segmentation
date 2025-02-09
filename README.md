# E-Commerce Customer Segmentation with RFM Analysis & KMeans Clustering

![3D Visualization of Customer Clusters](https://github.com/user-attachments/assets/46ea5f57-c9e1-408b-83de-f8f8a984cbeb)

## Overview

The project segments e-commerce customers using RFM Analysis (Recency, Frequency, Monetary) and K-Means clustering to enable targeted marketing strategies.

## Key Features

- **🔄 Data Pipeline**: From raw data cleaning to interactive dashboards.
- **📊 RFM Analysis**:
  - **🕒 Recency**: Days since last purchase
  - **🔁 Frequency**: Unique transactions
  - **💰 Monetary**: Total spending
- **🚫 Outlier Handling**: IQR-based removal of extreme spenders/frequent buyers.

## Pipeline

1. **📥 Load & Explore**  
   - Import dataset; perform initial EDA.
   - Identify issues: missing IDs, negative quantities, inconsistent codes.

2. **🧹 Clean Data**  
   - Convert Invoice/StockCode to strings; apply regex filters.
   - Remove records with missing Customer IDs and zero-priced items.

3. **🛠️ Feature Engineering**  
   - Aggregate Customer-Level Features.

4. **📊 Visualize & Remove Outliers**  
   - Plot distributions; remove outliers using IQR.

5. **🔄 Transform & Cluster**  
   - Standardize features.
   - Run KMeans (k=2–12); select optimal k (e.g., k=4) via inertia/silhouette scores.

6. **🔍 Interpret & Dashboard**  
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

```bash
# Clone the repository
git clone https://github.com/amerob/E-commerce-customer-segmentation.git
cd E-commerce-customer-segmentation

# Create and activate a virtual environment
python3 -m venv env
source env/bin/activate  # Linux/Mac
env\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt
