# R Portfolio: NHANES Data Analysis

## Project Overview

The project involves reading and merging multiple NHANES datasets, performing statistical analysis, and visualizing the results. Key tasks include:
- Data cleaning and preprocessing.
- Visualization of relationships between variables (e.g., body measurements and demographic data).
- Statistical modeling to explore health outcomes.

## Introduction

This project investigates the relationship between several health factors and demographic characteristics, using the National Health and Nutrition Examination Survey (NHANES) 2017-2018 data. The following research questions are addressed:

1. Is there a relationship between BMI and hs-CRP (a marker of inflammation)?
2. Is there a significant difference in sleeping duration between male and female participants?
3. Are HDL cholesterol levels different among racial/ethnic groups?
4. Is education level associated with BMI?

## Data

- Data source: NHANES 2017-2018
- Variables include: BMI, hs-CRP, HDL cholesterol, sleep duration, race/ethnicity, education level, and more.
- Total observations: 3,214 (filtered from 5,828 participants after cleaning and removing outliers).

## Libraries Used

- `readxl`: For importing data files.
- `tidyverse`: For data manipulation and visualization.
- `ggplot2`: For creating visualizations.
- `rstatix`: For statistical tests and analysis.
- `psych`: For descriptive statistics.
- `flextable`: For creating flexible tables.
- And more.

## Methods

### 1. Correlation Between BMI and hs-CRP
- Variables: BMI (continuous) and hs-CRP (continuous).
- Test used: Spearman’s Rank-Order correlation (due to non-normality).
- Visualization: Scatterplot.

### 2. Sleep Duration by Gender
- Variables: Sleep duration (continuous) and gender (categorical).
- Test used: Wilcoxon Rank-Sum test (non-parametric).
- Visualization: Boxplots and histograms.

### 3. HDL Cholesterol Levels by Race/Ethnicity
- Variables: HDL cholesterol (continuous) and race/ethnicity (categorical).
- Test used: Kruskal-Wallis test and pairwise comparisons with Bonferroni correction.
- Visualization: Boxplots and pairwise comparison visualizations.

### 4. Education Level and BMI Association
- Variables: BMI (categorical) and education level (categorical).
- Test used: Pearson’s Chi-squared test.
- Visualization: Contingency tables, bar charts, and balloon plots.

## Key Results

1. **Correlation Between BMI and hs-CRP**:
   - A significant positive correlation between BMI and hs-CRP (Spearman's ρ = 0.51, p < 0.001).

2. **Sleep Duration by Gender**:
   - Female participants had significantly longer sleep duration than males (p < 0.001).

3. **HDL Cholesterol by Race/Ethnicity**:
   - Significant differences in HDL cholesterol levels among racial/ethnic groups (p < 0.001).
   - Non-Hispanic Black participants had the highest HDL cholesterol levels.

4. **Association Between Education Level and BMI**:
   - Significant association between education level and BMI (p < 0.001). Participants with higher education were more likely to have a healthy weight.

## Visualizations

![image](https://github.com/user-attachments/assets/0e58f175-5237-44e0-a1d5-4a94603eefd1)

*Figure 1. Scatterplot showing the relationship between BMI and hs-CRP.*

![image](https://github.com/user-attachments/assets/4565e0ed-b375-4bf1-8999-26da66a86b27)

*Figure 2. Boxplots of sleep duration by gender.*

![image](https://github.com/user-attachments/assets/57b4f946-76de-49a3-a72f-f137104116f7)

*Figure 3. Visualisation of the significant result of Pairwise comparisons
**: p =< 0.01, ***: p =< 0.001, ****: p =< 0.0001*

![image](https://github.com/user-attachments/assets/924b439a-a0b2-4ce7-a91f-97b6770dad28)

*Figure 4. The clustered bar chart shows the frequency of BMI of the NHANES 2017−2018
participants according to their education level.*

![image](https://github.com/user-attachments/assets/a04cbd7c-d22a-4aa9-bdd5-312067c0048b)

*Figure 5. Balloon plot for the visualisation of the contigency table.*


## How to Run the Analysis

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/nhanes-analysis.git

