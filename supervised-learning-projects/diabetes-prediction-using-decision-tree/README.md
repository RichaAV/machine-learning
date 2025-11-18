<h1>Diabetes Progression Prediction Using Decision Tree Regression</h1>

<p>A machine-learning project that predicts disease progression for diabetes patients using the Decision Tree Regressor, combined with exploratory data analysis, hyperparameter tuning, and model evaluation.</p>

<h2>Project Overview</h2>

This project uses the Diabetes dataset from sklearn.datasets to build a regression model that predicts a quantitative measure of disease progression one year after baseline.

The workflow includes:

<ul><li>Data loading & preprocessing</li>

<li>Exploratory Data Analysis (EDA)</li>

<li>Visualisation of distributions, correlations, and outliers</li>

<li>Model building using Decision Tree Regressor</li>

<li>Hyperparameter tuning using GridSearchCV</li>

<li>Model evaluation</li>

<li>Visualisation of the final decision tree</li></ul>

<h2>🧰 Tech Stack</h2>

<ul>
<li>Language: Python</li>
<li>Libraries: pandas, NumPy, matplotlib, seaborn, scikit-learn (DecisionTreeRegressor, GridSearchCV, train_test_split, metrics)</li>
<li>Environment: Jupyter Notebook</li></ul>

<h2>🔄 Workflow Summary</h2>
<h3>1. Data Loading</h3>

The Diabetes dataset is loaded using load_diabetes(). Converted to DataFrame with feature columns:age, sex, bmi, bp, s1, s2, s3, s4, s5, s6

Target variable: disease progression score

<h3>2. Exploratory Data Analysis (EDA)</h3>

Performed comprehensive EDA including:

✔️ Correlation Heatmap

Shows relationships among features (bmi, bp, s5 show strong correlations with target).

✔️ Univariate Distribution

Histograms plotted for all 10 features to study distribution shape.

✔️ Outlier Detection

Boxplots for each feature to visually inspect extreme values.

✔️ Pairplot

Explored feature interactions and potential linear/non-linear patterns.

✔️ Missing Values

Dataset has no missing values.

<h3>3. Model Preparation</h3>

Split data into 70% training and 30% testing using train_test_split.

Baseline model: DecisionTreeRegressor().

<h3>4. Hyperparameter Tuning</h3>

Used GridSearchCV (cv = 5) to tune parameters:

<ul><li>criterion: squared_error, friedman_mse, absolute_error, poisson</li>

<li>splitter: best, random</li>

<li>max_depth: various depths from 1 to 25</li>

<li>max_features: sqrt, log2</li></ul>

Best parameters identified were used to generate predictions on the test set.

<h3>5. Model Evaluation</h3>

Evaluated using:

<ul><li>R2 Score</li>

<li>Mean Absolute Error (MAE)</li>

<li>Mean Squared Error (MSE)</li></ul>

Final metrics reflect the model's regression performance on unseen data.
