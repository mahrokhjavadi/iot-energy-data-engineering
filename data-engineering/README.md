# Data Engineering

This directory contains all data engineering components for the **Smart Energy IoT – End-to-End Pipeline**, including ETL processing, database modeling, schema design, and SQL scripts for both the operational (3NF) and analytical (DWH) layers.

The structure follows real-world data engineering standards and separates diagrams, SQL scripts, and documentation for clarity and maintainability.

---

## 📁 Structure

data-engineering/
│
├── diagrams/           # ERD, 3NF, Star Schema, SCD2 flow diagrams
│
├── sql/                # SQL scripts for Business DB + DWH creation
│   ├── 3nf_schema.sql
│   ├── dwh_star_schema.sql
│   ├── scd2_implementation.sql
│   └── helper_scripts.sql
│
└── docs/               # Additional technical documentation

---

## 🛠️ ETL & Data Cleaning

Although the core ETL scripts are stored in the main project folder, this section documents the data engineering logic:

- Handling missing values
- Type conversions (numeric, datetime parsing)
- Feature engineering (hour, day, month, season)
- Geospatial validation for IoT sensors
- Consistency + integrity checks before loading into DB


---

## 🗄️ Business Database (3NF)

The operational database is modeled in **3rd Normal Form** and includes:

- Households  
- Sensors  
- EnergyUsage  
- Weather  
- TimeDimension  

The goal is to ensure:

- Minimal redundancy  
- Strong referential integrity  
- Clean structure for transactional & analytical use  

ERD diagrams for 3NF are located in: data-engineering/diagrams/



---

## 🏛️ Data Warehouse (Star Schema + SCD Type 2)

The analytical layer includes:

### ⭐ Fact Tables
- fact_energy_usage

### ⭐ Dimension Tables
- dim_household (SCD Type 2 implemented)
- dim_sensor
- dim_time
- dim_weather

**SCD Type 2** tracks historical changes using:
- surrogate keys  
- effective timestamps  
- expiration timestamps  
- current record indicators  

SQL scripts for DWH creation are stored in: data-engineering/sql/



---

## 🧩 Diagrams

All schema and architecture diagrams:

- ERD  
- 3NF model  
- Star Schema  
- SCD Type 2 data flow  
- End-to-end pipeline diagram  

Located in: data-engineering/diagrams/



(Exported as PNG + the editable draw.io files.)

---

## 📚 Documentation

Additional explanations, schema notes, and architecture references are placed inside:  data-engineering/docs/



---

## 📦 Outputs Produced by This Module

✔ 3NF Business Database  
✔ Fully designed Star Schema + DWH  
✔ SCD Type 2 implementation logic  
✔ SQL scripts for automated database creation  
✔ Professional diagrams for reporting & documentation  

---

## ✨ Notes

This module ensures the entire pipeline is:

- Scalable  
- Fully documented  
- Aligned with industry best practices  
- Ready for BI, ML, and future expansion  

---









