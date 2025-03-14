# Economic Factors & Consumption
DSA210_TermProject
# Economic Factors and Their Impact on Personal Consumption Expenditure

# Introduction
This project explores the relationship between key economic factors—such as unemployment rates, inflation, and inflation-adjusted housing prices—and personal consumption expenditure. Our goal is to determine the extent to which these macroeconomic indicators influence consumer spending habits over time and whether they exhibit seasonal patterns. The study focuses on three major economies: Canada, the United States, and the United Kingdom.

Personal consumption expenditure (PCE) is a vital economic indicator, reflecting the overall economic health of a country. Fluctuations in PCE often correlate with economic downturns, periods of inflation, and labor market shifts. By analyzing these factors across different countries and economic conditions, this study aims to provide deeper insights into consumer behavior and macroeconomic trends.

# Motivation
Macroeconomic conditions significantly impact individuals' purchasing power and spending behavior. Understanding these relationships is crucial for policymakers, economists, businesses, and consumers alike. The research aims to address several critical questions:
- How do inflation rates, unemployment levels, and housing prices collectively influence personal consumption expenditure?
- Do specific economic indicators have a stronger impact on PCE than others?
- Can we identify recurring seasonal patterns in economic shifts and their effects on consumer behavior?
- Are there country-specific variations in how economic factors influence spending habits, or do similar trends emerge across multiple economies?
- How do real residential property prices impact consumer confidence and expenditure patterns?

Examining these questions can help provide more accurate economic forecasts, guide monetary policies, and assist businesses in strategic planning.

# Project Goal
The central objective of this project is to establish empirical relationships between macroeconomic variables and personal consumption expenditure. Specifically, we aim to:
- Examine historical trends to determine the impact of economic factors on personal consumption across different time periods.
- Identify seasonal patterns in consumer spending based on quarterly data.
- Compare findings across three countries to determine the similarities and differences in economic behavior.
- Apply statistical models to assess the predictive power of economic indicators on future personal consumption trends.
- Investigate how changes in real residential property prices affect consumer confidence and personal consumption.

# Data Sources
The project utilizes publicly available data from multiple economic sources:
- **Personal Consumption Expenditure Data:**
  - Canada: `Real Final Consumption Expenditure for Canada.csv`
  - United States: `Real Final Consumption Expenditure for US.csv`
  - United Kingdom: `Real Final Consumption Expenditure for United Kingdom.csv`
- **Unemployment Rate Data:**
  - Canada: `Unemployment Rate Total in Canada.csv`
  - United States: `Unemployment Rate Total in US.csv`
  - United Kingdom: Extracted from `Data_Extract_FromWorld Development Indicators.xlsx`
- **Inflation Data:**
  - Canada: `Inflation, consumer prices for Canada.csv`
  - United States: `Inflation, consumer prices for United States.csv`
  - United Kingdom: `Inflation, consumer prices in UK.xlsx`
- **Real Residential Property Prices:**
  - Canada: `Real Residential Property Prices for Canada.csv`
  - United States: `Real Residential Property Prices for US.xlsx`
  - United Kingdom: `Real Residential Property Prices UK.csv`

These datasets cover multiple years, allowing for a robust analysis of long-term trends and short-term fluctuations in economic indicators.

# Methodology
1. **Data Cleaning & Preprocessing:**
   - Handle missing values and ensure consistency across datasets.
   - Convert all data to a common time format (quarterly basis).
2. **Exploratory Data Analysis (EDA):**
   - Compute summary statistics and visualize trends in the data.
   - Identify potential correlations between variables.
3. **Statistical Analysis & Hypothesis Testing:**
   - Conduct regression analysis to quantify relationships.
   - Perform seasonal decomposition to detect periodic patterns.
   - Analyze the correlation between real residential property prices and personal consumption expenditure.
4. **Machine Learning Models (if applicable):**
   - Train predictive models to forecast personal consumption expenditure based on economic indicators.

