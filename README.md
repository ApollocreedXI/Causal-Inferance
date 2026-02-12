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

The method employed to evaluate the causality between financial literacy and financial well-being is double machine learning. This method attempts to partial out the effects of the confounders from the treatment (i.e., being financially literate in this case) and financial well-being. With the effect of the confounders removed on the treatment and financial well-being, the average treatment effect of being financially literate on financial well-being can be estimated to gather causal insights. 


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
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         causal_inferance and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
└── setup.cfg          <- Configuration file for flake8

```

--------

