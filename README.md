# East Africa Financial Inclusion Analysis
Exploratory data analysis of socio-economic factors associated with bank account ownership across four East African countries.

## Socio-Economic Drivers of Financial Inclusion in East Africa

**A Python data analysis project by Ismaila Ainoko Aminu**

This project explores patterns of formal bank account ownership across Kenya, Rwanda, Tanzania and Uganda. I used Python to examine how bank account ownership varies across geographic, demographic and socioeconomic groups, with the aim of identifying groups that appear to face greater barriers to formal financial access.

The project was completed as part of my Python data analytics learning journey with **SmartBizCrux Technologies**, under the guidance of **Coach Timothy Amaefule**. I worked on the analysis with my project buddy, **Ayomide Eniafe Emmanuel**.


## 1. Project Background

Access to formal financial services can make it easier for people to save, receive and make payments, and participate in the wider economy. However, access is not the same for everyone.

I chose this project to better understand how financial inclusion differs across communities and what characteristics are associated with having a formal bank account. My interest was to use data to identify patterns that financial institutions and policymakers may need to consider when designing financial inclusion initiatives.

## 2. Problem Statement

Financial institutions and policymakers need a clearer understanding of which groups are less likely to have access to formal banking. Without examining the data across different population groups, it can be difficult to identify where financial inclusion gaps are most visible.

This analysis investigates differences in bank account ownership across countries and by location, cellphone access, education, employment, gender and age.

## 3. Project Objective

The main objective was to explore patterns of bank account ownership in the selected East African countries and identify demographic, geographic and socioeconomic characteristics associated with access to a formal bank account.

### Questions Explored

- What proportion of respondents reported having a bank account?
- How did bank account ownership differ across the four countries?
- Was ownership different between rural and urban respondents?
- How did reported cellphone access relate to bank account ownership?
- How did ownership vary by education level and employment type?
- Were there differences between male and female respondents?
- How did bank account ownership vary across age groups?

## 4. Dataset

The project used the **East Africa Financial Inclusion Survey** dataset. The project methodology identifies the data as coming from FinMark Trust's FinScope Consumer Surveys across Kenya, Rwanda, Tanzania and Uganda.

| Dataset detail | Description |
|---|---|
| Records | 23,524 respondents |
| Columns | 13 original variables |
| Countries | Kenya, Rwanda, Tanzania and Uganda |
| Main outcome variable | `bank_account` |
| Data format | CSV |

### Main Variables Used

- `country` — respondent's country
- `bank_account` — whether the respondent reported having a bank account
- `location_type` — rural or urban residence
- `cellphone_access` — whether the respondent reported cellphone access
- `age_of_respondent` — respondent's age
- `gender_of_respondent` — respondent's gender
- `education_level` — respondent's education category
- `job_type` — respondent's employment or income category

Other fields in the dataset include survey year, household size, unique respondent ID, relationship with household head and marital status.

## 5. Tools and Technologies

- **Python** — programming language used for the analysis
- **Jupyter Notebook** — environment used to write and run the analysis
- **Pandas** — loading, inspecting, grouping and summarising the data
- **NumPy** — numerical computing support
- **Matplotlib** — creating charts and visualising results
- **Seaborn** — imported in the notebook as an additional visualisation library

## 6. Approach and Methodology

I followed an exploratory data analysis (EDA) approach.

### Step 1: Load and Inspect the Data

I loaded the CSV file into a Pandas DataFrame and used methods such as `head()`, `describe()`, `columns`, `dtypes` and `shape` to understand the records, variables and data types.

### Step 2: Check Data Quality

I checked the dataset for missing values and duplicate rows using `isnull().sum()` and `duplicated().sum()`.

The checks returned **zero missing values across the columns and zero duplicate rows**. Based on these checks, no missing-value removal or duplicate-row removal was needed for this analysis.

### Step 3: Explore Bank Account Ownership

I used `value_counts(normalize=True)` to calculate the overall percentage of respondents with and without a bank account. I then used `groupby()` and `value_counts(normalize=True)` to compare ownership across countries and other categories.

### Step 4: Create Age Groups

I examined the age distribution and used `pandas.cut()` to group respondents into four age bands:

- Youth (16–25)
- Young Adult (26–35)
- Adult (36–50)
- Senior (51+)

I then used a cross-tabulation to calculate bank account ownership percentages within each age group.

### Step 5: Visualise and Interpret the Results

I used bar charts to present the percentage of respondents with bank accounts across the different groups. The charts were intended to make differences easier to compare and communicate.

## 7. Key Findings

The results below are based on the calculations saved in my notebook. Percentages are rounded to two decimal places.

### Overall Bank Account Ownership

- **14.08%** of respondents reported having a bank account.
- **85.92%** reported not having a bank account.

This shows that most respondents in the dataset did not report owning a bank account.

### Differences Across Countries

| Country | Respondents with a bank account |
|---|---:|
| Kenya | 25.07% |
| Rwanda | 11.48% |
| Tanzania | 9.17% |
| Uganda | 8.61% |

Kenya had the highest bank account ownership rate in this sample, while Uganda had the lowest.

### Residential Location

| Location | Respondents with a bank account |
|---|---:|
| Urban | 17.87% |
| Rural | 11.65% |

The percentage was higher among urban respondents than rural respondents, showing a difference in reported access by residential location.

### Cellphone Access

| Cellphone access | Respondents with a bank account |
|---|---:|
| Yes | 18.38% |
| No | 1.71% |

Respondents who reported cellphone access had a higher bank account ownership rate than those who did not report cellphone access. This is an association in the survey data; it does not establish that cellphone access alone leads to bank account ownership.

### Education Level

| Education level | Respondents with a bank account |
|---|---:|
| No formal education | 3.90% |
| Primary education | 8.55% |
| Secondary education | 23.28% |
| Tertiary education | 51.08% |
| Vocational/Specialised training | 57.04% |
| Other / Don't know / RTA | 31.43% |

The highest rates in the listed categories were among respondents with vocational or specialised training and tertiary education. The lowest was among respondents with no formal education.

### Employment Type

Some differences in bank account ownership by job type were:

| Job type | Respondents with a bank account |
|---|---:|
| Formally employed Government | 77.52% |
| Formally employed Private | 54.12% |
| No Income | 2.07% |
| Informally employed | 7.95% |
| Farming and Fishing | 11.67% |
| Self employed | 13.17% |

Formal employment categories had higher ownership rates than several other employment or income categories in this dataset. The full notebook includes additional job categories.

### Gender

| Gender | Respondents with a bank account |
|---|---:|
| Male | 18.97% |
| Female | 10.68% |

The bank account ownership rate was higher among male respondents than female respondents in the survey.

### Age Group

| Age group | Respondents with a bank account |
|---|---:|
| Youth (16–25) | 8.50% |
| Young Adult (26–35) | 16.81% |
| Adult (36–50) | 17.37% |
| Senior (51+) | 12.82% |

The 36–50 age group had the highest ownership rate, while the 16–25 age group had the lowest.

## 8. What the Findings Suggest

Across the groups examined, bank account ownership was not evenly distributed. The analysis showed differences by country, residential location, cellphone access, education, employment, gender and age.

These patterns suggest that financial inclusion efforts may benefit from paying closer attention to rural communities, people without cellphone access, respondents with lower levels of formal education, people without income or in informal work, women and younger respondents.

The results can help frame further questions for financial institutions and policymakers. For example, they may investigate whether service availability, affordability, documentation requirements, income stability, digital access or financial literacy contribute to the differences observed.

## 9. Limitations

- This is an exploratory analysis of survey data and is limited to the variables available in the dataset.
- The analysis identifies associations and differences between groups; it does not prove that any one factor causes bank account ownership.
- The percentages describe the respondents represented in this dataset. They should not automatically be treated as current population-wide rates for all of East Africa.
- The analysis is descriptive. It does not use a causal model to isolate the effect of each factor from other characteristics.

## 10. Conclusion

This project gave me an opportunity to apply Python to a practical data analysis question. By inspecting the dataset, checking its quality, calculating group-level percentages and creating visualisations, I was able to identify clear differences in reported bank account ownership across the four countries and population groups.

One of the main lessons from this analysis is that financial inclusion should not be viewed as a single overall figure. Looking at the data by location, education, employment, gender, age and cellphone access gives a more detailed picture of which groups may be underserved.

As I continue developing my skills in Python and data analytics, this project has helped me practise turning raw survey data into findings that can support further investigation and decision-making.


## Exploratory Data Analysis & Visualizations

This section presents the key findings from the analysis, including the Python calculations, outputs, and visualizations used to investigate financial inclusion across East Africa.

### 1. Overall Bank Account Access in East Africa

Across the dataset, only **14.08%** of respondents own a bank account, while **85.92%** remain unbanked. This highlights the significant financial inclusion gap across the four countries.

**Calculation Code:**

![Overall Bank Account Access Calculation Code](visuals/visual%201i.png)

**Calculation Output:**

![Overall Bank Account Access Calculation Output](visuals/visual%201ii.png)

**Visualization Code:**

![Overall Bank Account Access Visualization Code](visuals/visual%201iii.png)


### 2. Bank Account Ownership by Country

Kenya leads in bank account ownership at **25.07%**, followed by Rwanda (**11.48%**), Tanzania (**9.17%**), and Uganda (**8.61%**). This reveals considerable differences in financial inclusion across the countries studied.

**Calculation Code:**

![Bank Account Ownership by Country Calculation Code](visuals/visual%202i.png)

**Calculation Output:**

![Bank Account Ownership by Country Calculation Output](visuals/visual%202ii.png)

**Visualization Code:**

![Bank Account Ownership by Country Visualization Code](visuals/visual%202iii.png)

### 3. Residential Location and Cell Phone Access

Respondents in **urban areas** have higher bank account ownership (**17.87%**) than those in rural areas (**11.65%**).

Cell phone access also shows a strong relationship with financial inclusion: **18.38%** of respondents with phone access own a bank account, compared with just **1.71%** of those without phone access.

**Calculation Code:**

![Location and Cell Phone Access Calculation Code](visuals/visual-3i.png)

**Calculation Output:**

![Location and Cell Phone Access Calculation Output](visuals/visual%203ii.png)

**Visualization Code:**

![Residential Location and Cell Phone Access Visualization Code](visuals/visual%203iii.png)

### 4. Socioeconomic and Demographic Drivers

The analysis shows a relationship between bank account ownership, education, and employment.

For example, **77.52%** of government-employed respondents and **57.04%** of respondents with vocational or specialised training own a bank account. In comparison, only **3.90%** of respondents with no formal education own one.

**Calculation Code:**

![Socioeconomic and Demographic Drivers Calculation Code](visuals/visual%204i.png)

**Calculation Output:**

![Socioeconomic and Demographic Drivers Calculation Output](visuals/visual%204ii.png)

**Visualization Code:**

![Socioeconomic and Demographic Drivers Visualization Code](visuals/visual%204iii.png)


- **Analyst:** Ismaila Ainoko Aminu
- **Project buddy:** Ayomide Eniafe Emmanuel
- **Learning programme:** SmartBizCrux Technologies
- **Coach:** Timothy Amaefule
