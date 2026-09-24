# UCI_Real_State_mini_project
UCI Real Estate dataset analysis exploring correlations between property features and house prices using Python, Pandas, Matplotlib, and Seaborn.
UCI Real Estate House Price Analysis

A mini data science project using the UCI Real Estate Valuation dataset to analyze the relationship between property features and house prices and build a Multiple Linear Regression model for house price prediction.

📌 Project Overview

This project explores how different real-estate-related features are correlated with the house price of unit area.

The analysis includes:

Exploratory Data Analysis (EDA)
Data cleaning
Correlation analysis
Correlation heatmap
Feature vs. house price visualizations
Train/Test Split
Multiple Linear Regression using Scikit-learn
Model predictions
Regression evaluation metrics
Actual vs. predicted visualization
Residual analysis
📊 Dataset

UCI Real Estate Valuation Dataset

The dataset contains information about real estate transactions and their relationship with house prices.

Features
Feature	Description
X1 transaction date	Transaction date
X2 house age	Age of the house
X3 distance to the nearest MRT station	Distance to the nearest MRT station
X4 number of convenience stores	Number of nearby convenience stores
X5 latitude	Geographic latitude
X6 longitude	Geographic longitude
Y house price of unit area	Target variable — house price per unit area

The No column was removed because it is an identifier and does not provide useful predictive information.

🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook / Google Colab
🔍 Exploratory Data Analysis

The dataset was inspected using:

df.info()
df.describe()
df.isnull().sum()

The analysis confirmed the structure of the dataset, descriptive statistics, and missing-value information.

🔗 Correlation Analysis

A Pearson correlation matrix was used to examine the linear relationship between the features and house price.

Key observations
Feature	Correlation with House Price
Transaction Date	0.09
House Age	-0.21
Distance to MRT	-0.67
Convenience Stores	0.57
Latitude	0.55
Longitude	0.52

The distance to the nearest MRT station has the strongest correlation in absolute value with house price (-0.67).

The number of convenience stores has the strongest positive correlation (0.57).

Correlation indicates a linear association between variables and does not establish causation.

🤖 Machine Learning Model

A Multiple Linear Regression model from Scikit-learn was used.

Workflow
Dataset
   ↓
Data Cleaning
   ↓
Correlation Analysis
   ↓
Define X and y
   ↓
Train/Test Split
   ↓
Multiple Linear Regression
   ↓
Predictions
   ↓
Model Evaluation

The dataset was divided using:

train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)

The model was then trained using:

model = LinearRegression()

model.fit(X_train, y_train)
📈 Model Evaluation

The model was evaluated using:

R²
MAE
MSE
RMSE
R²

The model achieved an R² of approximately 0.68 on the test dataset.

This means the model explains approximately 68% of the variation in house price in the test data.

R² should not be interpreted as model "accuracy."

Evaluation Metrics
MAE = mean_absolute_error(y_test, y_pred)

MSE = mean_squared_error(y_test, y_pred)

RMSE = np.sqrt(MSE)
📊 Visualizations

The project includes the following visualizations:

Correlation Heatmap

Shows the linear correlations between all variables.

Feature vs. House Price

Scatter plots were created for:

Transaction Date vs. House Price
House Age vs. House Price
Distance to MRT vs. House Price
Convenience Stores vs. House Price
Latitude vs. House Price
Longitude vs. House Price
Actual vs. Predicted House Prices

The model's predicted values are compared against the actual house prices.

Residual Plot

Residuals are plotted against predicted values to examine the model's prediction errors.

📁 Project Structure
UCI-Real-Estate-House-Price-Analysis/
│
├── Real estate valuation data set.xlsx
├── UCI_Real_Estate_House_Price_Analysis.ipynb
└── README.md
🎯 Key Takeaways
Distance to the nearest MRT station showed the strongest absolute correlation with house price.
Number of convenience stores showed the strongest positive correlation among the listed features.
Multiple Linear Regression was used to model house price using all available predictors.
The model achieved an R² of approximately 0.68 on the test dataset.
Correlation analysis and regression coefficients provide different information and should not be interpreted interchangeably.
Residual analysis was used to examine prediction errors.
🚀 Future Improvements

Possible improvements to this project include:

Feature scaling and comparison of model performance
Polynomial Regression
Ridge and Lasso Regression
Cross-validation
Feature selection
Comparison with other regression algorithms
Hyperparameter tuning
More detailed residual diagnostics
