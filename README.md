# Macroeconomic Drivers of Health: An Econometric EDA of Global Development

## Objective
This project moves beyond standard exploratory data analysis by applying econometric principles to the Gapminder dataset. The goal is to analyze the non-linear relationship between a nation's wealth (GDP per capita) and public health outcomes (Life Expectancy), treating the data as an unbalanced panel.

## Methodology & Assumptions
1.  **Data Cleaning:** Addressed missing values inherent in historical panel data using country-level forward filling, ensuring time-series continuity.
2.  **Transformations:** GDP per capita exhibits extreme right-skewness. To satisfy linearity assumptions for correlation and regression, a logarithmic transformation was applied.
3.  **Baseline Econometric Model:** A simple cross-sectional OLS regression was fitted to the most recent year's data to quantify the elasticity of life expectancy with respect to GDP.
4.  **Interactivity:** Used Plotly to recreate Hans Rosling's famous animated bubble chart, allowing users to track development trajectories over decades.

## Key Insights
* **The Wealth-Health Diminishing Return:** The relationship between GDP per capita and Life Expectancy is strictly logarithmic. Moving from a GDP of $1,000 to $10,000 yields massive gains in life expectancy, whereas moving from $40,000 to $50,000 yields marginal returns.
* **Regional Clustering:** Sub-Saharan African nations cluster heavily in the lower-left quadrant (low GDP, low life expectancy), though the trajectory from 1950-2007 shows a clear, albeit slow, upward shift.
* **Statistical Significance:** The OLS regression indicates that $\ln(GDP)$ explains a significant majority of the variance in global life expectancy.

## Tech Stack
* **Python:** Pandas for manipulation, NumPy for transformations.
* **Visualization:** Matplotlib/Seaborn for static publication-ready charts, Plotly Express for interactive dashboarding.
* **Statistics:** Statsmodels for OLS regression summaries.
