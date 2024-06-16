# 🔍Predicting Prosperity: Household Income Models🧠

#### Introduction
The "Regression Dataset for Household Income Analysis" is a synthetic dataset designed to simulate various demographic and socioeconomic factors that influence annual household income. The dataset comprises 10,000 records with 14 features, including age, education level, occupation, number of dependents, location, work experience, marital status, employment status, household size, homeownership status, type of housing, gender, primary mode of transportation, and annual household income. This report outlines the steps taken to clean, explore, and model the data to understand and predict household income.

#### Data Cleaning
The initial step involved ensuring the dataset was free of missing values and duplicates. All categorical variables were converted to appropriate data types for easier handling during analysis. The dataset appeared to be clean, with no missing values or duplicates.

#### Exploratory Data Analysis (EDA)
EDA was conducted to visualize and understand the distributions and relationships among the features. Key observations from the visualizations include:

- **Income Distribution**: The distribution of annual household income was plotted, revealing a right-skewed distribution, suggesting that most households have a moderate income, with fewer households earning very high incomes.
- **Income by Education Level**: A boxplot showed that higher education levels generally corresponded to higher median incomes, with doctorate holders earning the most, followed by those with master's, bachelor's, and high school education.
- **Income by Occupation**: Different occupations had varying income distributions, with technology and finance sectors generally earning more compared to healthcare, education, and other sectors.
- **Employment Status**: A bar plot illustrated the count of individuals across different employment statuses, with full-time employment being the most common.
- **Relationships Between Variables**: Pairplots and correlation matrices were used to explore relationships between variables such as age, work experience, and income, revealing positive correlations between work experience and income.

#### Feature Engineering
To prepare the data for modeling, categorical variables were transformed into numerical format using one-hot encoding. Numerical features were standardized to ensure all features had a similar scale, which is crucial for certain regression models.

#### Modeling
Several regression models were developed to predict annual household income:

1. **Linear Regression**: This basic model provided a benchmark for performance comparison.
2. **Ridge Regression**: A regularized version of linear regression that helps prevent overfitting by penalizing large coefficients.
3. **Lasso Regression**: Another regularization technique that can also perform feature selection by shrinking some coefficients to zero.
4. **Random Forest Regressor**: An ensemble model that leverages multiple decision trees to improve predictive performance and handle non-linear relationships.

The models were evaluated using metrics such as R-squared (R²) and Root Mean Squared Error (RMSE):

- **Linear Regression**: Achieved an R² indicating the proportion of variance in the income that was predictable from the features, and an RMSE reflecting the average error of the model's predictions.
- **Ridge Regression**: Showed slight improvements over the linear model due to regularization.
- **Lasso Regression**: Similar to Ridge but also indicated which features were less important by shrinking their coefficients to zero.
- **Random Forest Regressor**: Provided the best performance among the models, effectively capturing complex relationships in the data.

#### Conclusion
The analysis revealed significant insights into how different demographic and socioeconomic factors influence household income. Higher education levels and certain occupations were strong predictors of higher income, while work experience also showed a positive correlation. The Random Forest Regressor outperformed other models, suggesting that non-linear relationships and interactions between features play a crucial role in predicting household income.

Future work could involve further tuning of models, exploring additional features, or applying more advanced techniques such as gradient boosting machines or neural networks. This analysis framework provides a solid foundation for understanding and modeling household income based on demographic and socioeconomic factors.

Dataset Link: https://www.kaggle.com/datasets/stealthtechnologies/regression-dataset-for-household-income-analysis/data
