# Bank Data Analysis

This repository contains an analysis of bank data, focusing on various aspects such as age, expected recovery amount, actual recovery amount, sex, and recovery strategy. This is a Datacamp project.

## Tasks

1. **Load the Data**:
   - Import pandas under the alias pd and numpy under the alias np.
   - Read in "datasets/bank_data.csv" using read_csv() and save it as df.

2. **Scatter Plot of Age vs. Expected Recovery Amount**:
   - From matplotlib, import the pyplot module under the alias plt.
   - Plot expected_recovery_amount on the x-axis and age on the y-axis.
   - Set the label on the x-axis to "Expected Recovery Amount" and the label on the y-axis to "Age".
   - Finish the plt statement with plt.show().

3. **Average Age Difference Test**:
   - Filter for expected recovery amounts greater than or equal to $900 and less than $1100, saving it as era_900_1100.
   - Filter era_900_1100 for "Level 0 Recovery" and select the age column, saving it as Level_0_Age.
   - Filter era_900_1100 for "Level 1 Recovery" and select the age column, saving it as Level_1_Age.
   - Compute the Kruskal-Wallis test to see if the average ages are statistically significantly different using stats.kruskal(Level_0_age,Level_1_age).

4. **Chi-Square Test for Sex vs. Recovery Strategy**:
   - Filter df for expected recovery amounts greater than or equal to $900 and less than $1100.
   - Compute the crosstab of sex and recovery_strategy.
   - Print the crosstab.
   - Run the chi-square test by inputting the crosstab variable into stats.chi2_contingency().
   - Print the p-value using p_val.

5. **Scatter Plot of Actual vs. Expected Recovery Amount**:
   - Set x to expected_recovery_amount and y to actual_recovery_amount.
   - Set the label on the x-axis to "Expected Recovery Amount" and the label on the y-axis to "Actual Recovery Amount".
   - Finish the plt statement with plt.show().

6. **Actual Recovery Amount Difference Test**:
   - Create variables Level_0_actual and Level_1_actual for the actual recovery amounts of customers with expected recovery amounts between $900 and $1100 belonging to Level 0 and Level 1, respectively.
   - Compute the Kruskal-Wallis test to see if they are statistically significantly different using stats.kruskal().
   - Redefine Level_0_actual and Level_1_actual for the range of $950 to $1050, then perform the Kruskal-Wallis test again.

7. **Regression Model for Actual vs. Expected Recovery Amount**:
   - Select the expected_recovery_amount column of era_900_1100 and assign it to x.
   - Select the actual_recovery_amount column of era_900_1100 and assign it to y.
   - Print out the model summary using model.summary().

8. **Regression Model with Recovery Strategy Indicator**:
   - Create the indicator_1000 column by filtering df for expected recovery amounts less than 1000.
   - Select the expected_recovery_amount and indicator_1000 columns from era_900_1100 and assign it to X.
   - Select the actual_recovery_amount column from era_900_1100 and assign it to y.
   - Print out the model summary using model.summary().

9. **Regression Model for $950 to $1050 Range**:
   - Redefine era_950_1050 to include the indicator variable created in task 8.
   - Define x as the expected_recovery_amount and the indicator_1000 when the expected recovery amount was >= $950 and < $1050.
   - Define y as the actual_recovery_amount when the expected recovery amount was >= $950 and < $1050.

## Data and Tools

The analysis is performed on a dataset of bank data, which is assumed to be in the "datasets/bank_data.csv" file. The queries and analysis are written in Python using the pandas and numpy libraries for data manipulation and the matplotlib library for data visualization.

## Conclusion

This repository provides a comprehensive analysis of bank data, focusing on the relationship between age, expected recovery amount, actual recovery amount, sex, and recovery strategy. The analysis includes scatter plots, statistical tests, and regression models to uncover insights and patterns in the data. The results of this analysis can be used by banks to improve their recovery strategies and make more informed decisions about their customers.
