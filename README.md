## Introduction

School Performance and Socioeconomic Factors Analysis

## Project Overview

This project investigates the relationship between school performance, measured by average ACT scores, and socioeconomic factors. Using datasets from EdGap and the Common Core of Data (CCD), we perform exploratory data analysis, data cleaning, and regression modeling to determine which factors are most predictive of school performance.

    - Objective: Examine how community education, household income, unemployment rate, family structure, and student poverty relate to ACT scores.

    - Domain: Education / Socioeconomic Data Science

    - Key Techniques: Data Cleaning, Data Merging, Exploratory Data Analysis (EDA), Linear Regression, Data Visualization

## Project Structure

├── data/ # Raw and cleaned data files
│ ├── EdGap_data.xlsx
│ ├── school_informatiom_sch_029_1617_w_1a_11212017.csv
│ └── cleaned_education_data.csv # Cleaned dataset
├── code/ # Jupyter notebooks
│ └── school_performance_analysis.ipynb
├── reports/  
│ └── Education_Project_Report.pdf
├── requirements.txt # Project dependencies
└── README.md # Project documentation

## DATA

    - EdGap Data: EdGap_data.xlsx

    - School Information (CCD): school_informatiom_sch_029_1617_w_1a_11212017.csv

## Analysis

1. Load and Clean Data

   - Imported EdGap and CCD datasets.

   - Removed duplicates and out-of-range values.

   - Handled missing values for key variables such as ACT scores, income, unemployment, and percent of students on free/reduced lunch.

2. Merge and Prepare Data

   - Merged datasets using school IDs (NCESSCH).

   - Selected and renamed relevant columns.

   - Created derived variables:

     - income_k – median household income in thousands.

     - act_vs_median – difference from median ACT score.

3. Exploratory Analysis

   - Visualized ACT scores versus socioeconomic factors using scatterplots and regression plots.

   - Created state-level map of average ACT scores.

4. Regression Analysis

   - Performed linear regression (OLS) using raw and standardized predictors.

   - Identified significant predictors:

     - Positive: Percent of adults with college degrees.

     - Negative: Student poverty (percent on free/reduced lunch) and local unemployment.

   - Student poverty has the strongest relative impact among significant predictors.

## Files

    - Notebook performing analysis: school_performance_analysis.ipynb

    - Cleaned dataset: cleaned_education_data.csv

## Results

    - Socioeconomic factors influence school performance, explaining about 62% of the variation in ACT scores.

    - Higher community education levels positively predict ACT scores.

    - Student poverty and local unemployment negatively predict ACT scores.

    - Median household income and percent of children in married-couple families were not significant after controlling for other variables.

## Authors

Porhay Rouen — porhay007

## License

This project is licensed under the MIT License — see the LICENSE file for details.

## Acknowledgements

    - EdGap and Common Core of Data (CCD) for datasets

    - Python libraries: pandas, numpy, matplotlib, seaborn, plotly, statsmodels, scikit-learn

    - Seattle University DATA 5100 course for project guidance
