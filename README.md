# SQL Data Cleaning and EDA

## Overview
This project involves analyzing global layoffs data using SQL. The goal is to clean, standardize, and explore the dataset to extract meaningful insights. The project is divided into three main parts:
- **Data Cleaning**: Removing duplicates, handling null values, standardizing data, and correcting anomalies.
- **Data Transformation**: Creating a staging table, adding necessary columns, and formatting the date field.
- **Exploratory Data Analysis (EDA)**: Identifying key trends such as layoffs by company, industry, and country.

---
## Database and Table Used
- **Database**: `world_layoffs`
- **Table**: `layoffs` (original) → `layoffs_Staging2` (cleaned version)

---
## 1️⃣ Data Cleaning
### **Steps Taken:**
### 🔹 Creating a Staging Table
- Created a duplicate table (`layoffs_Staging2`) to avoid modifying the original data.
- Data from the original table was inserted into the staging table.

### 🔹 Removing Duplicates
- A unique `ID` column for identification was added, and after work done deleated
- Used `ROW_NUMBER()` to find and delete duplicate rows.

### 🔹 Standardizing Data
- Trimmed and corrected `location` values.
- Standardized industry names (e.g., "Crypto currency" → "Crypto").
- Corrected country name anomalies (e.g., "United States." → "United States").

### 🔹 Formatting Date Column
- Updated the date format to ensure consistency.
- Changed the data type of the `date` column to `DATE`.

### 🔹 Handling NULL and Blank Values
- Updated blank `industry` values using data from matching company-location pairs.
- Removed rows where both `total_laid_off` and `percentage_laid_off` were NULL.

---
## 2️⃣ Exploratory Data Analysis (EDA)
### 🔹 Key Insights and Queries

**1️⃣ Maximum Layoffs and Highest Layoff Percentage**
- Identified the highest recorded layoffs and the maximum percentage of layoffs.

**2️⃣ Companies with 100% Layoffs**
- Filtered records where all employees were laid off and sorted them by total layoffs.

**3️⃣ Total Layoffs by Company**
- Aggregated and sorted companies by the highest number of layoffs.

**4️⃣ Layoffs by Industry, Country, and Year**
- Analyzed total layoffs across different industries, countries, and years.

**5️⃣ Rolling Total of Layoffs by Month**
- Computed a cumulative sum of layoffs per month to observe trends over time.

**6️⃣ Top 5 Companies with the Most Layoffs per Year**
- Used ranking techniques to find the top five companies with the highest layoffs each year.

**7️⃣ Top 5 Industries with Most Layoffs per Month**
- Ranked the top five industries with the most layoffs in each month of every year.

---
## Conclusion
This project provides a structured approach to **cleaning, transforming, and analyzing layoffs data**. By leveraging SQL, we:
✅ Removed duplicates and inconsistencies.  
✅ Standardized and corrected anomalies.  
✅ Explored key trends in layoffs across companies, industries, and countries.  
✅ Computed rolling totals and ranked top entities based on layoffs.


---
## Future Enhancements
- Implement visualizations in Power BI or Tableau.
- Add forecasting models to predict future layoffs trends.
- Integrate external economic factors for deeper insights.

---
### 🚀 **Author**: Abhishek Mahadev Raut  
### 📅 **Date**: March 2025 -- Cleaning and EDA complete



