# 📊 Data Wrangling
The process of cleaning, transforming, and organizing raw data into a structured and usable format for analysis.

### What is Data Wrangling? 🛠️
Data wrangling, or data munging, involves cleaning, transforming, and organizing raw data into a structured format for analysis. It's essential for ensuring data quality and usability.

#### Key Steps:
1. **🟪 Data Collection and Gathering Data** 📊
2. **🟪 Assessing Data** 🔄
3. **🟪 Data Cleaning** 🧼

## Detail Description 🗒️
1. **🟪 Data Collection and Gathering Data** 📊
   - Gathering raw data from various sources.
     - `i. CSV files`
     - `ii. APIs`
     - `iii. Web Scraping`
     - `iv. Databases ` 

2. **🟪 Assessing Data** 🔄
    - The process you're describing is often referred to as **data assessment** or **data auditing** within the broader field of data wrangling. 
    - During this phase, you evaluate the data to identify any issues, such as missing values, inconsistencies, or errors, but you do not necessarily correct them.

⭐️ **Necessary Steps**
- **Data Profiling**:
   - This involves examining the data for its structure, content, and relationships.
- **Data Quality Assessment**:
   - Checking the data for common quality issues such as: Missing values ,Duplicate records ,Inconsistent data formats, Incorrect data types.
- **Data Consistency**:
   - Ensuring that the data follows specific rules and constraints. For example: Range checks (values fall within a specific range) ,Uniqueness checks (no duplicate primary keys), Referential integrity (foreign key constraints are maintained).
- **Documentation and Summarization**:
   - Documenting all findings and issues identified during the assessment. This includes: Detailed descriptions of the issues ,Potential impact on analysis ,Suggestions for cleaning and transforming the data
  
        
3. **🟪 Data Cleaning** 🧼
   - Cleaning data is the process of fixing or removing incorrect, corrupted, incorrectly formatted, duplicate, or incomplete data within a dataset. This step ensures that the data is accurate, consistent, and usable for analysis.

⭐️ **Necessary Steps**
- **Handle Missing Data**:
  - **Imputation**: Fill missing values using mean, median, mode, or more advanced techniques like KNN imputation.
  - **Removal**: Drop rows or columns with a significant amount of missing data.
  - **Example**: Use `pandas` to fill missing values: `df.fillna(df.mean(), inplace=True)`.
- **Remove Duplicates and Correct Errors**:
  - **Remove Duplicates**: Identify and remove duplicate rows.
  - **Correct Errors**: Fix or remove inconsistent data entries (e.g., typos, incorrect values).
  - **Example**: Remove duplicates using `pandas`: `df.drop_duplicates(inplace=True)`.

## 📅 Worked on at least one dataset daily and solved all the above scenarios.
Happy coding and data prepping! 🚀
