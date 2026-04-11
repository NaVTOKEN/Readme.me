Manufacturing Machine Sensor Analytics

Project Overview

This project analyzes manufacturing machine performance using sensor, production, and maintenance data. The goal is to identify early warning signs of machine failures, calculate operational KPIs, and evaluate overall production efficiency.

Technologies Used

Python
Data Processing: Pandas, NumPy
Statistical Analysis: SciPy
Data Visualization: Seaborn, Matplotlib
Database: SQL (Planned)
Dashboards: Power BI / Tableau (Planned)

Dataset Description

The project integrates multiple datasets into a unified analytical view:

Sensor Data: Machine temperature, vibration, pressure, and RPM readings.
Maintenance Logs: Historical machine failures, repair times, and technician assignments.

Machine Master: Static machine metadata including plant location, machine type, and installation year.

Production Logs: Daily units produced, defect counts, and shift information.

Key KPIs Calculated

Machine Age (in years and days)
Availability (adjusted for repair downtime)
Defect Rate %
Quality Score
Overall Equipment Effectiveness (OEE)
Failure Risk Indicators (Hours before failure)

Data Processing Steps

Data Cleaning & Preprocessing: Formatting timestamps safely across multiple datasets.
Feature Engineering: Calculating rolling averages and applying Z-scores to detect temperature anomalies and vibration spikes.
Data Integration: Merging disparate CSV files on common keys (machine_id, timestamp).
Handling Missing Values: Using forward-fill techniques for continuous sensor readings and zero-filling for production gaps.
KPI Calculation: Deriving complex metrics like OEE using structured Pandas operations.

Project Structure

manufacturing_machine_sensor_analytics/
├── data/
│   ├── raw/
│   │   ├── machine_master.csv
│   │   ├── maintenance_logs.csv
│   │   ├── production_logs.csv
│   │   └── sensor_data.csv
│   └── processed/
│       ├── final_manufacturing_analytics.csv
│       └── final_manufacturing_analytics_handled_NaN.csv
├── manufacturing_sensor_analysis.ipynb
└── README.md
