---
# HHA507 || NHANES 2021-2023 Inferential Analytics
---
---

#### This repository contains my analysis and documentation for the NHANES 2021-2023 data in performing basic inferential statistics using Python in Google Colab. This includes exploring relationships and differences in health metrics and demographic variables, utilizing the skills learned in class to answer key questions about the dataset.


#### The [`National Health and Nutrition Examination Survey (NHANES)`](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023) is a program of studies designed to assess the health and nutritional status of adults and children in the United States. The survey is unique in that it combines interviews and physical examinations. NHANES is a major program of the National Center for Health Statistics (NCHS). NCHS is part of the `Centers for Disease Control and Prevention (CDC)` and has the responsibility for producing *vital and health statistics* for the nation.

#### Please refer to [**`nhanes_inferential_2023.ipynb`**](___) notebook, which I created using Python in **`Google Colab`**. It contains scripts/codes, and provides easy access to my analysis, including data visualizations where applicable, associated with the scripts and results.

#####  • Courtesy of [Professor Hants Williams' GitHub Repository](https://github.com/hantswilliams/HHA-507-2024/blob/main/Module5/nhanes/NHANES_2022_2023.ipynb)
#####  • For further information and a link to the dataset used in this assignment: [NHANES 2021-2023](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023)

---

## Dataset Overview
#### *The following NHANES variables were used in an attempt to perform the analysis:*

  - **Marital Status** (`DMDMARTZ`)
  - **Education Level** (`DMDEDUC2`)
  - **Age in Years** (`RIDAGEYR`)
  - **Systolic Blood Pressure** (`BPXOSY3`)
  - **Diastolic Blood Pressure** (`BPXODI3`)
  - **Vitamin D Lab Interpretation** (`LBDVD2LC`)
  - **Hepatitis B Lab Antibodies** (`LBXHBS`)
  - **Weak/Failing Kidneys** (`KIQ022`)
  - **Minutes of Sedentary Behavior** (`PAD680`)
  - **Current Self-Reported Weight** (`WHD020`)
    
---
## Inferential Analysis
#### *The following questions were used to perform the analysis:*

   - **Question 1**: "Is there an association between marital status (married or not married) and education level (bachelor’s degree or higher vs. less than a bachelor’s degree)?"  
     - Variables: `DMDMARTZ` (marital status) and `DMDEDUC2` (education level).

   - **Question 2**: "Is there a difference in the mean sedentary behavior time between those who are married and those who are not married?"  
     - Variables: `DMDMARTZ` (marital status, recoded) and `PAD680` (sedentary behavior time, cleaned).

   - **Question 3**: "How do age and marital status affect systolic blood pressure?"  
     - Variables: `RIDAGEYR` (age), `DMDMARTZ` (marital status, recoded), and `BPXOSY3` (systolic blood pressure).

   - **Question 4**: "Is there a correlation between self-reported weight and minutes of sedentary behavior?"  
     - Variables: `WHD020` (self-reported weight, cleaned) and `PAD680` (sedentary behavior time, cleaned).

   - **Question 5 (Creative Analysis)**:


