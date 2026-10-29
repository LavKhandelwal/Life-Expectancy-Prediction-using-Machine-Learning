Life Expectancy Prediction Using Machine Learning



About the Project:


This project uses machine learning to predict life expectancy based on health, economic, and social indicators from the WHO life expectancy dataset. It compares Linear Regression, Decision Tree Regression, and Random Forest Regression to evaluate their predictive performance.


Objectives:



- Analyze factors associated with life expectancy.


- Preprocess and prepare the dataset for machine learning.


- Train and compare three regression models.


- Evaluate model performance using standard regression metrics.


- Visualize model performance and feature importance.


- Predict life expectancy using user-provided feature values.



Dataset:


The project uses `Life-Expectancy-Data-Updated.csv`, containing 2,864 records and 21 columns.


The dataset includes variables such as:


- Country and region


- Year


- Infant and under-five deaths


- Adult mortality


- Alcohol consumption


- Immunization indicators, including Hepatitis B, Polio, and Diphtheria


- Measles and HIV incidence


- BMI and nutritional indicators


- GDP per capita and population


- Schooling and economic status


- Life expectancy


The target variable is `Life_expectancy`.


Technologies Used:



- Python


- Pandas


- NumPy


- Matplotlib


- Scikit-learn


- Jupyter Notebook



Machine Learning Models:


1. Linear Regression


Used as a baseline model to estimate life expectancy based on the selected numerical features.



2. Decision Tree Regression


Uses a decision tree to model relationships between the input features and life expectancy.



3. Random Forest Regression


Combines multiple decision trees to predict life expectancy and estimate feature importance.



Project Workflow



1. Data Loading: Load the CSV dataset using Pandas.


2. Data Preprocessing: Handle missing numerical values, prepare features, and encode economic status when applicable.


3. Feature Selection: Remove non-numeric identifiers, exclude the year feature, and filter features based on correlation.


4. Feature Scaling: Standardize the selected features using `StandardScaler`.


5. Model Training: Split the data into training and testing sets using an 80:20 ratio.


6. Model Evaluation: Compare the models using MAE, RMSE, and R² score.


7. Visualization: Plot model R² scores and the top 10 Random Forest feature importances.


8. Prediction: Accept user-provided feature values and predict life expectancy using the trained Random Forest model.


Evaluation Metrics:


- Mean Absolute Error (MAE): Measures the average absolute difference between actual and predicted values.


- Root Mean Squared Error (RMSE): Measures prediction error while penalizing larger errors more heavily.


- R² Score: Measures how well the model explains variation in the target variable.



The notebook displays the evaluation results for all three models. Actual scores depend on the dataset and execution.


Project Structure:

```text
Life-Expectancy-Prediction/
├── Life_Expectancy_Analysis.ipynb
├── Life-Expectancy-Data-Updated.csv
└── README.md
```


Installation and Setup


1. Clone the Repository


```bash
git clone https://github.com/<your-username>/<your-repository>.git
cd <your-repository>
```

Alternatively, download the repository and open its folder in VS Code.



2. Install Dependencies

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```


3. Run the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `Life_Expectancy_Analysis.ipynb` and run the cells in order.

Ensure that `Life-Expectancy-Data-Updated.csv` is in the same directory as the notebook.



Results and Visualizations:


The notebook generates:



- A comparison chart of R² scores for the three regression models.


- A horizontal bar chart showing the top 10 feature importances from the Random Forest model.


- A table comparing MAE, RMSE, and R² scores.


No fixed performance scores are stated here because the results should be taken from an actual notebook execution.


Limitations:

- Predictions depend on the quality and coverage of the dataset.


- The selected features are filtered using a correlation threshold, which may exclude useful nonlinear relationships.


- The notebook uses a random train-test split rather than a time-based split.


- User-provided prediction values must follow the same feature definitions and units as the training data.


- The model estimates statistical relationships and should not be interpreted as proving causation.



Future Enhancements:

- Tune model hyperparameters to improve performance.


- Add cross-validation for more robust evaluation.


- Compare additional regression algorithms.


- Build an interactive prediction interface.


- Improve feature selection and model interpretation.


- Save trained models for reuse without retraining.



License:

No license is currently specified.
