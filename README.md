---
# HHA507 || NHANES 2021-2023 Inferential Analytics
---
---

#### This repository contains my analysis and documentation for the NHANES 2021-2023 data in performing basic inferential statistics using Python in Google Colab. This includes exploring relationships and differences in health metrics and demographic variables, utilizing the skills learned in class to answer key questions about the dataset.


#### The [`National Health and Nutrition Examination Survey (NHANES)`](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023) is a program of studies designed to assess the health and nutritional status of adults and children in the United States. The survey is unique in that it combines interviews and physical examinations. NHANES is a major program of the National Center for Health Statistics (NCHS). NCHS is part of the `Centers for Disease Control and Prevention (CDC)` and has the responsibility for producing *vital and health statistics* for the nation.

#### Please refer to [**`nhanes_inferential_analysis.ipynb`**](https://github.com/raqssoriano/nhanes_inferential_2023/blob/main/nhanes_inferential_analysis.ipynb) notebook, which I created using Python in **`Google Colab`**. It contains scripts/codes, and provides easy access to my analysis, including steps taken and data visualizations associated with the scripts and results.

#####  • Courtesy of [Professor Hants Williams' GitHub Repository](https://github.com/hantswilliams/HHA-507-2024/blob/main/Module5/nhanes/NHANES_2022_2023.ipynb)
#####  • For further information and a link to the dataset used in this assignment: [NHANES 2021-2023](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023)

---

## Dataset Overview
#### *The following NHANES variables were used in an attempt to perform the analysis:*

  - [**Marital Status**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/DEMO_L.htm#DMDMARTZ) (`DMDMARTZ`)
  - [**Education Level**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/DEMO_L.htm#DMDEDUC2) (`DMDEDUC2`)
  - [**Age in Years**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/DEMO_L.htm#RIDAGEYR) (`RIDAGEYR`)
  - [**Systolic Blood Pressure**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/BPXO_L.htm#BPXOSY3) (`BPXOSY3`)
  - [**Diastolic Blood Pressure**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/BPXO_L.htm#BPXODI3) (`BPXODI3`)
  - [**Vitamin D Lab Interpretation**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/VID_L.htm#LBDVD2LC) (`LBDVD2LC`)
  - [**Hepatitis B Lab Antibodies**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/HEPB_S_L.htm#LBXHBS) (`LBXHBS`)
  - [**Weak/Failing Kidneys**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/KIQ_U_L.htm#KIQ022) (`KIQ022`)
  - [**Minutes of Sedentary Behavior**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/PAQ_L.htm#PAD680) (`PAD680`)
  - [**Current Self-Reported Weight**](https://wwwn.cdc.gov/Nchs/Nhanes/2021-2022/WHQ_L.htm#WHD020) (`WHD020`)
    
---
## Inferential Analysis
#### *The following questions were used to perform the analysis:*

1. **Question 1**: "Is there an association between marital status (married or not married) and education level (bachelor’s degree or higher vs. less than a bachelor’s degree)?"

   - **Answer**: *There is a significant association between marital status and education level.*
   - **Variables**: `DMDMARTZ` (marital status) and `DMDEDUC2` (education level).
   - **Type of Statistical Test used**: **`Chi-Square`** (analyzes the relationship between two categorical key variables)

2. **Question 2**: "Is there a difference in the mean sedentary behavior time between those who are married and those who are not married?"
   
     - **Answer**: *There is no significant difference in the sedentary behavior time between those individuals who are married and those who are not married.*
     - **Variables**: `DMDMARTZ` (marital status) and `PAD680` (sedentary behavior time)
     - **Type of Statistical Test used**: **`T-test`** (compares the means of a continuous two key variables)

3. **Question 3**: "How do age and marital status affect systolic blood pressure?"
   
     - **Answer**:
       - `Marital Status` (DMDMARTZ) on **Systolic BP** - *Main effect*: there is a **statistically significant** effect.
          - F-value: 14996.105454
          - p-value: 0.000000
       - `Age in Years` (RIDAGEYR) on **Systolic BP** - *Main effect*: same with marital status, age has a **statistically significant** effect on SBP.
          - F-value: 1112.368439
          - p-value: 1.722970
       - `Effect for Both Marital Status & Age` - *Interaction effect*: there is a **significant** effect between these demographics on SBP, but not as strong as the individual main effects of marital status and age.
          - F-value: 10.148355 
          - p-value: 3.429116
          
       - **Variables**: `RIDAGEYR` (age), `DMDMARTZ` (marital status), and `BPXOSY3` (systolic blood pressure)
       - **Type of Statistical Test used**: `2-way` **`ANOVA`** (analyzes the effect of two independent variables and a dependent variable)

4. **Question 4**: "Is there a correlation between self-reported weight and minutes of sedentary behavior?"
   
     - **Answer:** There is a **statistically significant** AND **moderate positive** linear relationship between self-reported weight and sedentary behavior time, as shown below. Given the p-value is `<0.05`, there's a <5% chance that these results are due to random variation, and not because of an actual effect. This information is taken from Professor Hants' **Inferential Statistics** powerpoint, found in slide 31.

        - **Pearson Correlation**: `0.1559714584645021` (moderate positive)

        - **p-value**: `1.6988498386828133e-44` (statistically significant)
          
     - **Variables**: `WHD020` (self-reported weight) and `PAD680` (sedentary behavior time)
     - **Type of Statistical Test used**: `Pearson` **`Correlation`** (to analyze the correlation between two continuous key variables)

5. **Question 5 (Creative Analysis)**: "Do different age groups (age in years) have different sedentary behavior?"
   
    - **Answer:** There is **no statistically significant** difference in the minutes of sedentary behavior between different age groups. Given the p-value is `>0.05`, it fails to reject the null hypothesis (no significant difference between groups), in reference to Professor Hants' **Inferential Statistics** powerpoint, found in slide 31.
      
      - **1-Way ANOVA Test Statistic**: `0.11255241591314752`
      - **p-value**: `0.8935528425095732`

    - **Variables**: `RIDAGEYR` (age in years) and `PAD680` (sedentary behavior time)
    - **Type of Statistical Test used**: `1-way` **`ANOVA`** (compares the means of a continuous dependent variable and a single categorical independent variable)
