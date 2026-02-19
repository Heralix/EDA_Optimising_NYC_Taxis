📊 EDA_Optimising_NYC_Taxis
 Exploratory Data Analysis – Optimising NYC Taxi Operations

Name: Pranav Dhurandhar
Assignment: EDA – Optimising NYC Taxis
Course: (Add course name if required)
Date: (Add submission date)

📌 Problem Statement

The objective of this project is to perform Exploratory Data Analysis (EDA) on NYC Taxi Trip Records to:

Identify demand patterns across hours, days, and months

Analyse operational efficiency and traffic trends

Study pricing behaviour and vendor comparison

Evaluate tipping patterns and passenger behaviour

Suggest data-driven optimisation strategies

The ultimate goal is to optimise routing, pricing strategy, and resource allocation.

📂 Files Included

This repository contains:

📓 EDA_Optimising_NYC_Taxis_<your_name>.ipynb
→ Interactive Jupyter Notebook with full code implementation

📄 EDA_Optimising_NYC_Taxis_Report.pdf
→ Detailed analysis report with visualisations, findings, and recommendations

📊 Dataset Information

Dataset Used: NYC Taxi Trip Records – January 2023

Source:
https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Geographical shapefile:
taxi_zones.shp (used with GeoPandas)

⚠️ Note:
The dataset is not uploaded to this repository due to its large size.
All analysis is based on the official NYC TLC dataset.

🧠 Analysis Overview

The project is divided into the following major sections:

1️⃣ General EDA

Classification of variables (Numerical / Categorical)

Hourly pickup trends

Daily (weekday vs weekend) comparison

Monthly pickup trends

Payment type distribution

Correlation between:

Fare & trip distance

Fare & trip duration

Tip & distance

2️⃣ Financial Analysis

Identification of zero/negative values

Revenue share: Night vs Day

Average fare per mile

Fare per mile per passenger

Vendor comparison

Tier-based fare analysis (0–2 miles, 2–5 miles, >5 miles)

3️⃣ Operational Efficiency

Speed analysis by hour

Identification of busiest hours

Scaling up sampled data using sampling fraction

Weekday vs weekend traffic pattern comparison

Pickup vs dropoff zone analysis

Pickup/Dropoff ratio analysis

Night traffic zone identification (11 PM – 5 AM)

4️⃣ Geographical Analysis

Merged trip records with NYC taxi zones shapefile

Created choropleth maps of:

Zone-wise trips

Traffic density

GeoPandas was used for spatial analysis.

5️⃣ Pricing Strategy Insights

Fare behaviour across hours

Vendor-level pricing comparison

Distance-tier pricing structure

Tipping behaviour patterns

Factors affecting low and high tip percentages

📈 Key Insights

Late evening (11 PM) is the busiest hour.

Manhattan zones dominate pickups and dropoffs.

Night revenue share is significantly lower than daytime (~19%).

Fare per mile decreases as passenger count increases.

Short-distance trips have higher fare-per-mile rates.

Some zones show high pickup/dropoff imbalance indicating directional demand.

⚙️ Assumptions Made

Sampling fraction assumed: 5% (0.05)

Speed calculated as:
trip_distance / trip_duration

Night hours defined as:
11 PM to 5 AM

Zero-distance trips excluded from correlation analysis

All assumptions are documented inside the report.

🛠️ Tools & Libraries Used

Python

Pandas

NumPy

Matplotlib

Seaborn

GeoPandas

📌 How to Run
1️⃣ Download the Dataset

Download the NYC Taxi Trip dataset (January 2023) from:

https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Also download the taxi_zones shapefile for geographical analysis.

2️⃣ Place Files in Project Folder

Place the following files inside your project directory:

yellow_tripdata_2023-01.parquet (or CSV version)

taxi_zones folder containing:

taxi_zones.shp

taxi_zones.dbf

taxi_zones.shx

taxi_zones.prj

taxi_zones.sbn

taxi_zones.sbx

⚠️ Do not change the internal structure of the taxi_zones folder.

3️⃣ Install Required Libraries

Run:

pip install pandas numpy matplotlib seaborn geopandas pyarrow


(pyarrow is required if using parquet files.)

4️⃣ Import the Dataset in Jupyter Notebook

If using Parquet file:

import pandas as pd

df = pd.read_parquet("yellow_tripdata_2023-01.parquet")
df.head()


If using CSV file:

import pandas as pd

df = pd.read_csv("yellow_tripdata_2023-01.csv")
df.head()

5️⃣ Import Shapefile for Geographical Analysis
import geopandas as gpd

zones = gpd.read_file("taxi_zones/taxi_zones.shp")
zones.head()

6️⃣ Run the Notebook Sequentially

Execute cells in order to reproduce:

EDA analysis

Financial insights

Operational efficiency analysis

Geographical visualisations

Pricing strategy insights

🎯 Final Outcome

The project provides actionable insights for:

Optimising driver deployment

Strategic zone positioning

Dynamic pricing adjustments

Improving revenue during low-demand hours

Understanding customer tipping behaviour
