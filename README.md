# 📊 Netflix Movies & TV Shows Data Analysis

![Project Banner](https://github.com/zararah-malik/Netflix-Movies-and-TVShows/blob/main/banner.jpg)

## Introduction

This project is an in-depth analysis of **Netflix Movies and TV Shows**, focusing on uncovering insights through data visualization and analytics. Using **Python** for data cleaning and **Power BI** for visualization, I explored trends, distributions, and key patterns in Netflix's catalog. The goal was to transform raw data into meaningful insights that highlight Netflix's content trends over time.

## Problem Statement

I explored several key questions in this project:

- **What is the distribution of Movies vs. TV Shows on Netflix?**
- **Which countries produce the most content on Netflix?**
- **What are the trends of content being added over the years?**
- **Which genres (listed_in) are the most popular?**
- **Who are the most frequent directors and actors?**
- **What is the distribution of movie durations?**

## How I Approached the Problem

To tackle these questions, I **cleaned and prepared** the data using Python before moving on to visualization. Here’s how I handled missing values and feature engineering:

```python
import pandas as pd

# Load the dataset
df = pd.read_csv("netflix_titles.csv")

# Creating new columns for better analysis
df['Year_Added'] = pd.to_datetime(df['date_added']).dt.year
df['Month_Added'] = pd.to_datetime(df['date_added']).dt.month

# Filling missing values
df['cast'].fillna('Unknown', inplace=True)
df['country'].fillna('Unknown', inplace=True)
df['director'].fillna('Unknown', inplace=True)

# Save the cleaned data
df.to_csv("cleaned_netflix_data.csv", index=False)
```

After cleaning, I leveraged **Power BI** to create an interactive dashboard that visualizes key insights.

## Skills Utilized
- **Data Cleaning** (Handled missing values, formatted date columns, and structured data for analysis)
- **Feature Engineering** (Created new attributes like `Year_Added` and `Month_Added`)
- **Data Visualization** (Designed interactive dashboards in **Power BI**)
- **Storytelling with Data** (Transformed numbers into meaningful insights)

## Dashboard

### **1️⃣ Overview Page**
#### **Problem:** What does Netflix's content library look like in terms of movies vs. TV shows? Which countries contribute the most?
#### **Action:** I created bar charts, pie charts, and a map to illustrate content distribution and country-wise contribution.
#### **Result:** A clear visual breakdown of Netflix’s content distribution, making it easy to spot major trends.

![Overview Dashboard](https://github.com/zararah-malik/Netflix-Movies-and-TVShows/blob/main/Overview.png)

### **2️⃣ Trending Page**
#### **Problem:** How has Netflix’s content addition evolved over time? Are there any patterns in content release?
#### **Action:** Used line charts and bar graphs to display trends in content additions by year and month.
#### **Result:** Showcased historical trends, revealing how Netflix’s content library has grown significantly over the years.

![Trending Dashboard](https://github.com/zararah-malik/Netflix-Movies-and-TVShows/blob/main/Trending.png)

### **3️⃣ Drilldown Page**
#### **Problem:** How do monthly trends vary within different years?
#### **Action:** Implemented **Drilldown functionality** in Power BI to allow users to explore content trends on a monthly level.
#### **Result:** Users can analyze **seasonal trends** and observe when Netflix adds the most content.

![Drilldown Dashboard](https://github.com/zararah-malik/Netflix-Movies-and-TVShows/blob/main/Drilldown.png)

## Tools Used
- **Python (Pandas, NumPy)** – Data Cleaning & Feature Engineering
- **Power BI** – Data Visualization & Interactive Dashboard
- **Excel** – Additional data handling

## Conclusion

This project was an exciting dive into **Netflix’s vast content library**, offering valuable insights into trends, distributions, and content dynamics. From cleaning messy data with **Python** to designing an interactive dashboard in **Power BI**, this experience helped me **sharpen my analytical skills and storytelling abilities.**

🚀 **The key takeaway?** Data is more than just numbers—it tells a story! I’m looking forward to working on more projects and uncovering even deeper insights. If you’re interested in Power BI, Python, or data analytics, let’s connect and exchange ideas! 🔥

---

**Feel free to check out the project and reach out if you have any thoughts or suggestions!** 😊
