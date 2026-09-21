# Data

This project combines three public datasets to examine extreme heat exposure, heat volatility, long-term heat change, and social vulnerability across the continental United States.

## Data Sources

### 1. Extreme Heat Days

**Source:** Centers for Disease Control and Prevention (CDC), National Environmental Public Health Tracking Network

**Coverage:** 1979–2022

**Geographic Level:** County

The dataset provides annual county-level counts of extreme heat days and serves as the primary dataset for the analysis.

[CDC National Environmental Public Health Tracking Network](https://www.cdc.gov/nceh/tracking/)

### 2. Social Vulnerability Index (SVI)

**Source:** CDC / Agency for Toxic Substances and Disease Registry (ATSDR)

**Year:** 2022

**Geographic Level:** County

The Social Vulnerability Index is a composite measure of socioeconomic and demographic vulnerability. It was used to compare patterns in extreme heat exposure, heat volatility, and long-term heat change across different levels of social vulnerability.

[CDC/ATSDR Social Vulnerability Index](https://www.atsdr.cdc.gov/placeandhealth/svi/)

### 3. U.S. Census Regions

**Source:** U.S. Census Bureau

Census region classifications were used to compare heat patterns across four U.S. regions:

- Midwest
- Northeast
- South
- West

[U.S. Census Bureau](https://www.census.gov/)

## Data Integration

The datasets were combined in Tableau to support county-level, state-level, regional, and social-vulnerability analyses.

- `ExtremeHeatDays.csv` was connected to `us_regions_census.csv` using the shared `StateFIPS` field. This allowed county-level heat observations to be assigned to U.S. Census regions.
- `ExtremeHeatDays.csv` was connected to the Social Vulnerability Index dataset using the shared `CountyFIPS` field, allowing county-level heat metrics to be compared with county-level social vulnerability.

Using county-level identifiers preserved geographic detail for the heat and SVI analysis, while StateFIPS was used only for assigning records to broader Census regions.
  
## Data Availability

The raw datasets are not stored in this repository. They are publicly available from the source organizations linked above.

This repository focuses on the analytical methodology, Tableau visualizations, and findings developed from these public datasets.
