# US SWE Salaries Analysis Project

You can access the application via [Link](https://guochenliao.shinyapps.io/swe_salary_analysis/).
## 1. Project Purpose
The project aims to analyze the economic landscape for software developers across US states by examining their salaries and other financial metrics. It seeks to understand the financial advantages and disparities within the SWE compared to other careers.

## 2. Data Description + How was the Data Collected?
### Data Description
- The dataset contains **12 columns** and **77 rows**, representing various financial metrics and specific city data.
- Metrics include adjusted and unadjusted salaries for software developers, median home prices, cost of living, rent, and local purchasing power.

### Data Collection
- The dataset is an aggregation of various datasets, providing different perspectives and insights into software developer salaries.
- It includes symbolic data (city names and states) and numeric data (financial metrics).

## 3. Target Users
This interactive App is designed for:
- Software Developers: To understand the economic landscape of their profession across different US states.
- Data Analysts and Economists: To analyze and compare the financial metrics related to the software development profession.
- Job Seekers: To identify financially advantageous locations for software development careers.

## 4. Questions Trying to Answer
- How does the salary of SWEs compare across different states?
- What is the percentage of salary for SWEs over other professions?
- What is the percentage of rent over salary for SWEs compared with other professions?


## 5. Insights from Data
- The rent constitutes approximately 21.4% of the total salary for a SWE, contrasting with 39.5% for average salaries across all careers.
- There is a notable discrepancy in the salary structures between software engineers and other professions, highlighting potential financial advantages associated with a career in software development.

## 6. Improvement Wishlist
- Date Expansion: Include data from different years to show how the financial metrics change over time for SWEs.
- Additional Metrics: Integrate more financial metrics, such as tax rates, to provide a comprehensive financial overview.
- User Interface: Add histogram page at the dashboard for better visualization

## 7. Sources or References
- [1] T. Devastator, “U.S. software developer salaries,” Kaggle, https://www.kaggle.com/datasets/thedevastator/u-s-software-developer-salaries (accessed Oct. 9, 2023) [Link](https://www.kaggle.com/datasets/thedevastator/u-s-software-developer-salaries). 
- [2] F. S. Bruno Bonfrisco, “Sofware developer income/expenses per USA City,” Zenodo, https://doi.org/10.5281/zenodo.7412091 (accessed Oct. 9, 2023).  [Link](https://doi.org/10.5281/zenodo.7412091).
- [3] U. C. Bureau, “Tiger/line shapefiles,” Census.gov, https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html (accessed Oct. 10, 2023). 

## 8. Data Tidying and Pre-processing
- The data is read from a CSV file named `SweSalaries.csv`.
- The `City` column is separated into two distinct columns: `City_Name` and `State_Name`.
- The data is then grouped by `State_Name` to calculate averages for various financial metrics.
- The following R libraries are used for processing and visualizing the data:
  - `readr`, `dplyr`, `tidyr`, `magrittr`, `ggplot2`, `qrcode`, `lattice`, `wordcloud2`, `shiny`, `leaflet`, `maps`, `sf`, `shinydashboard`.

## 9. Design Decisions

### 1. **What**
- Datasets: The primary dataset is a table of SWE salaries across different US cities.
- Attributes: The dataset contains quantitative attributes like salaries, rent, home prices, and more.

### 2. **Why**
- Target: Analyzing patterns in SWE salaries, comparing salaries across states, and visualizing the relationship between different financial metrics.

### 3. **How**
- Encode: The data is encoded using bar plots, scatter plots, bubble plots, and box plots.
  - Bar Plots: Used to visualize the top 10 states based on average adjusted salaries.
  - Scatter Plots: Used to visualize the relationship between home prices and mean salaries, and between rent and mean adjusted salaries.
  - Bubble Plots: Used to visualize the relationship between rent and mean adjusted salaries, with the size of the bubbles representing the rent-to-salary ratio.
  - Box plots: Used to visualize the relationship between mean adjusted salaries and living cost, where the salaries are categorized into three levels.
- Reduce: Data is aggregated by state to provide a summarized view.
- Facet: The Shiny app provides multiple views (map and line graph) to allow users to explore different facets of the data.

## 10. Appendix
- Time Log Chart:
![Working time log](https://github.com/Mark-Liao305/CSC324/assets/85295108/c71c14f9-a7f5-4492-ab87-b4ffe17dc412)
