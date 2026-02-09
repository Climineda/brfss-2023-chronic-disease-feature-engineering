# BRFSS 2023 Chronic Disease Prediction — Feature Engineering & Analysis
This repository contains my workflow for preparing, engineering, and analyzing features from the Behavioral Risk Factor Surveillance System (BRFSS) 2023 dataset to support chronic disease prediction.
The project emphasizes interpretability, public‑health relevance, and transparent documentation of analytical decisions.

## Project Overview
Chronic diseases arise from a combination of behavioral, clinical, psychosocial, and demographic factors.
This project uses BRFSS 2023 — the largest continuously collected health survey in the world — to:

* engineer meaningful predictors

* visualize key health and behavioral patterns

* document the reasoning behind each transformation

* prepare the dataset for downstream modeling

The workflow is structured to mirror a professional data‑science pipeline.

## Workflow Summary
**1.** Exploratory Data Analysis (EDA)
Completed in 01_eda.ipynb.

Includes:

* data cleaning

* missing‑value handling

* variable inspection

* correlation analysis across all numerical variables

* initial visualizations

* export of cleaned dataset

The cleaned dataset is saved as:
*/data/brfss_2023_cleaned.csv*

**2.** Feature Engineering
Performed in 02_feature_engineering.ipynb.

Includes:

* engineering clinically meaningful features

* creating domain‑informed transformations

* generating clear, interpretable visualizations

* documenting the why and how behind each engineered feature

This notebook focuses on transforming raw BRFSS variables into predictors suitable for modeling.

**3.** Modeling (upcoming)
Will use engineered features to predict chronic disease presence and evaluate model performance.

## Engineered Features (Summary)
Each feature was selected based on public‑health relevance, interpretability, and BRFSS codebook definitions.

* **BMI (Continuous & Categorical)**
Captures obesity‑related risk using both continuous BMI and CDC weight classes.

* **Physical Activity (ACTIVE)**
Binary indicator of exercise in the past 30 days.

* **Smoking History (SMOKER)**
Binary exposure variable for lifetime smoking (≥100 cigarettes).

* **Heavy Alcohol Use (HEAVY_DRINKER)**
Binary indicator of heavy drinking based on BRFSS thresholds.

* **Stress Score (STRESS_LEVEL)**
Ordinal measure of psychological strain; compared across chronic disease status.

* **General Health (GENHLTH_SCORE)**
Reverse‑coded ordinal measure of self‑rated health.

* **Poor Physical & Mental Health Days**
Numeric counts (0–30) capturing functional limitations.

* **Demographics (Age, Sex, Education, Income)**
Key social determinants of health included for context and modeling.

## Why This Project Matters
Chronic disease prediction requires understanding the social, behavioral, and psychological determinants that shape health outcomes.
This project emphasizes:

* transparent feature engineering

* interpretable transformations

* domain‑informed reasoning

* reproducible analysis

The goal is to build a dataset that is both statistically sound and public‑health meaningful.

## Data Source
Centers for Disease Control and Prevention (CDC)
Behavioral Risk Factor Surveillance System (BRFSS), 2023  
https://www.cdc.gov/brfss

## Next Steps
Build predictive models using engineered features

Evaluate model performance

Interpret feature importance

Connect findings to public‑health implications
