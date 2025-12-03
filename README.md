# Retail Sales Pattern Analysis

This repository contains an end-to-end analytical project focused on understanding sales behavior, seasonal patterns, and demand dynamics across products, regions, and payment methods. The purpose of the work is to support business decisions related to inventory planning, product assortment, commercial strategy, and demand forecasting.

## Project Objective

The primary objective of this project is to analyze sales data in order to detect seasonal patterns, identify demand cycles, understand product performance, and reveal behavioral differences across customer regions and categories. The analysis also aims to support demand anticipation in the short and medium term through predictive modeling, while generating key business performance indicators such as total sales, units sold, average ticket, gross margin, inventory rotation, category participation, payment method usage, and growth rates.

## Business Context

The project is framed within decision-making needs in three areas. First, supply and assortment management, in which companies must decide which products to prioritize depending on seasonality and regional consumption patterns. Second, operational efficiency, where organizations seek to avoid both over-stocking and stock-outs while optimizing logistics. Third, commercial planning, where promotions and pricing decisions depend on demand peaks and troughs throughout the year. Throughout the analysis, guiding questions help steer insights, such as when and where seasonal peaks occur, where inventory could be reassigned without affecting service levels, and how payment behavior influences ticket size and purchase frequency.

## Data Source and Scope

The data used in this project comes from a Kaggle dataset. It includes twelve months of transactions, which allows for the study of seasonality. The dataset is assumed to be representative and sufficiently complete.



## Repository Structure

The repository follows a modular and reproducible layout so that each stage of the analysis can be traced and executed independently. The structure is organized as follows:
```text
reto_ma2003b/
│
├── data_raw/          # Original unmodified CSV files downloaded from Kaggle
├── data_cleaned/      # Processed and validated datasets, summarized in master.parquet
│
├── notebooks/         # Analytical work in Jupyter Notebooks:
│   ├── data_cleaning.ipynb
│   ├── eda.ipynb
│   ├── clustering.ipynb
│   └── modeling.ipynb
│         
│
├── reports/           # Variable dictionary and log of data cleaning
│
├── README.md          # Main project documentation
├── requirements.txt   # Library dependencies needed to run the project
└── .gitignore         # Version control exclusions

```
## License and Attribution

This project is developed for academic purposes as part of course MA2003B.

## Authors

Mario Gaitan, Sofia Knutas, Kristina Stapnes, Renato Castillo