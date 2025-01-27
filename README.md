# Medical Students Health Analysis

## About the Dataset

This project utilizes a dataset sourced from [Kaggle](https://www.kaggle.com/), containing information about medical students and their health activities. The dataset includes variables such as age, weight, smoking habits, diabetes status, and other health-related factors.

## Project Objectives (Research Questions)

This project aims to analyze the health activities and patterns of medical students by addressing the following key questions:

1.  **Age Distribution:** What is the age distribution of medical students in the dataset?
2.  **Smoking Prevalence:** How many students in the dataset are smokers?
3.  **Diabetes Prevalence:** How many students have been diagnosed with diabetes, and how does diabetes prevalence vary across different age groups and genders?
4.  **BMI and Weight Relationship:** What is the Body Mass Index (BMI) distribution of the students?

## Content of Notebook (`analysis.ipynb`)

The Jupyter Notebook (`analysis.ipynb`) performs the following steps:

1.  **Libraries Import and Data Description:**
    - Imports the `pandas` library for data manipulation.
    - Loads the dataset from `medical.csv` into a Pandas DataFrame.
    - Provides initial data exploration using `head()`, `info()`, `describe()`, and `shape` to understand data structure, types, and basic statistics.

2.  **Data Preprocessing and Cleaning:**
    - Selects relevant columns for analysis: 'Age', 'Gender', 'BMI', 'Smoking', 'Diabetes'.
    - Handles missing values using median imputation for 'Age' and 'BMI' and mode imputation ('No') for categorical features 'Smoking' and 'Diabetes'.
    - Removes duplicate rows and rows with missing 'Gender' values.
    - Confirms data cleaning by checking for remaining missing values.

3.  **Creating Age Groups for Analysis:**
    - Defines age bins and labels to categorize students into age groups: '0-18 Years', '19-25 Years', '26-30 Years', '31-34 Years'.
    - Creates a new 'Age Group' column based on these categories using `pd.cut`.

4.  **Exploratory Data Analysis (EDA) and Visualizations:**
    - **Age Group Distribution:** Calculates and visualizes the distribution of students across age groups, broken down by gender.

    ```markdown
    ![Gender_Age_Group.png](https://downlabs.org/wp-content/uploads/2025/01/Gender_Ag_Grou-768x445.png)

    *Bar chart showing the number of male and female students in each age group.*
    ```

    - **BMI Category Distribution:** Calculates and visualizes the distribution of students across BMI categories ('Underweight', 'Normal', 'Overweight', 'Obese'), broken down by gender.

    ```markdown
    ![BMI Category Distribution](INSERT_RELATIVE_PATH_TO_BMI_CATEGORY_DISTRIBUTION_IMAGE_HERE)
    *Bar chart showing the number of male and female students in each BMI category.*
    ```

    - **Smoking Habits Distribution:** Calculates and visualizes the distribution of smoking habits (Smoker/Non-Smoker) across age groups.

    ```markdown
    ![Smoking Habits Distribution](INSERT_RELATIVE_PATH_TO_SMOKING_HABITS_DISTRIBUTION_IMAGE_HERE)
    *Bar chart showing the number of smokers and non-smokers in each age group.*
    ```

    - **Diabetes Distribution:** Calculates and visualizes the distribution of diabetes diagnosis (Yes/No) across age groups.

    ```markdown
    ![Diabetes Distribution](INSERT_RELATIVE_PATH_TO_DIABETES_DISTRIBUTION_IMAGE_HERE)
    *Bar chart showing the number of students with and without diabetes in each age group.*
    ```
## Conclusion

This project reveals a **predominantly healthy profile of medical students** within the dataset, characterized by a balanced gender distribution, concentration in typical medical education age ranges, a majority with normal BMI, and low rates of smoking and diabetes.

**Key Outcomes:**

- **Age Group Distribution:** The **26-30 Years** age group represents the largest segment of medical students in the dataset, followed closely by the "19-25 Years" group.

- **Gender Distribution by Age Group:**
    - **Balanced Overall:**  Gender distribution is generally balanced across all age groups.
    - **Largest Group:** The **26-30 Years** age group is the largest overall and also exhibits a balanced number of males and females (250 Females, 247 Males).
    - **Youngest Group Variation:** The youngest age group ("0-18 Years") shows a slight male majority (29 Males vs 25 Females).

- **BMI Category Distribution by Gender:**
    - **Normal BMI is Most Common:**  The "Normal" BMI category is the most frequent for both genders.
    - **Overweight Males Slightly Higher:**  There are slightly more overweight males than females in the dataset.
    - **Healthy Weight Majority:**  Overall, a significant portion of the medical students maintain a healthy weight, as indicated by the dominance of the "Normal" BMI category.

- **Smoking Habits Distribution by Age Group:**
    - **Lowest Smoking in Older Groups:** Smoking prevalence is lowest in the older age groups ("31-34 Years"), with a minimal number of smokers.
    - **Younger Groups Show Slightly More Smokers:**  The "19-25 Years" and "26-30 Years" age groups have slightly higher numbers of smokers compared to the oldest and youngest groups, although still a minority.
    - **Non-Smoking Predominant:**  Across all age groups, the "No Smoking" category is overwhelmingly dominant, emphasizing a strong non-smoking trend.

- **Diabetes Distribution by Age Group:**
    - **Lowest Diabetes in Younger Groups:** Diabetes is least prevalent in the youngest age groups ("0-18 Years" and "19-25 Years"), with very few diagnosed cases.
    - **Slight Increase in Older Groups:** The "26-30 Years" and "31-34 Years" age groups show a marginal increase in diabetes cases, but the overall prevalence remains low.
    - **Low Diabetes Overall:**  Diabetes is not a common condition within this medical student population, regardless of age group, but older students show a slightly elevated risk.

**Overall Conclusion:**

The dataset shows a picture of medical students who are generally healthy, particularly regarding smoking and weight. While diabetes prevalence is low, a slight age-related increase suggests a need for age-tailored health awareness. The 26-30 year age group is the largest and most balanced in terms of gender, representing a core demographic within the medical student population. Notably, **no single age group stands out as smoking more than others; smoking is consistently low across all ages.**  This analysis provides a valuable baseline for understanding the health profiles of future medical professionals and points to areas for potential health promotion efforts targeted at older students.

---


**Libraries Used:**

*   **pandas:**  Data manipulation and analysis in tabular format.

**Functions and Techniques Used:**

*   **Data Preprocessing:** Missing value handling, data cleaning, categorical data conversion.
*   **Exploratory Data Analysis (EDA):** Descriptive statistics, data visualization using bar charts, data grouping with `groupby()`, data binning with `pd.cut()`.
*   **Functions:** `pandas.read_csv()`, `pandas.DataFrame.head()`, `pandas.DataFrame.info()`, `pandas.DataFrame.describe()`, `pandas.DataFrame.isnull().sum()`,  `pandas.DataFrame.fillna()`, `pandas.DataFrame.dropna()`, `pandas.DataFrame.duplicated()`, `pandas.DataFrame.drop_duplicates()`, `pandas.DataFrame.groupby()`, `pandas.DataFrame.plot()`, `pandas.cut()`, `pandas.DataFrame.value_counts()`.
