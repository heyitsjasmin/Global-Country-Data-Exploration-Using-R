# Global Country Data Exploration Using R

**Exploring country-level indicators through data cleaning, descriptive statistics, and data manipulation in R.**

> An academic Data Science assignment using the `world-data-2023` dataset. This repository combines individual exercises and a collaborative data-preparation exercise.

## 📌 Project Overview

This project explores demographic, economic, and social indicators across countries using R. The coursework focuses on extracting relevant information, summarizing variables, handling missing values, converting data types, and reshaping datasets for further analysis.

**Dataset:** `world-data-2023.csv` — 195 countries and 35 variables in the original assignment  
**Tools:** R, `tidyverse` (`dplyr`, `readr`, `tidyr`, and `stringr`)

## 🎯 Objectives

- Practice filtering, sorting, selecting, grouping, and summarizing country-level data.
- Calculate descriptive statistics for numerical indicators.
- Identify missing values and prepare variables for analysis.
- Convert formatted currency and percentage values into numeric variables.
- Reshape summary tables from wide to long format.

## 🔎 Analysis Workflow

### Part 1 — Country Data Exploration (Individual Exercises)

The individual exercises cover:

1. Ranking the 10 countries with the largest **armed forces size**.
2. Identifying countries with **fertility rates lower than Indonesia's**.
3. Summarizing **armed forces size** and **fertility rate** using descriptive statistics.
4. Counting the most commonly recorded **currency codes** in the dataset.
5. Comparing countries in ASEAN with the highest and lowest **infant mortality** values.

### Part 2 — Data Preparation and Transformation (Group Exercises)

The group exercises include:

1. Counting missing values across the dataset.
2. Removing rows with missing values using `drop_na()`.
3. Checking and converting variable types, including columns containing `%` and `$` symbols.
4. Applying a fixed USD-to-IDR conversion used in the coursework.
5. Creating illustrative unemployment-rate categories with `case_when()`.
6. Aggregating GDP and CPI statistics by the custom categories.
7. Reshaping summary results with `pivot_longer()`.

## 📊 Selected Results

| Metric | Result in the original assignment |
| --- | ---: |
| Countries in the raw dataset | 195 |
| Variables in the raw dataset | 35 |
| Missing values detected | 337 |
| Countries remaining after `drop_na()` | 110 |
| Countries with fertility rates below Indonesia's | 98 |

The analysis also identifies these countries at the extremes of **infant mortality within the ASEAN subset**:

| Highest values | Infant mortality | Lowest values | Infant mortality |
| --- | ---: | --- | ---: |
| Laos | 37.6 | Singapore | 2.3 |
| Myanmar | 36.8 | Malaysia | 6.7 |
| Cambodia | 24.0 | Thailand | 7.8 |

*All figures above are outputs from the original coursework dataset, not current country statistics.*

## 📂 Repository Structure

```text
Global Country Data Exploration Using R/
├── Analysis/     # R analysis script / coursework code
├── Datasets/     # Dataset used for the analysis
└── README.md     # Project documentation
```

## ▶️ How to Run

1. Open the R script or R Markdown file in `Analysis/` using RStudio.
2. Install and load `tidyverse` if needed.
3. Set the working directory to the repository root and update the dataset path in the script. For example, if the dataset is named `world-data-2023.csv`:

   ```r
   library(tidyverse)
   data <- read_csv("Datasets/world-data-2023.csv", show_col_types = FALSE)
   ```

4. Run the analysis sections in sequence.

## 📝 Notes & Limitations

- This is an **exploratory data-wrangling assignment**, not a causal or predictive study.
- Complete-case deletion reduced the data from 195 to 110 countries; missing-data patterns should be assessed before using this method for a substantive research project.
- The `Rich`, `Developing`, and `Poor` labels in the coursework were **custom categories defined solely using unemployment-rate thresholds**. They are not official economic-development classifications.
- Currency conversion used a fixed rate for a classroom exercise; it should not be interpreted as a current exchange rate.
- The original assignment presents results as code and tables; it does **not** contain data visualizations.

## 👥 Credits

The independent exercises were completed by **Jasmin Nur Hanifa**. The group section was prepared collaboratively with **Mufrih Nur Huda Tri Putra** and **Nabiilah Rahmatiah Tangke** for the Data Science course.
