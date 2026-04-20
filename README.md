## Hong Kong Local Food Production & Climate Analysis (2007-2024)
# Project Overview
This study examines relationships between atmospheric pressure, relative humidity, rainfall, and annual yields of vegetables, livestock, seafood, and poultry in Hong Kong. The goal is to identify which food sectors are most sensitive to weather patterns and provide data-driven insights for local food security planning.

# Data Sources
Food Production: Hong Kong government statistics (Table 990-92071_en.xlsx) - annual production by category

Climate Data: Hong Kong Observatory daily records (2007-2024) for pressure (hPa), humidity (%), and rainfall (mm)

# Key Findings
Climate correlation is weak or negligible across all three variables

2007 is a statistical outlier - production nearly double typical years under normal climate conditions

Non-climate drivers dominate - policy changes, urbanization, economic shifts explain post-2007 decline

Production is concentrated - pigs + salt-water fish = 81% of total output

Recent acceleration - 10.5% drop from 2023 to 2024, lowest production in study period

# Technical Implementation
ETL: Power Query (unpivoting food data, cleaning climate CSVs, imputing missing values)

Data Model: Star schema (Fact: FoodProduction; Dims: YearDim, FoodCategory)

DAX Measures: Total Production, YoY Growth %, Production Volatility, High Humidity Year Flag

# Visualizations: Dual-axis line charts, scatter plot matrix, heatmap, ribbon chart

# Limitations
Granularity mismatch (annual production vs. daily climate)

Imputed rainfall errors using mean values

Limited diversity (vegetables/field crops near-zero baseline)

No control for confounding variables (COVID-19, policy changes, land use)

Single weather station may not capture microclimates

# Recommendations for Hong Kong Food Security
Investigate the post-2007 structural break in production

Diversify beyond the pig/fish duopoly

Address accelerating 2022-2024 decline

Maintain climate monitoring but prioritize economic/policy factors
