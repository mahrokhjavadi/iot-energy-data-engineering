# Data Directory

This folder contains all datasets used in the Smart Energy IoT end-to-end pipeline.  
It is structured to clearly separate original input data from processed outputs and the final MySQL database.

## 📁 Folder Structure

- **raw/**  
  Contains the original Kaggle dataset:  
  - `smart_grid_dataset_city_hourly_enriched.csv`  
  This is the unmodified source used for building the database.

- **db/**  
  Contains the final MySQL database:  
  - `smart_city_iot.db`  
  This database was created after applying the complete ETL workflow, normalization (3NF), stored procedures, and Data Warehouse modeling (Star Schema + SCD2).

- **.keep**  
  Placeholder file ensuring the directory is tracked by Git.

## 📌 Notes
- No intermediate “cleaned” files are stored here.  
- All transformations were performed directly into SQL using MySQL stored procedures, functions, and scripts located under `data-engineering/sql/`.

