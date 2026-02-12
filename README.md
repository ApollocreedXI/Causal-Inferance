# Causal Inferance
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f2031056-d351-491f-9545-45507643d869" />



<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

## Introduction to the project
Many research papers that analyze factors that contribute to financial well-being are often descriptive and do not make casual inference (Sajid, Mushtaq, Murtaza, Yahiaoui, & Pereira, 2024). They often employ OLS regression to obtain coefficient estimates that describe the impact a unit increase in a particular feature (e.g., financial literary, financial confidence) causes on financial-wellbeing. In my analysis, I intend to move past descriptive analysis by utilizing a casual machine learning framework known as double machine learning which treats observational data as if it were a randomized control trial. By assigning observations to treatment groups within covariate profiles, I will attempt to understand the average treatment affect that financial literacy has on the financial well-being.

## Data provenance
The project utilizes 2024 survey data from the National Financial Capabilities Survey (NFCS). This state-by-state survey occurs every three years, starting in 2009, and captures the financial capabilities of adults in the United States. Each wave consists of over 25,000 individual participants across all 50 states and Washington D.C, making it a well-representative dataset. The survey focuses on four key components: Making ends meet, planning ahead, managing financial products, and financial knowledge. The dataset can be sourced from the NFCS organization’s website at https://finrafoundation.org/data-and-downloads

## Main methods used
Ordinary least squares is one of the main methods employed, and its purpose in this project is for baseline modeling. This modeling methodology attempts to find the regression line that minimizes the squared prediction error of all the data points from the regression line. The purpose of this baseline model is to investigate if being financially literate, as defined by Lusardi and Mitchell, provides a statistically significant improved outcome on financial well-being. 

<img width="623" height="463" alt="image" src="https://github.com/user-attachments/assets/70bce2b4-418f-46df-abfa-789e0423dee0" />


The method employed to evaluate the causality between financial literacy and financial well-being is double machine learning. This method attempts to partial out the effects of the confounders from the treatment (i.e., being financially literate in this case) and financial well-being. With the effect of the confounders removed on the treatment and financial well-being, the average treatment effect of being financially literate on financial well-being can be estimated to gather causal insights. 

## Summary of findings
An important finding is that the indicator variable of whether a participant is financially literate is statistically significant $(t=2.233, p<0.05)$ in our baseline model. On average, after controlling for all other variables, being financially literate is associated with a moderate increase in financial well-being. The statistically significant finding is consistent with other research on financial literacy and its relationship with financial well-being.

After accounting for all covariates, there is no causal impact caused by financial literacy on financial well-being. This finding suggests that the causal effect of outcomes on financial well-being is more complex. Given the statistically significant results found in our OLS regression and its relation with saving and consumption theory, we can say that financial literacy likely still plays a pivotal role in financial well-being, although other factors may have to be considered. For instance, research by Muhammad Sajid and others found a strong positive impact of financial literacy and financial confidence on financial well-being with the intervening effect of financial behaviors ( M. Sajid et al., Financial literacy, confidence and well-being: The mediating role of financial behavior, 2024). This suggests that financial well-being is not just a factor of absolute financial knowledge, but rather a combination of the confidence to act upon this knowledge, shaping an individual's financial behaviors to seek the optimal balance of consumption, saving, and investing for their current financial situation.

## Other Key Findings
<img width="499" height="570" alt="image" src="https://github.com/user-attachments/assets/faf60542-2ba3-4b8f-89d1-aa278ccbe8aa" />

About 1/3 of respondents are financially literate. This corroborates the findings of the S&P Ratings Services Global Financial Literacy Survey that globally, about 2/3 of individuals are not financially literate. 

<img width="870" height="334" alt="image" src="https://github.com/user-attachments/assets/2e87a5e1-a273-4b59-9de7-9064b05255e3" />

Faceting the treatment by gender, we see an interesting pattern. A higher proportion of males is financially literate than the proportion of financially literate women. This finding is consistent with financial literacy research found in the GFLS and a RAND American Life Panel regarding the gender gap in financial literacy.

<img width="1240" height="376" alt="image" src="https://github.com/user-attachments/assets/cb0d52c8-870e-4504-beaf-4e82fbdccd45" />
The ridge plot above suggests that, in aggregate, as an individual achieves higher educational attainment, their overall financial well-being increases as well. 

## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
└── setup.cfg          <- Configuration file for flake8

```
## Reproducibility 
1.	Create a virtual environment
2.	Download the project dependencies via the requirements.txt file in this repository
3.	Download the 2024 NFCS data - https://finrafoundation.org/data-and-downloads
4.	Place the data in a repository that can be referenced by jupyter notebook.
5.	Download the notebook 
6.	Open the notebook and change the “pd.read_csv()” to read the data from your designated repository
7.	Run the remainder of the code
--------



