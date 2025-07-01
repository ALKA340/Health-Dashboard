![Dashboard Banner](cover.png)

****🌊 **WellnessWave – Power BI Health & App Usage Dashboard**

🧠 **About the Project**

A health-tech analytics dashboard that simulates real-world data from a fictional fitness platform. This project explores user activity, sleep patterns, heart rate, and subscription behavior to identify trends and health risks using Power BI and SQL. 

🛠️ **Tools Used**

Power BI for dashboard creation and DAX logic

SQL for extracting insights from raw data

Excel for initial data handling and storage

GitHub for project versioning and presentation

📂 **Files Included**

File Name

Description

WellnessWave.pbix

Power BI dashboard file

health_data.csv

Sample dataset used for the analysis

cover.png

Banner image for GitHub presentation

README.md

Project overview and documentation

📊 **Key Visuals in Dashboard**

Card: Avg Heart Rate, Avg Steps, Avg Sleep Hours

Bar Chart: Steps by City

Pie Chart: Gender distribution

Donut Chart: Subscription types

Line Chart: Sleep Hours over time

Slicers: Filter by City, Gender, and Subscription

Risk Detection using DAX column:

HealthRisk =
IF(
    'health_data'[HeartRate] > 100 && 'health_data'[SleepHours] < 5,
    "At Risk",
    "Normal"
)
This logic flags users as "At Risk" based on high heart rate and insufficient sleep.

🧪** SQL Queries for Business Insights**

Simulated queries written assuming the health_data.csv is stored in a SQL table named health_data.
1. 📍 Top Cities by Average Daily Steps
Top Cities by Average Steps
SELECT City, AVG(Steps) AS AvgSteps
FROM health_data
GROUP BY City
ORDER BY AvgSteps DESC;

2. 🚨 Identify “At Risk” Users
SELECT UserID, HeartRate, SleepHours
FROM health_data
WHERE HeartRate > 100 AND SleepHours < 5;

3. 🧘‍♀️ Compare App Usage by Subscription Type
SELECT Subscription, AVG(AppUsageMins) AS AvgUsage
FROM health_data
GROUP BY Subscription;

4. 🚹 Gender-Wise Average Steps
SELECT Gender, AVG(Steps) AS AvgSteps
FROM health_data
GROUP BY Gender;

5. 💼 Count of Users per Subscription Tier
SELECT Subscription, COUNT(*) AS TotalUsers
FROM health_data
GROUP BY Subscription;

   
💡 **Insights Derived**

-Gender-based activity patterns show women have slightly higher average sleep
- Users aged **18–25** have the highest average steps but lowest sleep hours.
- Most **At Risk** users had heart rates > 100 and slept less than 5 hours.
- **Delhi and Bangalore** users show higher app engagement.

---


## 🧪 Health Risk Detection Logic



**🌸 Created By
Alka Mittal
📍 IGDTUW, Delhi | Aspiring Data Analyst
🔗 LinkedIn
📧 am2021374@gmail.com

