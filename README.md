# Taiwan vs Japan Starting Salary Analysis

A comprehensive statistical analysis comparing starting salaries for new graduates between Taiwan and Japan across different education levels and industries, adjusted for purchasing power parity (PPP).

## Project Overview

This project analyzes and compares starting salaries between Taiwan and Japan to answer key research questions:
- Is there a significant salary difference between Japan and Taiwan?
- Does higher education lead to salary increases within each country?
- How do salaries compare across countries for the same education level?
- What are the salary variations across different industries?

## Project Structure

```
wage-1/
├── df_combined.csv           # Combined dataset for analysis
├── df_jp_long.csv            # Japan salary data (long format)
├── df_jp_wide.csv            # Japan salary data (wide format)
├── df_tw_long.csv            # Taiwan salary data (long format)
├── df_tw_wide.csv            # Taiwan salary data (wide format)
├── EDA.ipynb                 # Exploratory Data Analysis notebook
├── jp.ipynb                  # Japan-specific analysis
├── tw.ipynb                  # Taiwan-specific analysis
├── sql_analysis.ipynb        # SQL-based data queries and aggregations
├── wage_analysis.R           # Statistical testing (t-tests, ANOVA)
├── regression_analysis.R     # Linear regression models
└── README.md                 # This file
```

## Analysis Methods

### 1. **Exploratory Data Analysis (EDA.ipynb)**
- Data loading and preprocessing
- Descriptive statistics
- Visualization of salary distributions
- PPP-adjusted real salary calculations

### 2. **Statistical Testing (wage_analysis.R)**
- **Independent t-tests**: Compare salaries between countries
- **Paired t-tests**: Compare education levels within countries
- Analysis of nominal vs real (PPP-adjusted) salaries

### 3. **Regression Analysis (regression_analysis.R)**
- Linear regression models examining factors affecting salary
- Models include:
  - Education level
  - Country
  - Industry category
  - Interaction effects
- Coefficient visualization and interpretation

### 4. **SQL Analysis (sql_analysis.ipynb)**
- Aggregate queries for weighted averages
- Industry salary ranges
- Cross-tabulation by country and education

## Requirements

### Python
```bash
pandas
numpy
matplotlib
seaborn
pandasql
sqlite3
```

### R
```r
tidyverse
rstatix
effsize
stargazer
coefplot
knitr
```

## Usage

### Python Analysis
```bash
# Run Jupyter notebooks
jupyter notebook EDA.ipynb
jupyter notebook sql_analysis.ipynb
```

### R Analysis
```r
# Run in R or RStudio
source("wage_analysis.R")
source("regression_analysis.R")
```

## Data Sources

- **Taiwan**: Ministry of Labor salary survey data for new graduates
- **Japan**: Ministry of Health, Labour and Welfare employment statistics
- **PPP Conversion**: OECD purchasing power parity indices

## Notes

- All salaries are calculated for new graduates (starting positions)
- Real salaries are adjusted using PPP conversion rates
- Education levels: Junior College, University, Graduate School
- Industry categories vary by country's classification system

## Author

yichieh6

## License

This project is available for educational and research purposes.