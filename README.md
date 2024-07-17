# 📊 Data-Preparation-Toolkit

Welcome to **DataCraftTools**, your comprehensive guide and toolkit for mastering essential data preparation techniques in Python! 🐍 This repository offers detailed examples and practical code snippets for data cleaning, transformation, feature engineering, and exploratory data analysis (EDA) using powerful libraries like Pandas, NumPy, Matplotlib, and Scikit-learn. Whether you're a data enthusiast, analyst, or aspiring data scientist, this toolkit will equip you with the skills to efficiently process and analyze datasets for actionable insights.

## 🗂️ Essential Topics Covered

### 🧹 Data Cleaning
- **Handle Missing Data**:
  - **Imputation**: Fill missing values using mean, median, mode, or more advanced techniques like KNN imputation.
  - **Removal**: Drop rows or columns with a significant amount of missing data.
  - **Example**: Use `pandas` to fill missing values: `df.fillna(df.mean(), inplace=True)`.
- **Remove Duplicates and Correct Errors**:
  - **Remove Duplicates**: Identify and remove duplicate rows.
  - **Correct Errors**: Fix or remove inconsistent data entries (e.g., typos, incorrect values).
  - **Example**: Remove duplicates using `pandas`: `df.drop_duplicates(inplace=True)`.

### 🔄 Data Transformation
- **Scaling and Normalization**:
  - **Scaling**: Adjust the range of features (e.g., Min-Max Scaling, Standard Scaling).
  - **Normalization**: Transform features to a standard scale (e.g., normal distribution).
  - **Example**: Use `scikit-learn` for standard scaling: `from sklearn.preprocessing import StandardScaler; scaler = StandardScaler(); df_scaled = scaler.fit_transform(df)`.
- **Encoding Categorical Variables**:
  - **One-Hot Encoding**: Convert categorical variables to binary vectors.
  - **Label Encoding**: Assign unique numerical values to each category.
  - **Example**: One-hot encoding with `pandas`: `pd.get_dummies(df, columns=['category_column'])`.
- **Date and Time Transformations**:
  - Extract useful information from date and time fields (e.g., year, month, day, hour).
  - Create new features based on date and time (e.g., day of the week, weekend indicator).
  - **Example**: Extract year from a date column: `df['year'] = df['date_column'].dt.year`.

### 🛠️ Feature Engineering
- **Creating New Features**:
  - Generate new features by combining or transforming existing ones (e.g., polynomial features, interaction terms).
  - **Example**: Create polynomial features: `from sklearn.preprocessing import PolynomialFeatures; poly = PolynomialFeatures(degree=2); df_poly = poly.fit_transform(df)`.
- **Feature Selection**:
  - Use techniques to retain important features and remove redundant ones (e.g., correlation thresholding, LASSO).
  - **Example**: Feature selection with LASSO: `from sklearn.linear_model import Lasso; lasso = Lasso(); lasso.fit(X, y); important_features = X.columns[lasso.coef_ != 0]`.

### 🔍 Exploratory Data Analysis (EDA)
- **Visualizing Data**:
  - Use various plots to understand data distributions (e.g., histograms, box plots, scatter plots).
  - **Example**: Use `matplotlib` or `seaborn` for visualization: `import seaborn as sns; sns.histplot(df['column_name'])`.
- **Identifying Outliers and Anomalies**:
  - Detect and analyze outliers using visualization and statistical methods (e.g., Z-score, IQR).
  - **Example**: Identify outliers with Z-score: `from scipy import stats; df['zscore'] = stats.zscore(df['column_name']); outliers = df[df['zscore'].abs() > 3]`.

## 📚 Total Recommended Questions To Become Proficient

### Data Cleaning
- **Imputation**: 5-7 questions/datasets
- **Removal**: 3-5 questions/datasets
- **Remove Duplicates**: 3-5 questions
- **Correct Errors**: 3-5 questions
- **Total**: 14-22 questions

### Data Transformation
- **Scaling and Normalization**: 5-7 questions
- **One-Hot Encoding**: 3-5 questions
- **Label Encoding**: 3-5 questions
- **Date and Time Transformations**: 5-7 questions
- **Total**: 16-24 questions

### Feature Engineering
- **Creating New Features**: 5-7 questions
- **Feature Selection**: 5-7 questions
- **Total**: 10-14 questions

### Exploratory Data Analysis (EDA)
- **Data Distributions**: 5-7 questions
- **Correlations and Patterns**: 5-7 questions
- **Identifying Outliers and Anomalies**: 5-7 questions
- **Total**: 15-21 questions

**Overall Total**: 55-81 questions

## 📅 Daily Questions To Solve

- **Beginner Level**: 3-5 questions per day
- **Intermediate Level**: 2-3 questions per day
- **Advanced Level**: 1-2 questions per day

Happy coding and data prepping! 🚀
