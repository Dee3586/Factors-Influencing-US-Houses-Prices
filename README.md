# README: Factors Influencing US House Prices Analysis

![Image](https://github.com/user-attachments/assets/e946c659-b0b1-4e50-8a61-358c55f5aee6)    ![175929181-c0cac550-caba-4313-b257-50b69d5060c8](https://github.com/user-attachments/assets/7135fbc9-2141-4cb0-a8dd-e52ad42baf3d)


## Project Overview
This Excel-based project investigates the most significant economic and demographic factors that influence house prices in the United States. Using 240 data points, regression analysis, correlation functions, pivot tables, and Excel visualizations, we identify which variables most strongly affect the U.S. housing market.

---

## Key Research Questions and Answers

1. **What are the most significant economic and demographic factors that influence house prices in the United States?**
   - Statistically significant factors (p < 0.05):
     - const_price_index
     - delinquency_rate
     - GDP
     - house_for_sale_or_sold
     - housing_subsidies
     - income
     - interest_rate
     - construction_unit
     - total_houses
     - unemployment_rate
     - urban_population
   - Less significant:
     - building_permits (p = 0.20)
     - mortgage_rate (p = 0.09)
     - total_const_spending (p = 0.94)

2. **How does total construction spending correlate with changes in house prices?**
   - Very weak correlation (coefficient = 0.0185, p = 0.9366). Not statistically significant.

3. **Does the number of new construction units or building permits significantly impact house prices?**
   - construction_unit is significant (p = 0.00008). Positive effect.
   - building_permits is not significant (p = 0.20).

4. **What is the relationship between the Construction Price Index and average house prices over time?**
   - Strong positive relationship. Coefficient = 0.5668, p < 0.00001.

5. **Is there a correlation between the total number of houses available and fluctuations in house prices?**
   - Significant negative relationship. Coefficient = -0.0033, p = 6.66E-05.

6. **How do GDP growth and income levels influence house prices?**
   - GDP has a small positive effect (p = 0.0136).
   - Income has a small but significant negative effect (p = 0.0046), likely due to affordability pressure.

7. **To what extent does the unemployment rate affect the housing market?**
   - Unemployment_rate has a positive coefficient (2.1184, p = 0.00004). Could reflect countercyclical policy effects.

8. **What impact does the delinquency rate have on house prices?**
   - Strong negative impact. Coefficient = -2.8882, p = 1.56E-12.

9. **How do mortgage rates and interest rates affect home affordability and prices?**
   - interest_rate is strongly significant (p = 2.24E-16), coefficient = 4.0638.
   - mortgage_rate is not significant (p = 0.0935).

10. **What is the effect of urban population growth on house prices?**
    - Strong positive effect. Coefficient = 20.5894, p = 0.0051.

---

## Excel Tools Used

### Regression Analysis (via Data Analysis ToolPak)
- Go to: Data > Data Analysis > Regression
- Y Range: house_price_index
- X Range: building_permits through urban_population
- Output includes:
  - Multiple R: 0.9945
  - R²: 0.989
  - Adjusted R²: 0.988
  - Significance F: 2.24E-211

### Correlation Matrix
- Formula: =CORREL(array1, array2)
  Example: =CORREL(B2:B241, C2:C241)

### Pivot Tables
- Example 1:
  - Rows: Year or Quarter
  - Columns: Region
  - Values: Average house_price_index
- Example 2:
  - Rows: Affordability Band (use grouping on calculated affordability)
  - Values: Average house_price_index

### Excel Visualizations
- Charts:
  - Line chart for house price trends
  - Scatter plots with trendlines (e.g., const_price_index vs house_price_index)
- Conditional Formatting:
  - Color scales for delinquency_rate or interest_rate spikes
  - Data bars for affordability scores

---

## Formulas Used

### Correlation
=CORREL(array1, array2)

### Affordability Score
=income / (house_price_index * mortgage_rate)

### Percentage Change in Prices
=(CurrentPrice - PreviousPrice) / PreviousPrice

### Line of Best Fit in Chart
- Insert scatter plot > Add Trendline > Show Equation and R²

---

## Regression Output Summary

Regression Statistics:
- Multiple R: 0.9945
- R²: 0.989
- Adjusted R²: 0.988
- Observations: 240

ANOVA:
- df = 14, F = 1439.22, Significance F = 2.24E-211

Coefficients:
| Variable                 | Coefficient | P-value     |
|--------------------------|-------------|-------------|
| Intercept                | -1335.8789  | 0.0052      |
| building_permits         | 0.0036      | 0.1973      |
| const_price_index        | 0.5668      | 2.47E-55 ✔  |
| delinquency_rate         | -2.8882     | 1.56E-12 ✔  |
| GDP                      | 0.0050      | 0.0136 ✔    |
| house_for_sale_or_sold   | -0.0929     | 0.0205 ✔    |
| housing_subsidies        | 1.2722      | 0.0002 ✔    |
| income                   | -0.0027     | 0.0046 ✔    |
| interest_rate            | 4.0638      | 2.24E-16 ✔  |
| mortgage_rate            | 1.2643      | 0.0935      |
| construction_unit        | 0.0153      | 7.95E-05 ✔  |
| total_houses             | -0.0033     | 6.66E-05 ✔  |
| total_const_spending     | 0.0185      | 0.9366      |
| unemployment_rate        | 2.1184      | 4.16E-05 ✔  |
| urban_population         | 20.5894     | 0.0051 ✔    |

✔ = Statistically significant

---

## Summary

- The Excel model explains 99% of house price variance (R² = 0.989).
- Key drivers: Construction Price Index, Urban Population, Delinquency Rate, Unemployment, Interest Rates, Construction Units.
- Excel provided full modeling, correlation, and visualization capacity without external code or scripts.

---

Project completed entirely in Microsoft Excel using native statistical tools and visualization features.
I am open to collaborate on projects related to Data Analysis Statistical Analysis, and Visualization . You can reach me via my email [dammythompson23@gmail.com]
