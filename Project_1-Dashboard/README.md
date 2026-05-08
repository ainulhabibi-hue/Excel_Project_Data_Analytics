# Excel Salary Dashboard

![Salary Dashboard Preview](/0_Resources/Images/1_Salary_Dashboard_Final_Dashboard.gif)

## Overview

This Excel dashboard project explores salary trends in the data job market using real-world 2023 job posting data. The dashboard was designed to help aspiring data professionals compare salaries across different job roles, countries, and work schedules.

The project focuses on transforming raw job market data into an interactive dashboard that supports salary exploration and career research.

---

## Project Goals

The dashboard was built to answer several practical questions:

* Which data jobs offer the highest median salaries?
* How do salaries differ across countries?
* Does work schedule type affect compensation?
* Which roles are more valuable in the current market?

---

## Tools & Excel Features

The project was completed entirely in Microsoft Excel using:

* 📊 Charts & Data Visualization
* 🧮 Formulas and Functions
* 🔍 Dynamic Filtering
* ❎ Data Validation
* 📋 Interactive Dashboard Design

---

## Dataset

The dataset contains 2023 data job postings collected from real-world sources.
The data includes:

* Job titles
* Salary information
* Country/location
* Job schedule types
* Skills and technologies

---

# Dashboard Development

## 📊 Salary Comparison by Job Title

<img src="/0_Resources/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary Comparison Chart">

### Key Features

* Horizontal bar charts were used to improve readability across multiple job titles.
* Salary values were formatted for quick interpretation.
* Job roles were sorted from highest to lowest median salary.

### Insights

* Senior-level positions consistently show higher salary ranges.
* Engineering-focused roles tend to outperform analyst positions in compensation.
* Specialized technical expertise appears to be strongly associated with higher pay.

---

## 🌍 Global Salary Distribution

![Country Salary Map](/0_Resources/Images/1_Salary_Dashboard_Country_Map.gif)

### Dashboard Design

* Excel map charts were used to visualize salary differences between countries.
* Color intensity highlights regions with higher and lower median salaries.

### Insights

* Salaries vary significantly depending on geographic region.
* Countries with larger technology sectors generally offer higher compensation.
* The dashboard makes it easier to identify potential high-paying markets for remote or international opportunities.

---

# Formula Implementation

## 💰 Dynamic Median Salary Calculation

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

### Formula Purpose

This formula calculates the median salary dynamically based on:

* Selected job title
* Country filter
* Schedule type
* Available salary records

### Why Median?

Median salary was chosen instead of average salary because it reduces the impact of extreme outliers and provides a more realistic representation of compensation trends.

---

## 📋 Schedule Type Filtering

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

### Functionality

This formula creates a cleaned and filtered list of schedule types by:

* Removing invalid values
* Excluding combined categories
* Returning only usable filter options

### Dashboard Benefit

The filtered list improves dashboard interaction and keeps dropdown selections organized and user-friendly.

---

# Interactive Features

## ❎ Data Validation & User Input

Data validation was applied to dashboard filters such as:

* Job Title
* Country
* Schedule Type

This improves:

* Dashboard usability
* Input consistency
* User experience
* Data accuracy

The interactive filters allow users to quickly explore salary trends based on their preferred criteria.

---

# Key Takeaways

From this project, several important trends became clear:

* Technical and engineering roles generally command higher salaries.
* Geographic location has a major influence on compensation levels.
* Interactive dashboards make salary exploration more accessible and easier to interpret.
* Excel can be used not only for spreadsheets, but also for building professional analytical dashboards.

---

# Final Thoughts

This project helped strengthen my skills in:

* Excel dashboard development
* Data visualization
* Formula-based analysis
* Interactive reporting
* Presenting insights from real-world datasets

The dashboard demonstrates how Excel can be leveraged to transform raw job market data into actionable career insights for job seekers and data professionals.
