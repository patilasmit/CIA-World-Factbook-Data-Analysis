# CIA World Factbook Data Analysis

## Project Overview
This project involves analyzing data from the **CIA World Factbook**, which provides comprehensive information on countries around the world. The dataset includes various metrics such as population, area, GDP, demographics, and more. By leveraging SQL queries, this analysis seeks to uncover meaningful insights related to global demographics and economics.

## Objectives
- **Data Exploration**: Understand the structure and content of the CIA World Factbook dataset.
- **Data Cleaning**: Handle any missing values, inconsistencies, and ensure data integrity.
- **Analysis Tasks**:
  1. Identify the country with the highest population.
  2. Determine the country with the least number of people.
  3. Analyze which country is witnessing the highest population growth.
  4. Investigate which country has an extraordinary number for the population.
  5. Find the most densely populated country in the world.

## Tools Used
- **Database**: MySQL, PostgreSQL, SQLite, or any other SQL database management system.
- **IDE**: SQL Workbench, pgAdmin, or other database management tools.

## Dataset
- **Source**: The CIA World Factbook dataset can be obtained from various sources, such as Kaggle, the official CIA website, or other data repositories.
- **Structure**: The dataset includes a single table with columns such as:
  - `Country`
  - `Population`
  - `Area`
  - `GDP`
  - `Population Growth Rate`

## SQL Skills Demonstrated
- **Data Querying**: Using SQL commands such as `SELECT`, `FROM`, `WHERE`, `GROUP BY`, `JOIN`, etc.
- **Aggregation Functions**: Implementing functions like `SUM`, `COUNT`, `AVG` for data analysis.
- **Subqueries**: Utilizing nested queries for complex analysis tasks.
- **Data Cleaning Techniques**: Addressing null values and inconsistencies in the dataset.
- **Statistical Calculations**: Performing calculations and comparisons for insights.

## Analysis Queries

### Key Queries
1. **Which country has the highest population?**
   ```sql
   SELECT Country, Population
   FROM WorldFactbook
   ORDER BY Population DESC
   LIMIT 1;
   ```

2. **Which country has the least number of people?**
   ```sql
   SELECT Country, Population
   FROM WorldFactbook
   ORDER BY Population ASC
   LIMIT 1;
   ```

3. **Which country is witnessing the highest population growth?**
   ```sql
   SELECT Country, Population_Growth_Rate
   FROM WorldFactbook
   ORDER BY Population_Growth_Rate DESC
   LIMIT 1;
   ```

4. **Which country has an extraordinary number for the population?**
   ```sql
   SELECT Country, Population
   FROM WorldFactbook
   WHERE Population > 1_000_000_000;  -- Adjust the threshold as necessary
   ```

5. **Which is the most densely populated country in the world?**
   ```sql
   SELECT Country, (Population / Area) AS Density
   FROM WorldFactbook
   ORDER BY Density DESC
   LIMIT 1;
   ```

## Conclusion
This SQL portfolio project on **CIA World Factbook data analysis** demonstrates proficiency in handling real-world datasets and deriving meaningful insights using SQL. The project showcases the ability to manipulate and analyze large datasets related to global demographics and economics, highlighting the power of SQL in data exploration and analysis.
