# Project 2 – Air Pollution and Sickle Cell Disease  
**Author:** Ziyuan Wang  
**Course:** BIOSTAT 721  
**Date:** November 17, 2025  

---

## Overview

This project analyzes daily air pollution measurements from the RDU airport monitor between 2018 and 2020. The goal is to clean the raw data and explore seasonal patterns in key pollutants—carbon monoxide (CO), fine particulate matter (PM2.5), and ozone (O₃)—which may be relevant for understanding environmental risk factors for individuals living with sickle cell disease (SCD).

All data processing, visualization, and reporting were conducted in R using R Markdown.

---

## Repository Structure

```
Project2_AirPollution/
│
├── data/
│   ├── AQ_2018.csv
│   ├── AQ_2019.csv
│   └── AQ_2020.csv
│
├── 721-project2-ziyuan-wang-v2.Rmd
├── 721-project2-ziyuan-wang-v2.docx
├── Project2_AirPollution.Rproj
├── renv.lock
├── renv/                  # Package environment created by renv
└── README.md
```

---

## How to Reproduce

### 1. Open the Project  
Download or clone this repository, then open:

```
Project2_AirPollution.Rproj
```

### 2. Restore the R Environment  
The required packages and versions are managed through **renv**.  
Run:

```r
renv::restore()
```

### 3. Knit the R Markdown File  
Render the final report by knitting:

```
721-project2-ziyuan-wang-v2.Rmd
```

---

## Data Description

The `data/` folder contains three daily air quality datasets:

- **AQ_2018.csv**  
- **AQ_2019.csv**  
- **AQ_2020.csv**

Each dataset includes daily measurements for:

- **CO** — Daily maximum 8-hour average  
- **PM2.5** — Daily mean  
- **Ozone** — Daily maximum 8-hour average  

---

## Methods Summary

A custom cleaning function was used to process each annual dataset:

- renaming pollutant variables  
- fixing date formats  
- averaging multiple readings per day  
- removing duplicated rows  
- replacing negative pollutant measurements with zero  

After cleaning, the datasets (2018–2020) were combined into a single unified file.

Monthly summaries and visualizations were then produced:

- CO and ozone monthly averages with **95% confidence intervals**  
- PM2.5 monthly patterns shown **by year**  

---

## Output

The final deliverables include:

- **R Markdown file** → `721-project2-ziyuan-wang-v2.Rmd`  
- **Word report** → `721-project2-ziyuan-wang-v2.docx`  
- Summary tables, cleaned data, and statistical visualizations  

---

## Author

**Ziyuan Wang**  
Duke University  
BIOSTAT 721 Project 2
