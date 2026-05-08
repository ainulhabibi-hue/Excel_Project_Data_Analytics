# Data Job Market Analysis in Excel

## Project Overview

This project explores salary trends and skill demand in the data job market using Excel-based data analysis techniques. The analysis focuses on identifying which skills are most valuable, how salaries vary across regions, and what technologies appear most frequently in data-related roles.

Using real-world 2023 job posting data, the project demonstrates how Excel can be used for data cleaning, modeling, and analytical reporting.

---

# Business Questions

The analysis was designed to answer several key questions about the data industry:

1. Do jobs requiring more skills tend to offer higher salaries?
2. How do salaries differ between regions and countries?
3. Which skills are most commonly requested in data-related jobs?
4. Which technical skills are associated with higher pay?

---

# Tools & Techniques

The following Excel tools were used throughout the project:

* 📊 Pivot Tables
* 📈 Pivot Charts
* 🧮 DAX Measures
* 🔍 Power Query
* 💪 Power Pivot
* 📋 Data Modeling

---

# Dataset

The dataset contains real-world data job postings from 2023, including:

* Job titles
* Salary information
* Country/location
* Required skills
* Schedule types

The data was cleaned and transformed before analysis to improve consistency and usability.

---

# 1️⃣ Relationship Between Skills and Salary

## 🔍 Data Preparation with Power Query

### Data Extraction

The raw dataset was imported into Power Query and separated into two structured tables:

* `data_jobs_all`
* `data_job_skills`

This separation made it easier to build relationships between jobs and associated skills.

---

### Data Transformation

Several cleaning and preparation steps were performed:

* Corrected column data types
* Removed unnecessary fields
* Trimmed extra spaces
* Standardized text formatting
* Cleaned inconsistent values

#### Data Cleaning Preview

![Power Query Jobs Table](/0_Resources/Images/2_Project_Analysis_Screenshot1.png)

![Power Query Skills Table](/0_Resources/Images/2_Project_Analysis_Screenshot2.png)

---

### Data Loading

The cleaned queries were loaded into Excel for further analysis and modeling.

![Loaded Jobs Data](/0_Resources/Images/2_Project_Analysis_Screenshot3.png)

![Loaded Skills Data](/0_Resources/Images/2_Project_Analysis_Screenshot4.png)

---

## 📊 Findings

### Key Insights

* Roles requiring broader technical skill sets generally showed higher median salaries.
* Senior and engineering-focused positions demonstrated the strongest relationship between skill count and compensation.
* Less specialized positions tended to have lower salary ranges.

![Skills vs Salary Chart](/0_Resources/Images/2_Project_Analysis_Chart1.png)

### Interpretation

The results suggest that combining multiple technical skills may increase market value in the data industry. Employers appear willing to offer higher compensation for candidates with broader technical capabilities.

---

# 2️⃣ Salary Comparison Across Regions

## 🧮 Pivot Tables & DAX Analysis

A Power Pivot data model was used to analyze salary differences across countries and job categories.

---

## DAX Measures

### Median Salary Measure

```DAX id="u5m5yr"
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```

### United States Salary Filter

```DAX id="8juyov"
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States"
)
```

---

## 📊 Findings

### Key Insights

* Senior Data Engineers and Data Scientists consistently ranked among the highest-paying positions.
* US-based salaries were significantly higher in many technical roles.
* Salary gaps between regions were especially visible in cloud and engineering-related jobs.

![Regional Salary Comparison](/0_Resources/Images/2_Project_Analysis_Chart2.png)

### Interpretation

Geographic location remains a major factor in salary expectations. Countries with larger technology ecosystems appear to provide stronger compensation for advanced data roles.

---

# 3️⃣ Most In-Demand Skills in Data Jobs

## 💪 Data Modeling with Power Pivot

A relationship was created between:

* `data_jobs_all`
* `data_job_skills`

using the `job_id` field.

This allowed skill-level analysis across different job categories.

---

## Data Model Structure

![Data Model](/0_Resources/Images/2_Project_Analysis_Screenshot5.png)

---

## Power Pivot Environment

![Power Pivot](/0_Resources/Images/2_Project_Analysis_Screenshot6.png)

---

## 📊 Findings

### Key Insights

* SQL and Python appeared most frequently across data-related positions.
* Cloud technologies such as AWS and Azure showed strong demand growth.
* Technical skills related to databases and automation remained highly valuable.

![Top Skills Chart](/0_Resources/Images/2_Project_Analysis_Chart3.png)

### Interpretation

The analysis highlights the importance of foundational technical skills in modern data careers. SQL, Python, and cloud platforms continue to dominate employer requirements across multiple job categories.

---

# 4️⃣ Salary Impact of Top Skills

## 📈 Advanced Pivot Chart Analysis

A combination PivotChart was used to compare:

* Median Salary
* Skill Likelihood (%)

### Visualization Design

* Clustered columns represented salary values
* A secondary axis displayed skill frequency
* Marker styling was adjusted to improve readability

---

## 📊 Findings

### Key Insights

* Skills such as Python, SQL, and Oracle were associated with higher salary ranges.
* General office tools like Word and PowerPoint showed lower salary correlations.
* Specialized technical expertise appears to have stronger compensation potential.

![Top Skills Salary Chart](/0_Resources/Images/2_Project_Analysis_Chart4.png)

### Interpretation

The results indicate that technical specialization plays an important role in salary growth. Data professionals investing in high-demand technologies may improve both employability and compensation opportunities.

---

# Conclusion

This project demonstrates how Excel can be used to perform end-to-end data analysis, from data cleaning and transformation to modeling and visualization.

Through this analysis, several trends became clear:

* Technical specialization is strongly linked to higher salaries
* SQL and Python remain essential industry skills
* Regional salary differences are significant across data roles
* Cloud technologies continue to grow in importance

The project also strengthened practical skills in:

* Power Query
* Pivot Tables
* DAX
* Power Pivot
* Data Visualization
* Analytical storytelling

Overall, this analysis provides a clearer understanding of current trends in the data job market and the skills that appear most valuable for career growth.
