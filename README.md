# Economic Factors & Consumption
DSA210_TermProject

# Introduction
This project explores the relationship between key economic factors such as unemployment rates, inflation, inflation-adjusted housing prices, and historical wartime periods with personal consumption expenditure. Our goal is to determine the extent to which these macroeconomic indicators influence consumer spending habits over time and whether they exhibit seasonal patterns. The study focuses on three major economies: Canada, the United States, and the United Kingdom.

Personal consumption expenditure (PCE) is a vital economic indicator, reflecting the overall economic health of a country. Fluctuations in PCE often correlate with economic downturns, periods of inflation, labor market shifts, and major historical events such as wars. By analyzing these factors across different countries and economic conditions, this study aims to provide deeper insights into consumer behavior, macroeconomic trends, and the economic impact of wartime periods.

# Motivation
Macroeconomic conditions significantly impact individuals' purchasing power and spending behavior. Understanding these relationships is crucial for policymakers, economists, businesses, and consumers alike. The research aims to address several critical questions:
- How do inflation rates, unemployment levels, and housing prices collectively influence personal consumption expenditure?
- Do specific economic indicators have a stronger impact on PCE than others?
- Can we identify recurring seasonal patterns in economic shifts and their effects on consumer behavior?
- Are there country-specific variations in how economic factors influence spending habits, or do similar trends emerge across multiple economies?
- How do real residential property prices impact consumer confidence and expenditure patterns?
- What is the role of war as an economic factor, and how does it affect personal consumption trends?
- How do wartime periods impact inflation, unemployment, and consumer spending behavior in Canada, the US, and the UK?

Examining these questions can help provide more accurate economic forecasts, guide monetary policies, and assist businesses in strategic planning.

# Project Goal
The central objective of this project is to establish empirical relationships between macroeconomic variables, historical wartime periods, and personal consumption expenditure. Specifically, we aim to:
- Examine historical trends to determine the impact of economic factors on personal consumption across different time periods.
- Identify seasonal patterns in consumer spending based on quarterly data.
- Compare findings across three countries to determine the similarities and differences in economic behavior.
- Apply statistical models to assess the predictive power of economic indicators on future personal consumption trends.
- Investigate how changes in real residential property prices affect consumer confidence and personal consumption.
- Analyze how wartime events influence macroeconomic trends and personal consumption behavior.

# Data Sources  

| #  | Data Type | Country | Source Link | Years Covered |
|----|------------|---------|-------------|---------------|
| 1  | Personal Consumption Expenditure | Canada | [Link](https://fred.stlouisfed.org/series/NCRSAXDCCAQ) | 1961-2024 |
| 2  | Personal Consumption Expenditure | US | [Link](https://fred.stlouisfed.org/series/NCRSAXDCUSQ) | 1970-2024 |
| 3  | Personal Consumption Expenditure | UK | [Link](https://fred.stlouisfed.org/series/NCRSAXDCGBQ) | 1995-2024 |
| 4  | Unemployment Rate | Canada | [Link](https://fred.stlouisfed.org/series/LRUNTTTTCAM156S) | 1955-2025 |
| 5  | Unemployment Rate | US | [Link](https://fred.stlouisfed.org/series/UNRATE) | 1948-2025 |
| 6  | Unemployment Rate | UK | [Link](https://fred.stlouisfed.org/series/LRUNTTTTGBQ156S) | 1971-2024 |
| 7  | Inflation | Canada | [Link](https://fred.stlouisfed.org/series/FPCPITOTLZGCAN) | 1960-2023 |
| 8  | Inflation | US | [Link](https://fred.stlouisfed.org/series/FPCPITOTLZGUSA) | 1960-2023 |
| 9  | Inflation | UK | [Link](https://fred.stlouisfed.org/series/FPCPITOTLZGGBR) | 1960-2023 |
| 10 | Real Residential Property Prices | Canada | [Link](https://fred.stlouisfed.org/series/QCAR628BIS) | 1970-2024 |
| 11 | Real Residential Property Prices | US | [Link](https://fred.stlouisfed.org/series/QUSR368BIS) | 1970-2024 |
| 12 | Real Residential Property Prices | UK | [Link](https://fred.stlouisfed.org/series/QGBR368BIS) | 1969-2024 |

These datasets cover multiple years, allowing for a robust analysis of long-term trends and short-term fluctuations in economic indicators, particularly during wartime periods.

# Methodology
1. **Data Cleaning & Preprocessing:**
   - Handle missing values and ensure consistency across datasets.
   - Convert all data to a common time format.
2. **Exploratory Data Analysis (EDA):**
   - Compute summary statistics and visualize data.
   - Identify potential correlations between variables.
3. **Statistical Analysis & Hypothesis Testing:**
   - Conduct regression analysis to quantify relationships.
   - Perform seasonal decomposition to detect periodic patterns.
   - Assess the economic impact of  inflation on employment, and consumption trends.
4. **Machine Learning Models (if applicable):**
   - Train predictive models to forecast personal consumption expenditure based on economic indicators and historical wartime events.
  


## Findings

### Missing Value Analysis

After loading and consolidating the full dataset, we performed a missing‐value analysis for each country. The results below show that **no** missing values were found in any of the key variables for Canada, the UK, or the USA—hence, no imputation was necessary.

#### Canada
| Variable                   | Missing Count | Missing Percentage (%) |
|----------------------------|--------------:|-----------------------:|
| Year                       |             0 |                    0.0 |
| Property_Prices            |             0 |                    0.0 |
| Unemployment_Rate          |             0 |                    0.0 |
| Inflation                  |             0 |                    0.0 |
| Consumption_Expenditure    |             0 |                    0.0 |

#### UK
| Variable                   | Missing Count | Missing Percentage (%) |
|----------------------------|--------------:|-----------------------:|
| Year                       |             0 |                    0.0 |
| Property_Prices            |             0 |                    0.0 |
| Unemployment_Rate          |             0 |                    0.0 |
| Inflation                  |             0 |                    0.0 |
| Consumption_Expenditure    |             0 |                    0.0 |

#### USA
| Variable                   | Missing Count | Missing Percentage (%) |
|----------------------------|--------------:|-----------------------:|
| Year                       |             0 |                    0.0 |
| Property_Prices            |             0 |                    0.0 |
| Unemployment_Rate          |             0 |                    0.0 |
| Inflation                  |             0 |                    0.0 |
| Consumption_Expenditure    |             0 |                    0.0 |

> **Note:** Since there were no missing observations, we proceeded to the next phase without any imputation.

### Outlier Analysis (IQR Method)

We tested each feature for outliers using the Interquartile Range (IQR) method. Whenever a feature’s outlier rate exceeded 5 %, we planned to apply Winsorizing to cap extreme values.

#### Canada
| Feature                   | Outlier Count | Outlier Percentage (%) |
|---------------------------|--------------:|-----------------------:|
| Property_Prices           |             2 |                   3.70 |
| Unemployment_Rate         |             1 |                   1.85 |
| Inflation                 |             5 |                   9.26 |
| Consumption_Expenditure   |             0 |                   0.00 |

#### UK
| Feature                   | Outlier Count | Outlier Percentage (%) |
|---------------------------|--------------:|-----------------------:|
| Property_Prices           |             1 |                   3.45 |
| Unemployment_Rate         |             0 |                   0.00 |
| Inflation                 |             2 |                   6.90 |
| Consumption_Expenditure   |             0 |                   0.00 |

#### USA
| Feature                   | Outlier Count | Outlier Percentage (%) |
|---------------------------|--------------:|-----------------------:|
| Property_Prices           |             1 |                   1.89 |
| Unemployment_Rate         |             0 |                   0.00 |
| Inflation                 |             5 |                   9.43 |
| Consumption_Expenditure   |             0 |                   0.00 |

> **Note:**  
> - Inflation in both Canada (9.26 %) and the USA (9.43 %) exceeded our 5 % threshold, so we applied Winsorizing to those distributions.  
> - All other features had outlier rates below 5 %, so they remained unchanged.

### Correlation Analysis

After cleaning and handling outliers, we examined the pairwise correlations between our key economic indicators for Canada. Below is the heatmap visualization and the corresponding numeric matrix.

#### Heatmap (Canada)  
![Correlation Matrix (Heatmap) - Canada](outputs/corr_heatmap_canada.png)

#### Canada Correlation Matrix

|                          | Inflation | Unemployment_Rate | Property_Prices | Consumption_Expenditure |
|--------------------------|----------:|------------------:|----------------:|------------------------:|
| **Inflation**            |      1.00 |             -0.05 |           -0.37 |                   -0.56 |
| **Unemployment_Rate**    |     -0.05 |              1.00 |           -0.37 |                   -0.31 |
| **Property_Prices**      |     -0.37 |             -0.37 |            1.00 |                    0.94 |
| **Consumption_Expenditure** |  -0.56 |             -0.31 |            0.94 |                    1.00 |

> **Key observations:**  
> - **Property_Prices ↔ Consumption_Expenditure (0.94):** Very strong positive correlation, indicating that rising property prices tend to coincide with higher consumption expenditure.  
> - **Inflation ↔ Consumption_Expenditure (-0.56):** Moderate negative correlation, suggesting that higher inflation is associated with reduced consumption spending.  
> - **Inflation ↔ Unemployment_Rate (-0.05):** Near-zero correlation, implying little linear relationship between these two variables in our sample.  

This analysis guided our feature-selection and modeling decisions in subsequent phases.

