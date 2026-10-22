# Citi Bike Analytics: Big Data, Machine Learning & Business Insights

## Project Overview

This project analyzes historical Citi Bike trip data in New York City to identify mobility patterns, understand user behavior, and generate insights that can support operational planning and infrastructure decisions.

The project combines large-scale data processing with business-oriented analysis, machine learning, and interactive dashboard visualization. It was developed as part of the **Big Data & NoSQL Databases course (Spring 2026)**.

## Objectives

- Process and clean large-scale bike-sharing trip data.
- Engineer features to analyze trip duration, distance, speed, rider age, and time-based usage patterns.
- Use analytical queries to identify demand trends, popular stations, and operational priorities.
- Train and compare machine learning models for rider gender classification.
- Translate analytical findings into actionable business insights using Power BI.

## Methodology

### 1. Data Cleaning & Feature Engineering

Used PySpark to standardize the dataset, handle missing values and duplicates, and identify potentially noisy records.

Engineered additional features, including:
- Rider age and trip duration.
- Estimated trip distance using the Haversine formula.
- Estimated trip speed.
- Time-of-day categories and monthly features.
- Flags for unusually short trips, excessive speeds, and potential age outliers.

### 2. Business Analytics with Spark SQL

Developed analytical queries to investigate:

- Round-trip percentages by user type.
- Most popular starting and ending stations.
- Peak hours and seasonal demand patterns.
- Trip duration across rider age groups.
- Bike utilization and potential maintenance priorities.
- Popular routes and differences in riding behavior.
- Weekday versus weekend usage.

The findings were interpreted from an operational perspective, including bike redistribution, station capacity planning, maintenance scheduling, and service optimization.

### 3. Machine Learning

Built a classification pipeline using Spark MLlib to compare three models:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

The models were evaluated using an 80/20 training-test split and accuracy.

**Result:** The Random Forest classifier achieved the highest reported accuracy of approximately **73.99%** on the evaluated test set.

The task demonstrates the application of machine learning to behavioral data. Gender classification is an experimental course objective rather than a direct measure of bike demand, and the reported accuracy should be interpreted within that scope.

### 4. Power BI Dashboard

Created a Power BI dashboard using exported analytical query results to communicate findings through visualizations.

The dashboard highlights:
- Hourly, weekday, and seasonal demand patterns.
- High-demand stations and frequently used routes.
- Bike utilization and potential maintenance priorities.

The visualizations connect technical analysis to practical recommendations for resource allocation and service planning.

## Key Findings

- **Demand patterns:** Trip activity showed morning and evening peaks, consistent with commuting behavior.
- **Weekday vs. weekend usage:** The notebook reports that weekdays accounted for 74.94% of trips, compared with 25.06% on weekends.
- **Station planning:** High-demand stations and routes can help prioritize bike redistribution and docking capacity.
- **Fleet management:** Trip-duration patterns by bike ID can help identify assets for further maintenance investigation.
- **Machine learning:** Random Forest performed best among the three evaluated classifiers, with a reported accuracy of 73.99%.

## Technologies Used

- **Programming:** Python
- **Big Data Processing:** Apache Spark, PySpark
- **Data Querying:** Spark SQL
- **Machine Learning:** Spark MLlib
- **Data Visualization & Business Intelligence:** Microsoft Power BI
- **Data Engineering:** Data cleaning, feature engineering, outlier flagging

## Project Structure

```text
citi-bike-analytics/
├── BigData_&_NoSQL_Final_Project.ipynb
└── README.md
```

The notebook contains the data processing pipeline, analytical queries, model training and evaluation, and Power BI dashboard workflow.

## How to Run

1. Clone or download this repository.
2. Open the notebook in Google Colab or a compatible Jupyter environment.
3. Install and configure the required Python and Apache Spark dependencies.
4. Provide the Citi Bike dataset and update the notebook's data path as needed.
5. Run the notebook cells in order to execute the pipeline, queries, and machine learning experiments.
6. To reproduce the dashboard, export the required query results and load them into Power BI.

**Note:** The raw dataset is not included in this repository by default. The notebook requires access to the input CSV file and a compatible Spark environment.

## Learning Outcomes

This project provided practical experience in large-scale data processing, data quality management, feature engineering, analytical SQL, machine learning evaluation, and business intelligence reporting. It also demonstrated how technical analysis can be translated into insights for operational decision-making.

## Team Project

Developed collaboratively as part of the Big Data & NoSQL Databases course, Spring 2026.
