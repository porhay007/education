# School Performance and Socioeconomic Factors Analysis

## Project Overview

This project investigates the relationship between school performance, measured by average ACT scores, and socioeconomic factors such as community education levels, household income, local unemployment rates, family structure, and student poverty. Using datasets from EdGap and the Common Core of Data (CCD), we perform data cleaning, exploratory data analysis (EDA), and linear regression modeling to identify the factors that most strongly predict school performance. Techniques include data merging, visualization, and statistical modeling using Python.

Objective: Examine how socioeconomic characteristics affect ACT scores across U.S. schools.

Domain: Education / Socioeconomic Data Science

Key Techniques: Data Cleaning, Data Merging, Exploratory Data Analysis (EDA), Linear Regression, Data Visualization

## Project Structure

```
├── data/ # Raw and cleaned data files
│ ├── EdGap_data.xlsx
│ ├── school_information_sch_029_1617_w_1a_11212017.csv
│ └── cleaned_education_data.csv # Cleaned dataset
├── code/ # Jupyter notebooks
│ └── school_performance_analysis.ipynb
├── reports/
│ └── Education_Project_Report.pdf # Final report
├── requirements.txt # Project dependencies
└── README.md # Project documentation
```

- data/: Contains raw and cleaned datasets used for analysis.

- code/: Jupyter notebook performing data cleaning, EDA, and modeling.

- reports/: Final PDF report summarizing findings.

- requirements.txt: Python packages required to run the analysis.

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

3. Exploratory Data Analysis (EDA)

- Visualized ACT scores versus socioeconomic factors using scatterplots and regression plots.

- Created state-level map of average ACT scores.

4. Regression Analysis

- Performed OLS regression using both raw and standardized predictors.

- Identified key predictors:

  - Positive: Percent of adults with college degrees.

  - Negative: Student poverty (percent on free/reduced lunch) and local unemployment rate.

- Found that student poverty has the strongest overall impact on ACT scores.

## Files

- Notebook performing analysis: school_performance_analysis.ipynb

- Cleaned dataset: cleaned_education_data.csv

- Final report : Education_Project_Report.pdf

## Results

- Socioeconomic factors influence school performance, explaining about 62% of the variation in ACT scores.

- Higher community education levels positively predict ACT scores.

- Student poverty and local unemployment negatively predict ACT scores.

- Median household income and percent of children in married-couple families were not significant after controlling for other variables.

## Authors

Porhay Rouen — [porhay007](https://github.com/porhay007)

## License

This project is licensed under the MIT License — see the LICENSE file for details.

## Requirements

The project uses the following tools and libraries:

- Python 3.10+
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- statsmodels
- scikit-learn

## Acknowledgements

- Data Sources: EdGap Project and the Common Core of Data (CCD)

- Tools: Python, Jupyter Notebook

- Guidance: Seattle University’s DATA 5100 course
