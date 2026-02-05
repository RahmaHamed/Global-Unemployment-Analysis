# Global Unemployment Trends & Data Pipeline (2014-2024)

## 📌 Project Overview
This repository contains a comprehensive Exploratory Data Analysis (EDA) and Preprocessing pipeline for a global unemployment dataset. The research focuses on identifying structural shifts in labor markets across various countries, genders, and age groups over a ten-year period.

## 🛠️ Data Science Pipeline

### 1. Exploratory Data Analysis (EDA)
* **Trend Identification:** Analyzed global unemployment spikes, specifically correlating the 2020–2022 outliers with the socioeconomic impact of the COVID-19 pandemic.
* **Bivariate Analysis:** Conducted gender-based comparisons, discovering that female unemployment rates exhibited higher volatility during the 2024 recovery phase.
* **Distribution Assessment:** Identified significant right-skewness in numerical features, justifying the need for advanced scaling in the preprocessing stage.
* **Correlation Analysis:** Financial variables like income and expenses show moderate correlation ($r=0.55$), while demographic features like age show weaker ties to immediate financial status.


### 2. Preprocessing & Data Engineering
* **Strategic Data Reduction:** Faced with missing values in the most recent 4-year cycle, I implemented a custom sampling and reduction strategy to maintain a balanced longitudinal study while optimizing for processing speed.
* **Feature Scaling:** Applied **Min-Max Scaling** to normalize unemployment rates (ranging from 0.03% to 70%). This ensured that no single extreme outlier dominated the variance during future modeling.
* **Interpretability Trade-off:** Documented the transition from raw percentages to scaled values (0-1), acknowledging the mathematical necessity for model stability vs. the challenge of real-world interpretability.

## 3.Unsupervised Learning
**(K-Means)Optimal K-Selection:** Used Elbow and Silhouette methods to determine that $k=3$ was the most appropriate number of clusters.
**Post-Hoc Analysis:** Employment status was analyzed after clustering to evaluate its distribution across the identified group


## Cluster,Financial Status,Employment Composition,Key Takeaway
**Cluster 0**,Moderate Income,"75% Employed, 25% Student ",Stable and predictable financial patterns.
**Cluster 1**,Low Income / High Savings,"80% Self-employed, 5% Unemployed ",Irregular patterns; high savings likely due to synthetic data generation.
**Cluster 2**,High Prosperity,"69% Employed, 31% Student ",Highest financial stability and savings-to-income ratios.


##  Key Findings & Limitations
* **Recovery Trends:** Data suggests a "return to normal" post-2022, though structural imbalances remain in specific demographic cohorts.
* **Future Scope:** The analysis highlights that while statistical modeling (EDA) identifies patterns, future iterations require the inclusion of features like Education Level and GDP Growth to establish causal relationships.
* **Synthetic Data:** Because the analysis is based on synthetic data, results are exploratory and motivate validation on real-world datasets.
* **Temporal Dynamics:** The cross-sectional nature of the study prevents assessment of income volatility or transitions between employment types over time.
* **Policy Impact:** Findings suggest that demographic labels alone are insufficient to predict financial stability, requiring targeted interventions
##  Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
