# Trade Shocks and Inflation Sensitivity Analysis

## Overview

This project analyzes the sensitivity of inflation to trade cost shocks (e.g., tariffs or logistics disruptions) across consumable vs. non-consumable goods. The research investigates whether consumable goods are more sensitive to trade shocks and if they contribute more significantly to inflation volatility compared to non-consumable goods.

## Research Question

Are consumable goods more sensitive to trade cost shocks (e.g., tariffs or logistics disruptions) than non-consumables, and do they contribute more to inflation volatility?

## Datasets

The analysis uses three main datasets:

1. **Trade Data**: 
   - CIF (Cost, Insurance, and Freight) values for imports into the USA
   - Disaggregated by product category based on HS codes
   - Separated into consumable and non-consumable data files

2. **Inflation Data**:
   - Yearly CPI inflation data for the USA from World Bank
   - Additional global inflation data for cross-country analysis

## Project Structure

The analysis follows these main steps:

1. **Environment Setup**: 
   - Import necessary libraries
   - Configure visualization parameters

2. **Data Loading**:
   - Import trade data for consumable goods
   - Import trade data for non-consumable goods
   - Import total trade data
   - Import inflation data

3. **Data Preparation**:
   - Aggregate trade data by year and category
   - Extract USA inflation data
   - Calculate year-to-year percent changes
   - Create derived variables for analysis
   - Merge trade and inflation datasets

4. **Exploratory Data Analysis**:
   - Visualize relationships between key variables
   - Perform correlation analysis
   - Analyze distributions of key metrics
   - Examine time series patterns
   - Create standardized comparisons using z-scores

5. **Modeling**:
   - Develop OLS regression models for inflation sensitivity
   - Implement Bayesian regression for inflation volatility
   - Conduct model diagnostics and evaluation
   - Generate predictions with confidence intervals

6. **Scenario Analysis**:
   - Test various trade shock scenarios
   - Create visualization of scenario results
   - Develop 3D prediction surfaces
   - Generate contour plots and sensitivity charts

7. **Cross-Country Analysis**:
   - Build country-specific models
   - Visualize patterns across regions and income groups
   - Create heatmaps showing most sensitive countries
   - Analyze regional and development status influences

## Key Findings

1. **Consumable Goods Impact**: Consumable goods have a significantly stronger effect on inflation changes. The coefficient for consumable imports (0.3295) is statistically significant, with a p-value of 0.049.

2. **Non-consumable Goods**: Non-consumable imports show a weaker relationship with inflation changes. The coefficient (-0.0398) is not statistically significant (p=0.657).

3. **Sensitivity Ratio**: Consumable goods are approximately 8 times more impactful than non-consumable goods on inflation changes.

4. **Volatility Analysis**: Trade shocks in consumable goods can significantly amplify inflation volatility, creating dangerous feedback loops in the economy.

5. **Cross-Country Patterns**: The relationship between trade shocks and inflation is consistent across different economies, with regional patterns showing shared inflation vulnerabilities.

6. **Temporal Lag**: Inflation appears to respond to trade shocks with approximately a one-period lag, providing a crucial forecasting window for policy interventions.

7. **Non-linear Effects**: Inflation response to consumable trade shocks shows a tipping point at approximately ±10%, where the effect begins to accelerate.

## Policy Implications

1. During periods of global supply chain disruption, policymakers should pay special attention to trade costs for consumable goods.

2. Trade policy decisions should consider the differential impact on inflation stability based on which category of goods is affected.

3. Even modest policy interventions targeting food and essential goods supply chains could have outsized stabilizing effects on inflation.

4. The observed lag between trade shocks and inflation response provides policymakers with an early warning window for proactive intervention.

## Model Performance

The OLS regression model for inflation sensitivity achieves an R-squared of 0.75, indicating good predictive capability that can be valuable for central banks and policy planners.

## Usage

To run this analysis:

1. Ensure you have Python 3.6+ installed with the following packages:
   - pandas
   - numpy
   - matplotlib
   - seaborn
   - statsmodels
   - scikit-learn
   - pymc
   - arviz

2. Prepare the following datasets:
   - `cleaned_data2_consumable.csv`: Trade data for consumable goods
   - `cleaned_data_nonconsumable.csv`: Trade data for non-consumable goods
   - `cleaned_data2total.csv`: Total trade data
   - `consolidated_inflation_data.csv`: Inflation data

3. Run the analysis script to reproduce the findings.

## Future Research Directions

1. Incorporate more granular product categories to identify specific goods with outsized inflation impacts.

2. Investigate further the time lag between trade shocks and inflation responses to provide more precise insights for policy timing.

3. Explore the interaction between monetary policy interventions and trade shocks to reveal optimal policy coordination mechanisms.

4. Develop country-specific early warning indicators based on the regional patterns identified.

5. Extend the analysis to include currency effects and exchange rate pass-through mechanisms for a more comprehensive inflation prediction system.

## Contact

For questions about this research, please contact [Your Contact Information].

## License

[Specify the license under which this project is released]
