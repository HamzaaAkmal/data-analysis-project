### First Semester BSDS1-A Data Analysis Project using Pandas

# Medical Students Health Analysis

## About the Dataset

This project utilizes a dataset sourced from [Kaggle](https://www.kaggle.com/), containing information about medical students and their health activities. The dataset includes variables such as age, weight, smoking habits, diabetes status, and other health-related factors.

## Project Objectives 

This project aims to analyze the health activities and patterns of medical students by addressing the following key questions:

1.  **Gender Distribution:** What is the Gender distribution of medical students in the dataset?
2.  **Smoking Habits:** How many students in the dataset are smokers?
3.  **Diabetes Affected Students :** How many students have been affected with diabetes in Age Group?
4.  **BMI distribution with Gender:** What is the Body Mass Index (BMI) distribution of the students Gender?
5.  **Conclusion**

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
    ![Age Group Distribution](./Gender_Age_Group.png)
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
    ![Diabetes Distribution](./BMI_Age_Group.png)
    *Bar chart showing the number of students with and without diabetes in each age group.*
    ```

## Conclusion

This exploratory data analysis of medical student health data provides valuable preliminary insights into the health profiles of the students within this dataset.  By addressing the key research questions, we've uncovered the following trends:

1.  **Age Groupings Highlight a Predominantly Young Adult Population:**  The dataset primarily represents medical students in the **19-30 year age range**, with the largest group falling into the **26-30 Years** category. 
   

2.  **Low Smoking Rates Suggest Health-Conscious Behavior:**  The visualization of smoking habits by age group demonstrably illustrates that the overwhelming majority of students are **non-smokers**. Thus very low smoking prevalence, consistent across all age categories and genders, is a positive indicator of health-conscious behavior among medical students.

3.  **Diabetes Rate:** Diabetes diagnosis rates are also remarkably low across all age groups, with **most students not reporting a diabetes diagnosis.**  While this is encouraging, it is important to acknowledge the presence of diabetes cases, especially in the older age cohorts (31-34 years). Continued monitoring and preventative measures should remain a priority, especially as the student population ages.

4.  **BMI Analysis Indicates Focus Needed on Weight Management:** The BMI category distribution analysis reveals a nuanced picture of student weight status.  While a substantial portion of students fall within the **"Normal" BMI range**, a considerable number are classified as **"Overweight,"** and a smaller but significant group falls into the **"Obese" category.** Additionally, a portion of students are categorized as **"Underweight."**  This distribution pattern suggests that, while many students maintain a healthy weight, targeted interventions focusing on weight management, nutrition education, and promoting balanced lifestyles could be beneficial, particularly for addressing the "Overweight" and "Obese" categories and supporting healthy weight gain for "Underweight" students.

**Overall Project Conclusion and Future Directions:**

This initial analysis paints a picture of a relatively healthy medical student population, particularly in terms of low smoking and diabetes rates. However, the analysis also highlights a potential area for focused health promotion and intervention regarding weight management, given the non-negligible percentage of students classified as "Overweight" or "Obese."


