# DC Crime and Traffic Incident Analysis (2019-2023)

## Project Overview

This project analyzes crime incidents and traffic crash patterns in Washington, DC from 2019 to 2023. The dashboard explores how reported crime incidents and traffic crashes vary across time, ward, incident category, and day/hour patterns.

The goal of this project is to create a clean, realistic, and data-driven dashboard that helps users understand spatial and temporal incident patterns across DC wards.

## Dashboard Preview

![DC Crime and Traffic Incident Analysis Dashboard](dc_crime_and_traffic_analysis_dashboard.png)

## Project Objective

The main objective of this project is to analyze public safety and transportation incident data in Washington, DC using open government data.

The dashboard answers questions such as:

1. How many crime incidents and traffic crashes were reported between 2019 and 2023?
2. Which DC wards had the highest combined incident volume?
3. What crime categories appeared most frequently?
4. What time of day and day of week had higher incident activity?
5. Is there a visible ward-level relationship between crime incidents and traffic crashes?

## Data Sources

The datasets used in this project come from official public data sources.

### Crime Data

Crime incidents were collected from Open Data DC / Data.gov. The records are published by the District of Columbia Metropolitan Police Department.

Crime Incidents in 2019:
https://catalog.data.gov/dataset/crime-incidents-in-2019

Crime Incidents in 2020:
https://catalog.data.gov/dataset/crime-incidents-in-2020

Crime Incidents in 2021:
https://catalog.data.gov/dataset/crime-incidents-in-2021

Crime Incidents in 2022:
https://catalog.data.gov/dataset/crime-incidents-in-2022

Crime Incidents in 2023:
https://catalog.data.gov/dataset/crime-incidents-in-2023

### Traffic Crash Data

Traffic crash data was collected from the official Crashes in DC dataset.

Crashes in DC:
https://catalog.data.gov/dataset/crashes-in-dc

Crash Details Table:
https://catalog.data.gov/dataset/crash-details-table

### Geographic Boundary Data

DC ward boundaries were collected from the official DC ward boundary dataset.

DC Ward Boundaries:
https://catalog.data.gov/dataset/wards-from-2022

## Dashboard Metrics

The dashboard includes the following key metrics:

1. Total Crime Incidents
2. Total Traffic Crashes
3. Average Daily Crime Incidents
4. Average Daily Traffic Crashes
5. Crime-to-Crash Ratio
6. Peak Crime Hour
7. Peak Crash Hour
8. Busiest Day for Crime
9. Busiest Day for Crashes
10. Ward-Level Total Incidents

## Dashboard Sections

### 1. KPI Cards

The top section of the dashboard shows high-level summary metrics, including total reported crime incidents, total traffic crashes, average daily crime incidents, average daily crashes, and the crime-to-crash ratio.

These metrics give a quick overview of the overall public safety and traffic incident activity in Washington, DC during the 2019-2023 period.

### 2. Incidents Over Time

The time-series chart shows monthly trends for crime incidents and traffic crashes.

This helps identify whether incident activity increased, decreased, or remained stable over time. It also helps reveal seasonal or recurring patterns.

### 3. Total Incidents by Ward

The ward map shows total combined incidents by DC ward.

Darker colors represent wards with higher combined incident volume, while lighter colors represent wards with lower incident volume. This makes it easier to identify geographic concentration across the city.

### 4. Incidents by Day of Week and Hour

The heatmap shows incident intensity by day of week and time of day.

Darker red areas indicate higher incident activity. This helps identify peak periods, such as weekday evenings, when both crime and traffic-related incidents may be more concentrated.

### 5. Top Crime Categories

The horizontal bar chart ranks the most common reported crime categories.

This section helps identify which crime types contribute the most to total reported crime incidents.

### 6. Ward-Level Crime vs. Crash Activity

The scatter plot compares crime incidents and traffic crashes by ward.

Each point represents one DC ward. This chart helps show whether wards with higher traffic crash activity also tend to have higher reported crime activity.

### 7. Ward Summary Table

The ward summary table provides a structured comparison of crime incidents, traffic crashes, and total incidents by ward.

This table supports the map and scatter plot by giving the exact numeric values behind the visual analysis.

## Key Insights

1. Crime incidents were higher than traffic crashes across the 2019-2023 period.

2. Ward-level patterns show that some wards had noticeably higher combined incident volume than others.

3. Evening hours showed stronger incident concentration compared with early morning hours.

4. The dashboard suggests a positive ward-level relationship between crime incident volume and traffic crash volume.

5. Wards 7 and 8 showed some of the highest combined incident totals in the dashboard view.

6. The dashboard is useful for identifying high-activity areas, peak incident times, and differences between wards.

## Tools Used

The dashboard can be built using:

1. Tableau
2. Power BI
3. Python
4. Pandas
5. Excel
6. Open Data DC
7. Data.gov

## Suggested Data Cleaning Steps

The following cleaning steps can be used before dashboard development:

1. Combine annual crime datasets from 2019, 2020, 2021, 2022, and 2023.
2. Standardize date columns into a consistent date format.
3. Extract year, month, day of week, and hour from incident date fields.
4. Standardize ward values.
5. Remove records with missing or invalid ward values.
6. Group crime incidents by ward, month, category, day, and hour.
7. Filter traffic crash records to the same 2019-2023 time period.
8. Aggregate crash records by ward, month, day, and hour.
9. Join crime and crash summaries at the ward level.
10. Use official DC ward boundaries for map visualization.

## Suggested Repository Structure

```text
dc-crime-traffic-analysis/
│
├── data/
│   ├── raw/
│   │   ├── crime_incidents_2019.csv
│   │   ├── crime_incidents_2020.csv
│   │   ├── crime_incidents_2021.csv
│   │   ├── crime_incidents_2022.csv
│   │   ├── crime_incidents_2023.csv
│   │   └── crashes_in_dc.csv
│   │
│   ├── processed/
│   │   ├── cleaned_crime_incidents_2019_2023.csv
│   │   ├── cleaned_traffic_crashes_2019_2023.csv
│   │   └── ward_level_summary.csv
│
├── dashboard/
│   └── dc_crime_traffic_dashboard.twbx
│
├── images/
│   └── dc_crime_and_traffic_analysis_dashboard.png
│
├── notebooks/
│   └── data_cleaning_and_analysis.ipynb
│
└── README.md
