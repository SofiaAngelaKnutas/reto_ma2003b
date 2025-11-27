# Retail Sales Pattern Analysis

This repository contains an end-to-end analytical project focused on understanding sales behavior, seasonal patterns, and demand dynamics across products, regions, and payment methods. The purpose of the work is to support business decisions related to inventory planning, product assortment, commercial strategy, and demand forecasting.

## Project Objective

The primary objective of this project is to analyze sales data in order to detect seasonal patterns, identify demand cycles, understand product performance, and reveal behavioral differences across customer regions and categories. The analysis also aims to support demand anticipation in the short and medium term through predictive modeling, while generating key business performance indicators such as total sales, units sold, average ticket, gross margin, inventory rotation, category participation, payment method usage, and growth rates.

## Business Context

The project is framed within decision-making needs in three areas. First, supply and assortment management, in which companies must decide which products to prioritize depending on seasonality and regional consumption patterns. Second, operational efficiency, where organizations seek to avoid both over-stocking and stock-outs while optimizing logistics. Third, commercial planning, where promotions and pricing decisions depend on demand peaks and troughs throughout the year. Throughout the analysis, guiding questions help steer insights, such as when and where seasonal peaks occur, where inventory could be reassigned without affecting service levels, and how payment behavior influences ticket size and purchase frequency.

## Data Source and Scope

The data used in this project comes from a Kaggle dataset. It includes twelve months of transactions, which allows for the study of seasonality. The dataset is assumed to be representative and sufficiently complete.

## Methodology and Workflow

### 1. Data Acquisition
- Importing raw datasets
- Reviewing schema, data types, and key identifiers

### 2. Data Cleaning and Preparation
- Handling missing values
- Removing duplicated records
- Detecting and evaluating outliers
- Standardizing formats (dates, numerical fields)
- Encoding categorical variables
- Creating derived variables:
  - month, week, seasonality indicators
  - RFM metrics
  - estimated margin
- Producing a cleaning log documenting decisions

### 3. Exploratory Data Analysis (EDA)
- Distribution and summary statistics
- Time series visualization
- Seasonal heatmaps (calendar-style)
- Sales evolution by region, category, and payment method

### 4. Segmentation and Clustering
- Clustering products based on demand patterns
- Algorithms considered:
  - K-Means
  - DBSCAN
  - Gaussian Mixture Models
- Automatic selection of number of clusters using:
  - Elbow method (inertia)
  - Silhouette score
- Interpretation of clusters by:
  - seasonal strength
  - volatility
  - payment mix
  - margin level

### 5. Predictive Modeling 
- Possible approaches:
  - Linear regression (with or without regularization)
  - Tree-based and boosting models
  - Time-series forecasting (ARIMA, ETS, Prophet)
  - Neural networks (if data volume allows)
- Evaluation and comparison using:
  - RMSE, MAE, MAPE
  - temporal cross-validation
  - baseline benchmarks

### 6. Visualization and Storytelling
- Executive-level dashboard
- Filters for region, category, and payment method
- Highlight visualizations:
  - trend decomposition
  - seasonal pattern maps
  - cluster diagram
  - feature importance


---

## Repository Structure

The repository follows a modular and reproducible layout so that each stage of the analysis can be traced and executed independently. The structure is organized as follows:
```text
reto_ma2003b/
│
├── data_raw/          # Original unmodified CSV files downloaded from Kaggle
├── data_cleaned/      # Processed and validated datasets, including master.parquet
│
├── notebooks/         # Iterative analytical work in Jupyter Notebooks:
│   ├── data_cleaning.ipynb
│   ├── eda.ipynb
│   ├── clustering.ipynb
│   └── modeling.ipynb
│
├── src/               # Python scripts for reusable functions (optional expansion)
│
├── reports/           # Exported plots, metrics, cluster summaries and findings
│
├── dashboard/         # Power BI / Looker Studio / Streamlit assets (if applicable)
│
├── README.md          # Main project documentation
├── requirements.txt   # Library dependencies needed to run the project
└── .gitignore         # Version control exclusions

```
## License and Attribution

This project is developed for academic purposes as part of course MA2003B.

## Authors

Mario, Sofia Knutas (A01831481), Kristina, Renato