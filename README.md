<div align="center">

  <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=1200&h=400&fit=crop" alt="Data Analysis Banner">

  <h1>Uber Ride Data Analysis 📊 🚗</h1>
  
  <p>
    An exploratory data analysis (EDA) of 1,156 Uber rides, diving into patterns, popular times, and trip purposes.
  </p>

  <p>
    <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python">
    <img src="https://img.shields.io/badge/Pandas-1.5-blue?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
    <img src="https://img.shields.io/badge/Matplotlib-3.6-blue?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib">
    <img src="https://img.shields.io/badge/Seaborn-0.12-blue?style=for-the-badge&logo=seaborn&logoColor=white" alt="Seaborn">
  </p>
</div>

## 🚀 Overview

This project involves a comprehensive analysis of an Uber ride dataset. The goal is to clean and process the ride data, perform feature engineering, and then extract actionable insights through exploratory data analysis (EDA) and visualization.

The analysis answers key business questions such as identifying peak ride times, popular purposes, and common trip distances.

## 📊 Dataset

The dataset contains 1,156 rows of Uber ride data from 2016. Each record includes the following columns:

* START_DATE: The date and time when the ride started.
* END_DATE: The date and time when the ride ended.
* CATEGORY: The category of the ride (e.g., Business, Personal).
* START: The starting location of the ride.
* STOP: The destination of the ride.
* MILES: The total miles of the ride.
* PURPOSE: The purpose of the ride (e.g., Meeting, Meal/Entertain).

## 🛠️ Data Preprocessing & Feature Engineering

Before analysis, the data was thoroughly cleaned and new features were engineered to provide deeper insights:

1.  *🧽 Handling Missing Values:* Filled NaN values in the PURPOSE column with "Unknown" to retain all records.
2.  *🔄 Date/Time Conversion:* Converted START_DATE and END_DATE from object to datetime types. Rides with improperly formatted dates were identified as NaT and later dropped.
3.  *✨ Feature Engineering:*
    * Date: Extracted the date from START_DATE.
    * Time: Extracted the hour (0-23) from START_DATE.
    * day-night: Binned the Time into four categories: "Morning" (0-10), "Afternoon" (10-15), "Evening" (15-19), and "Night" (19-24).
    * MONTH: Extracted the month from START_DATE.
    * DAY: Extracted the day of the week (e.g., 'Mon', 'Tues') from START_DATE.
4.  *🗑️ Final Cleanup:* Dropped all remaining NaN values (primarily from date conversion errors) to ensure a clean dataset for analysis, resulting in 413 complete records.

## 📈 Key Insights & Visualizations

### 1. Ride Category Analysis
*Question:* In which category do people book the most Uber rides?

*Finding:* The vast majority of rides are categorized as *Business*, with 'Personal' rides being significantly fewer.


<img width="814" height="469" alt="download" src="https://github.com/user-attachments/assets/6abed1fb-6c6f-4208-8418-58ccaa15d056" />

### 2. Ride Purpose Analysis
*Question:* For which purpose do people book Uber rides the most?

*Finding:* The most common purpose for rides is *Meeting, followed by **Meal/Entertain*. A significant number of rides also have an "Unknown" purpose.


<img width="866" height="448" alt="download (1)" src="https://github.com/user-attachments/assets/5585e553-52bb-43cb-8ad9-1ade1f7f42fa" />

### 3. Peak Ride Times (Time of Day) 🌙
*Question:* At what time of day do people book cabs the most?

*Finding:* The *Afternoon* (3 PM - 7 PM) is the busiest time for rides, followed closely by 'Morning' rides. 'Night' has the lowest ride frequency.

<img width="613" height="432" alt="download (2)" src="https://github.com/user-attachments/assets/7029b92b-edfa-4fe9-b2c8-478864f05dea" />


### 4. Monthly Ride Trends 📅
*Question:* In which months do people book Uber rides less frequently?

*Finding:* Ride frequency (ride count) shows a noticeable dip around *September and October. The *maximum distance traveled in a single trip peaked in March.


<img width="571" height="433" alt="download (3)" src="https://github.com/user-attachments/assets/dd31e0de-c827-4b10-a86f-fc301d3a80b7" />

### 5. Peak Ride Days (Day of Week) 🗓️
*Question:* On which days of the week do people book Uber rides most?

*Finding:* *Friday* is the most popular day for Uber rides, indicating a peak at the end of the work week.


<img width="562" height="432" alt="download (4)" src="https://github.com/user-attachments/assets/c9a263a3-1d49-4efe-bd6a-fe1fa6bd1afa" />

### 6. Trip Distance Analysis 🗺️
*Question:* How many miles do people usually book a cab for?

*Finding:* Most trips are *short-distance (under 10 miles)*. The distribution is heavily skewed, so the plot below is filtered for trips under 40 miles to show the most common trip lengths.


<img width="576" height="436" alt="download (5)" src="https://github.com/user-attachments/assets/9114a0c3-1210-481d-bed1-b7fd03be75b4" />

## 💻 Technologies Used

* *Python 3*
* *Pandas:* For data manipulation and analysis.
* *Matplotlib & Seaborn:* For data visualization.
* *Jupyter Notebook:* For interactive analysis.

## 📂 How to Use

To replicate this analysis, you can clone the repository and run the Jupyter Notebook:

```bash
# 1. Clone the repository
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name

# 2. Install dependencies (assuming you have pip)
pip install pandas numpy matplotlib seaborn

# 3. Launch Jupyter Notebook
jupyter notebook Uber_Data_Analysis_Project.ipynb
