# NHL Pipeline Project

## Overview

This project transforms raw National Hockey League (NHL) game data into Team DNA Profiles — data-driven representations of how teams play and evolve across seasons.

By integrating multiple datasets, the project identifies distinct Team Archetypes:
- Attackers
- Defenders
- Strategists
- Balancers

These archetypes are defined using key performance metrics such as efficiency, defense, and aggressiveness.

The outcome is an interactive visualization that highlights how team styles shift over time and how different archetypes influence success.

Data was consolidated, cleaned, and modeled using Microsoft Fabric and the Medallion architecture, demonstrating skills in data pipeline design, ETL, and data modeling.

## Project Structure
```
NHL_Pipeline/
├── notebooks/
│   ├── 01_silver_layer_data_cleaning_pyspark.ipynb
│   ├── 02_gold_layer_table_creation_sparksql.ipynb
├── docs/
│   └── project_documentation.pdf
├── reports/
│   └── powerbi_dashboard_screenshots/
│       └── Power BI report.pdf
└── README.md
```
- ```notebooks/``` – Jupyter notebooks for Silver layer cleaning and Gold layer table creation.
- ```docs/``` – Detailed project documentation.
- ```reports/``` – Power BI screenshots showcasing team archetypes and season trends.

## Datasets
- Raw datasets were manually uploaded to Microsoft Fabric Lakehouse.
- Due to large size, they are not included in this repository.
- They can be downloaded from Kaggle: [NHL Game Data](https://www.kaggle.com/datasets/martinellis/nhl-game-data?select=table_relationships.JPG).

## Workflow
### 1. Data Cleaning (Silver Layer)
- Performed using PySpark on lakehouse data.
- Cleaned raw game and player data, handled missing values and duplicates.

### 2. Team DNA Profiles & Archetypes (Gold Layer)
- Used Spark SQL to create dimension and fact tables.
- Computed metrics for each team and assigned archetypes.
- Designed star schema for analytics-ready tables.

### 3. Visualization
- Power BI dashboards visualize how team styles shift over seasons.
- Interactive slicers allow exploration by team, season, and archetype.

## What I Learned
- Categorizing sports teams based on performance metrics and tracking evolution over multiple seasons.
- Practical experience with PySpark and Spark SQL for structured data transformations.
- Designing a medallion architecture (Bronze, Silver, Gold layers) for analytics pipelines.
- Using Microsoft Fabric Lakehouse to manage raw data.
- Creating interactive dashboards to communicate insights visually.

## How to Run
1. Clone this repository
   ```bash
      git clone https://github.com/Yuyun-Kong/NHL_Pipeline.git
   ```
2. Download the datasets from the Kaggle link above (optional if you want to replicate analysis locally).
3. Open the notebooks in Jupyter Lab or Jupyter Notebook in the following order:
   ```text
      01_silver_layer_data_cleaning_pyspark.ipynb
      02_gold_layer_table_creation_sparksql.ipynb
   ```
4. View Power BI dashboards (screenshots available in ```reports/```).
