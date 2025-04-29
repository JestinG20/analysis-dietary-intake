# Impact of Dietary Intake on Blood Pressure

## Overview

This project investigates how various dietary nutrients impact blood pressure levels (both systolic and diastolic) using the NHANES dataset. The nutrients analyzed include sodium, calcium, magnesium, sugar, total fat, saturated fat, and cholesterol. This study aims to provide insights into dietary strategies for managing hypertension.

## Author

**Jestin George**  
Date: April 29, 2025

---

## Objectives

### Primary Aim
- Analyze the relationship between nutrient intake (sodium, calcium, magnesium, total fat, saturated fat, cholesterol, alcohol, and sugar) and blood pressure levels using NHANES data.

### Secondary Aims
- Assess how age and BMI influence this relationship.
- Investigate if nutrients like calcium and magnesium have protective effects across population groups.

---

## Dataset

- **Source**: NHANES dataset from the [CDC Website](https://www.cdc.gov/nchs/nhanes/)
- **Components Used**: Demographics, Dietary Intake (Day 1 & 2), Examination Data (Blood Pressure), Body Measurements.

---

## Libraries Used

- `dplyr`, `tidyr`, `ggplot2`, `car`, `haven`, `nhanesA`, `ppcor`, `corrplot`

---

## Data Preparation

- Loaded and merged multiple datasets using the `SEQN` identifier.
- Filtered out individuals under 18 years.
- Removed records with missing values.
- Computed averages for multiple blood pressure and dietary readings.
- Derived BMI and categorized variables (BP categories, age groups).

---

## Key Variables

- **Independent**: Sodium, Calcium, Magnesium, Sugar, Total Fat, Saturated Fat, Cholesterol
- **Dependent**: Systolic Blood Pressure, Diastolic Blood Pressure
- **Covariates**: Age, Gender, BMI

---

## Analysis Performed

### 1. Descriptive Statistics
- Frequency tables and summaries for categorical and continuous variables.
- Category-wise summaries for blood pressure categories.

### 2. Exploratory Data Analysis
- Box plots for blood pressure distribution.
- Histograms for nutrient distribution.
- Scatter plots showing relationships between dietary and demographic factors with BP.

### 3. Correlation Analysis
- Correlation matrix and correlation plots.
- Pearson correlation tests to examine nutrient-BP associations.

### 4. Regression Modeling
- **Basic Linear Regression**: Assessed individual predictors of systolic and diastolic BP.
- **Advanced Linear Regression**: Included interaction terms (e.g., nutrient * age * BMI).
- Multicollinearity checked using VIF.

---

## Key Findings

- **Negative correlation**: Calcium and magnesium with blood pressure.
- **Positive correlation**: Cholesterol and sugar with systolic BP.
- **Regression insights**:
  - Age and BMI are significant predictors of blood pressure.
  - Sugar, total fat, saturated fat, and cholesterol significantly influence systolic BP.
  - BMI is strongly associated with diastolic BP.

---

## Visualizations

- Distribution plots for nutrients.
- Boxplots and scatter plots showing demographic and nutrient effects on BP.
- Residual plots for regression diagnostics.

---

## How to Run

1. Clone this repository.
2. Ensure R and the required libraries are installed.
3. Run the R script or R Markdown file used for analysis (not included in this README).
4. Download NHANES `.xpt` files and place them in the working directory as referenced in the code.

---

## Future Work

- Incorporate additional NHANES cycles to strengthen findings.
- Explore non-linear models or machine learning approaches for better prediction.
- Analyze subgroup effects (e.g., by ethnicity or gender).

---

## License

This project is open-source and available under the [MIT License](LICENSE).

