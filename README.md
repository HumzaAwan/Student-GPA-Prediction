Student GPA Prediction
This repository contains a Jupyter Notebook (Student GPA.ipynb) that explores the relationship between student fitness data and their GPA using various regression models. The project analyzes a dataset of 145 students, incorporating features such as daily steps, exercise mode, minutes of activity, graduation status, and pulse rate to predict GPA.

Project Overview
The notebook implements and evaluates multiple regression techniques to model GPA based on fitness and academic features:

Ordinary Least Squares (OLS) Regression: Establishes a baseline linear model with an R-squared of 0.308, indicating moderate explanatory power.
Polynomial Regression: Tests non-linear relationships but yields a low R-squared of 0.0249, suggesting limited improvement.
Lasso Regression: Applies regularization for variable selection, achieving an R-squared of 0.3045, comparable to OLS.
Decision Tree: Explores non-linear patterns but shows signs of overfitting with high RMSE values (0.9971 on training, 1.0077 on test).
The analysis includes data preprocessing (standardization, duplicate removal, and handling missing values), model training, and performance evaluation using metrics like MAE, MSE, RMSE, and R-squared. Visualizations compare model performance across these metrics.

Dataset
Source: Studentfitdata.sav (SPSS file)
Features:
Steps: Daily steps taken
Mode: Exercise mode (binary, e.g., 0 or 1)
Minutes: Minutes of activity
Graduated: Graduation status (binary, 0 or 1)
Pulse: Resting pulse rate
Target: GPA (continuous, ranging from 0 to 4)
Size: 145 rows, 6 columns (after preprocessing)
Key Findings
The OLS model indicates that Graduated and Minutes are statistically significant predictors, though the overall R-squared (0.308) suggests other unmodeled factors influence GPA.
Polynomial and Decision Tree models do not significantly outperform OLS, with the latter showing overfitting.
Lasso regression provides variable selection but does not improve predictive power substantially.
Non-normality in the data (per Omnibus and Jarque-Bera tests) may affect model assumptions, suggesting potential for further data transformations.
Requirements
To run the notebook, install the following Python libraries:

bash

Copy
pip install numpy pandas seaborn statsmodels matplotlib scikit-learn
Additionally, ensure you have a library to read SPSS files (e.g., pyreadstat):

bash

Copy
pip install pyreadstat
How to Use
Clone the repository:
bash

Copy
git clone https://github.com/your-username/Student-GPA-Prediction.git
Navigate to the project directory:
bash

Copy
cd Student-GPA-Prediction
Place the Studentfitdata.sav file in the appropriate directory (update the file path in the notebook if needed).
Open and run the Jupyter Notebook:
bash

Copy
jupyter notebook Student\ GPA.ipynb
Future Improvements
Incorporate additional features (e.g., study hours, sleep quality) to improve model performance.
Experiment with advanced models like Random Forests or Gradient Boosting.
Apply data transformations to address non-normality.
Conduct cross-validation to ensure robust model evaluation.
