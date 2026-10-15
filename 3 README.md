# Car Price Prediction with Machine Learning

## Project Overview
Car Price Prediction is a Machine Learning project that predicts the selling price of used cars based on their features, such as manufacturing year, brand, fuel type, transmission, kilometres driven, and ownership history.

This project is completed as part of the OASIS INFOBYTE Data Science Internship. It demonstrates how regression algorithms can be used to estimate used-car prices from historical data.

## Objectives
- Load and understand the used-car dataset.
- Clean missing values, duplicate records, and inconsistent data.
- Perform Exploratory Data Analysis (EDA).
- Create useful features such as car age and brand.
- Train and compare different regression models.
- Evaluate model performance using MAE, RMSE, and R² score.
- Analyze feature importance and prediction errors.
- Select the best-performing model based on evaluation results.

## Dataset Description
This project uses the **CarDekho used-car dataset**.

The dataset contains information about used cars, including their prices, manufacturing years, kilometres driven, fuel types, transmission types, and ownership history.

### Important Features
- **Name:** Name of the car.
- **Year:** Manufacturing year of the car.
- **Selling Price:** Selling price of the car.
- **Kilometres Driven:** Total distance travelled by the car.
- **Fuel:** Fuel type of the car.
- **Seller Type:** Type of seller.
- **Transmission:** Manual or automatic transmission.
- **Owner:** Previous ownership category.
- **Car Age:** Age of the car calculated from its manufacturing year.
- **Brand:** Brand extracted from the car name.

The actual dataset columns are checked when the CSV file is loaded.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Joblib

## Machine Learning Algorithms
The following regression algorithms are implemented:

1. **Linear Regression** — predicts car prices using a linear relationship between features and price.
2. **Ridge Regression** — applies regularization to reduce the effect of large model coefficients.
3. **Random Forest Regressor** — combines multiple decision trees to predict prices.
4. **Gradient Boosting Regressor** — builds models sequentially to improve prediction performance.

## Project Workflow
1. Import the required Python libraries.
2. Load the CarDekho dataset from a CSV file.
3. Inspect dataset dimensions, columns, data types, and statistical summaries.
4. Identify missing values and duplicate records.
5. Clean the dataset and validate important numerical columns.
6. Create new features, including car age and brand.
7. Perform Exploratory Data Analysis using visualizations.
8. Analyze the relationships between selling price, car age, mileage, fuel type, and brand.
9. Separate input features and the target variable.
10. Split the dataset into 80% training data and 20% testing data.
11. Apply preprocessing using imputation, scaling, and one-hot encoding.
12. Train and compare four regression models.
13. Evaluate the models using MAE, RMSE, and R² score.
14. Select the leading model based on the lowest test-set RMSE.
15. Perform 5-fold cross-validation.
16. Analyze actual versus predicted prices and residuals.
17. Examine feature importance or absolute model coefficients.
18. Save the cleaned dataset and trained model.

## Exploratory Data Analysis (EDA)
The project uses the following visualizations:

- **Histogram:** Examines the distribution of used-car selling prices.
- **Box Plot:** Compares selling prices across fuel types.
- **Scatter Plot:** Studies the relationship between car age and selling price.
- **Mileage Analysis:** Examines the relationship between kilometres driven and selling price.
- **Brand Comparison:** Compares median prices for the ten most common car brands.
- **Correlation Heatmap:** Shows relationships between numerical features.

These visualizations help identify patterns and understand how different car characteristics relate to selling prices.

## Model Evaluation
The regression models are evaluated using three important metrics.

### 1. Mean Absolute Error (MAE)
MAE measures the average absolute difference between actual and predicted prices. A lower MAE indicates smaller average prediction errors.

### 2. Root Mean Squared Error (RMSE)
RMSE measures prediction errors while penalizing larger errors more strongly. A lower RMSE indicates better performance under this metric.

### 3. R² Score
R² measures how well the model explains variations in selling prices relative to a baseline that predicts the mean price. A higher R² generally indicates better performance.

The models are compared using these metrics, and the model with the lowest test-set RMSE is selected as the leading model.

## Cross-Validation and Feature Analysis
The project uses 5-fold cross-validation to examine how consistently the selected model performs across different training subsets.

It also analyzes feature importance or absolute model coefficients to identify influential predictors. For models without a tree-based feature-importance measure, absolute coefficients are used as a comparison aid.

Actual-versus-predicted plots and residual analysis are used to examine prediction errors.

## How to Run the Project

### Step 1: Install the Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter joblib
```

### Step 2: Start Jupyter Notebook

```bash
jupyter notebook
```

### Step 3: Open the Notebook
Open `3. Car Price Prediction with Machine Learning(2).ipynb`.

### Step 4: Load the Dataset
Run the notebook cells in sequence. When prompted, select the CarDekho dataset CSV file from your computer.

### Step 5: View the Results
Review the generated visualizations, model comparison table, evaluation metrics, cross-validation results, and feature analysis.

### Step 6: Save the Outputs
The notebook allows you to save the cleaned dataset as `cleaned_car_price_dataset.csv` and the trained model as `best_car_price_model.joblib`.

## Results
The project compares Linear Regression, Ridge Regression, Random Forest, and Gradient Boosting using MAE, RMSE, and R² score.

The leading model is selected using test-set RMSE, with cross-validation used as an additional reliability check. The actual model name and performance values depend on the results generated when the notebook is executed.

## Learning Outcomes
- Data cleaning and preprocessing using Pandas.
- Exploratory Data Analysis and data visualization.
- Feature engineering for Machine Learning.
- Encoding categorical variables and scaling numerical features.
- Training and comparing regression algorithms.
- Evaluating models using regression metrics.
- Applying cross-validation.
- Analyzing model predictions and errors.
- Saving trained Machine Learning models.

## Conclusion
This project demonstrates how Machine Learning can be used to estimate used-car selling prices using historical vehicle data. It combines data cleaning, feature engineering, exploratory analysis, regression modelling, model evaluation, cross-validation, and prediction-error analysis.

The results provide an estimate of a used car's selling price based on the available features. Predictions may not reflect current market prices or factors missing from the dataset, such as vehicle condition, location, and service history.
