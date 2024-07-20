<h1><span style="color: lightblue;"> 📊 Data Wrangling ⚡️</span></h1>
The process of cleaning, transforming, and organizing raw data into a structured and usable format for analysis.

### What is Data Wrangling? 🛠️
Data wrangling, or data munging, involves cleaning, transforming, and organizing raw data into a structured format for analysis. It's essential for ensuring data quality and usability.

### Key Steps ⭐️:
1. **🟪 Data Collection and Gathering Data** 📊
2. **🟪 Data Assessment** 🔄
3. **🟪 Data Cleaning** 🧼
4. **🟪 Feature Engineering**🔳

## Detail Description 🗒️
### 🟪 Data Collection and Gathering Data 📊
Data collection is the process of gathering raw data from different sources to analyze and make decisions. Here’s how you can collect data:

- **CSV Files**:
  - **Description**: CSV (Comma-Separated Values) files are simple text files where data is separated by commas. They're commonly used for storing tabular data.
  - **Example**: You can load CSV files using Pandas in Python:
    ```python
    import pandas as pd
    df = pd.read_csv('file.csv')
    ```
- **APIs**:
  - **Description**: APIs (Application Programming Interfaces) allow you to retrieve data from web services. They provide a way for different software systems to communicate.
  - **Example**: You can use requests to fetch data from an API:
    ```python
    import requests
    response = requests.get('https://api.example.com/data')
    data = response.json()
    ```
- **Web Scraping**:
  - **Description**: Web scraping involves extracting data from websites. This is done by parsing HTML or using specific web scraping tools.
  - **Example**: You can use BeautifulSoup in Python to scrape web data:
    ```python
    from bs4 import BeautifulSoup
    import requests
    response = requests.get('https://example.com')
    soup = BeautifulSoup(response.text, 'html.parser')
    ```
- **Databases**:
  - **Description**: Databases store data in structured formats and can be queried to retrieve specific information. Common types include SQL and NoSQL databases.
  - **Example**: You can connect to a SQL database using SQLAlchemy:
    ```python
    from sqlalchemy import create_engine
    engine = create_engine('sqlite:///database.db')
    df = pd.read_sql('SELECT * FROM table', engine)
    ```

### 🟪 Data Assessment 🔄
Data assessment is the process of evaluating your dataset to find issues such as missing values, errors, or inconsistencies. This step helps you understand the state of your data before you start cleaning it.

⭐️ **Basic Steps**
- **Manual Assessment**:
  - **Export and Review**: Save your dataset as a spreadsheet and visually inspect it for issues.
- **Automatic Assessment**:
  - **Programmatic Checks**: Use tools like Pandas to automatically view and analyze your data for problems.

### Necessary Steps
- **Data Profiling**:
  - **Examine Structure**: Look at how the data is organized and understand its relationships.
- **Data Quality Assessment**:
  - **Check for Issues**: Identify missing values, duplicates, inconsistent formats, and incorrect data types.
- **Data Consistency**:
  - **Ensure Rules**: Verify that data meets specific rules like value ranges, uniqueness of keys, and referential integrity.
- **Documentation and Summarization**:
  - **Record Findings**: Document all issues, their potential impact, and suggestions for cleaning and transforming the data.
  
### 🟪 Data Cleaning 🧼
Data cleaning involves fixing or removing incorrect, corrupted, or incomplete data to ensure your dataset is accurate and ready for analysis.

⭐️ **Basic Steps**
- **Handle Missing Data**:
  - **Imputation**: Fill in missing values with the mean, median, mode, or use advanced methods.
  - **Removal**: Delete rows or columns with too many missing values.
  - **Example**:
    ```python
    df.fillna(df.mean(), inplace=True)
    ```
- **Remove Duplicates and Correct Errors**:
  - **Remove Duplicates**: Find and delete duplicate rows.
  - **Correct Errors**: Fix errors or inconsistencies in the data (e.g., typos).
  - **Example**:
    ```python
    df.drop_duplicates(inplace=True)
    ```

### 🟪 Feature Engineering 🔧
Feature engineering is about creating and modifying features (columns) in your dataset to make it better for analysis and machine learning.

⭐️ **Basic Steps**
- **Create New Features**:
  - **Combine Features**: Make new columns by combining existing ones (e.g., total cost = quantity * price).
  - **Extract Date/Time Info**: Break down dates into year, month, etc.
  - **Example**: 
    ```python
    df['total_cost'] = df['quantity'] * df['price']
    ```
- **Transform Features**:
  - **Scale Features**: Adjust the range of numerical values so they're similar.
  - **Encode Categorical Data**: Convert text categories into numbers.
  - **Example**:
    ```python
    from sklearn.preprocessing import StandardScaler
    scaler = StandardScaler()
    df[['feature1', 'feature2']] = scaler.fit_transform(df[['feature1', 'feature2']])
    ```
- **Handle Outliers**:
  - **Find and Treat Outliers**: Remove or adjust extreme values that can skew your data.
  - **Example**:
    ```python
    df = df[(df['feature'] >= lower_bound) & (df['feature'] <= upper_bound)]
    ```
- **Feature Selection**:
  - **Remove Unneeded Features**: Drop columns that don’t help your analysis.
  - **Example**:
    ```python
    df.drop(['unneeded_feature1', 'unneeded_feature2'], axis=1, inplace=True)
    ```
- **Polynomial Features**:
  - **Add Non-Linear Features**: Create features that capture more complex patterns.
  - **Example**:
    ```python
    from sklearn.preprocessing import PolynomialFeatures
    poly = PolynomialFeatures(degree=2)
    df_poly = poly.fit_transform(df[['feature1', 'feature2']])
    ```

## 📅 Worked on at least one dataset daily and solved all the above scenarios.
Happy coding and data prepping! 🚀
