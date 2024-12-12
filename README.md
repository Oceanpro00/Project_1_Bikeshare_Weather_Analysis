# Project_1_Bikeshare_Weather_Analysis

## Overview

This project investigates the **impact of weather conditions** on **bike-share usage patterns** in Central Chicago. By leveraging historical data and API integrations, we aim to uncover **key trends, predict ridership,** and provide **actionable insights** for urban planning and operational improvements.

### Team Members
	•	Jitesh Makan
	•	Lovecy Thomas
	•	Sean Schallberger

## Objectives
	1.	Analyze the relationship between weather conditions (e.g., temperature, precipitation, wind speed) and bike-share usage.
	2.	Predict ride counts based on weather conditions using regression models and real-time API data.

### Primary Research Question

How do weather conditions impact bike-share usage patterns, and can forecasted weather data be used to predict usage?

### Supporting Research Questions
	1.	How Does Weather Impact Ride Volume?
	2.	What Temporal Trends Emerge Across Weather Conditions?
	3.	How Do Different User Types Respond to Weather?
	4.	How Are Stations Affected by Weather?

## Tools and Technologies

### Programming
	•	Python

### Libraries
	•	Data Analysis & Cleaning: Pandas, NumPy
	•	Visualization: Matplotlib, Plotly
	•	Statistical Modeling: Scipy
	•	API Integration: Requests

### APIs
	1.	OpenWeatherMap API: Historical and real-time weather data.
	2.	Divvy Bike Share Data: Publicly available datasets (Kaggle Link).

## Methodology

### 1. Data Collection
	•	Bike-Share Data: Monthly ride data (2020–2023) with details like trip duration, start times, user type, and rideable type.
	•	Weather Data: Hourly data from OpenWeatherMap, including temperature, precipitation, humidity, and weather conditions.

### 2. Data Cleaning
	•	Bike-Share Data:
	•	Filtered Chicago-specific data.
	•	Derived metrics like trip duration, ride hour, and user type.
	•	Removed invalid and duplicate entries.
	•	Weather Data:
	•	Converted UTC timestamps to local Chicago time.
	•	Removed duplicates and irrelevant columns.

### 3. Data Integration
	•	Merged datasets by day and hour.
	•	Calculated derived metrics, including normalized ride counts and temperature categories.

### 4. Exploratory Data Analysis (EDA)
	•	Examined usage trends across weather conditions, ride times, and user types.
	•	Visualized relationships with bar charts, scatter plots, and line graphs.

### 5. Predictive Modeling
	•	Trained regression models using weather variables to predict ride counts.
	•	Used R² to evaluate model accuracy.
	•	Integrated real-time weather data for hourly predictions.

## Key Code Features

### API Pull
	•	Retrieves real-time weather data for Chicago from OpenWeatherMap.
	•	Predicts hourly ride counts using regression models trained on historical data.
	•	Outputs prediction tables with R² values for each weather metric.

### Data Cleaning
	•	Combines monthly bike-share datasets into a unified dataframe.
	•	Cleans weather data for integration by adjusting timestamps and removing duplicates.

### Data Integration
	•	Merges bike-share and weather datasets by timestamp.
	•	Categorizes temperatures and weather conditions to facilitate analysis.

### Visualizations
	•	Bar charts for ride probability by weather condition.
	•	Scatter plots showing relationships between temperature and ridership.
	•	Line charts for temporal trends in ride counts.
	•	Histograms displaying predicted ride counts by hour.

## Deliverables

### Folder Structure

bike-weather-analysis/
│
├── data/
│   ├── chicago_weather_data_2020_2023.csv
│   ├── 202004-divvy-tripdata.csv
│   ├── ...
│
├── scripts/
│   ├── api_pull.py
│   ├── data_cleaning.py
│   ├── exploratory_analysis.py
│
├── output/
│   ├── merged_weather_bike_data.csv
│   ├── visualizations/
│   ├── predictions.csv
│
├── README.md

### Final Outputs
	1.	Cleaned Dataset: Merged and formatted bike-share and weather data.
	2.	Visualizations: Charts showcasing key trends.
	3.	Prediction Models: Hourly ride count predictions based on real-time weather data.

## Insights and Recommendations

### Insights
	1.	Ride Volume: Clear and cloudy weather drive higher ridership, while adverse conditions like rain and snow significantly reduce rides.
	2.	Temporal Trends: Peak usage during commuting hours and summer months.
	3.	User Behavior: Members maintain consistent usage; Casual Users are highly sensitive to weather changes.

### Recommendations
	1.	Increase bike availability during peak commuting hours and favorable weather.
	2.	Offer promotions targeting Casual Users during mild weather conditions.
	3.	Improve infrastructure, such as sheltered docks, to support riders during adverse weather.

## Instructions for Replication
	1.	Clone the repository:

git clone <repo_url>


	2.	Install dependencies:

pip install -r requirements.txt


	3.	Run scripts sequentially:
	•	data_cleaning.py: Prepares and integrates datasets.
	•	exploratory_analysis.py: Generates visualizations and descriptive insights.
	•	api_pull.py: Fetches real-time weather data and predicts ride counts.
	4.	Access outputs in the /output folder.

## Acknowledgments
	•	Divvy Bike Share for providing comprehensive bike usage data.
	•	OpenWeatherMap for offering detailed weather datasets.