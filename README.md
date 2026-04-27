# 🏥 Healthy Campus Survey Analysis

A statistical analysis of UC Riverside's Healthy Campus Initiative (HCI) survey data, exploring health concerns and behaviors among students, faculty, and staff. This project focuses on identifying top health concerns overall and examining differences across gender groups using descriptive statistics and chi-square tests.

---

## 📋 Overview

This project analyzes multi-response survey data collected from UC Riverside campus respondents. The analysis covers:

- Overall summary of the most selected health concerns (Q2_1–Q2_29)
- Gender-stratified analysis comparing female and male respondents
- Statistical significance testing using chi-square tests

The goal is to identify which health topics the campus community most wants to learn about, and whether those interests differ significantly by gender.

---

## 📂 Project Structure

```
healthy-campus-survey/
├── BhuvanaK-HCI-code.Rmd       # Main R Markdown analysis file
├── HCI survey data.csv         # Survey dataset (not included in repo)
├── README.md                   # Project documentation
└── output/
    └── BhuvanaK-HCI-code.html  # Knitted HTML output
```

---

## 🔧 Tools & Libraries

| Tool | Purpose |
|------|---------|
| R / RMarkdown | Primary analysis and reporting |
| ggplot2 | Data visualization (gender comparison charts) |
| dplyr | Data manipulation and filtering |
| tidyr | Reshaping data (pivot_longer) |
| base R | Overall summary charts and chi-square tests |

---

## 📊 Dataset

- **Source:** UC Riverside Healthy Campus Initiative (HCI) Survey
- **Variables analyzed:** Q2_1–Q2_29 (health concerns), Q30 (gender)
- **Question type:** Check-all-that-apply (multi-response)
- **Sample:** Campus respondents including students, faculty, and staff
- **Gender breakdown:** ~905 females, ~406 males

> ⚠️ Raw data is not included in this repository due to privacy considerations.

---

## 🧪 Methods

### 1. Data Cleaning
- Loaded raw CSV and checked structure
- Filtered gender variable (`Q30`) to include only `"Female"` and `"Male"` responses
- Converted multi-response columns to binary selected/not-selected indicators

### 2. Overall Summary
- Calculated the percentage of respondents who selected each of the 29 health concern options
- Sorted concerns from highest to lowest selection rate
- Visualized the **top 10 concerns** as a horizontal bar chart

### 3. Gender-Stratified Analysis
- Computed selection percentages separately for female and male respondents
- Created grouped bar charts comparing female vs. male interest across the top 10 concerns
- Used `lightpink` for female and `steelblue` for male bars for visual clarity

### 4. Statistical Testing
- Ran **chi-square tests of independence** for each of the 29 concerns
- Compared gender distributions (female vs. male) for each health topic
- Flagged concerns with `p < 0.05` as statistically significant

---

## 📈 Key Results

### Top 5 Overall Health Concerns
| Concern | % Selected |
|--------|-----------|
| Stress Management | 54.8% |
| Exercise / Fitness | 49.2% |
| Financial Wellness | 45.2% |
| Sleep | 44.4% |
| Healthy Eating | 39.2% |

### Gender Differences (Selected Highlights)
| Concern | Female | Male | Significant? |
|--------|--------|------|-------------|
| Stress Management | 60.4% | 38.5% | ✅ Yes |
| Weight Management | 39.4% | 17.6% | ✅ Yes |
| Mental Health | 39.6% | 29.1% | ✅ Yes |
| Sleep | 48.0% | 37.9% | ✅ Yes |
| Men's Health | 2.6% | 32.4% | ✅ Yes |

Female respondents generally reported higher interest across most health topics. Several concerns showed statistically significant gender differences (p < 0.05), including stress management, sleep, weight management, mental health, and women's/men's health.

---

## ▶️ How to Run

1. Clone this repository:
```bash
git clone https://github.com/bhuvanak04/healthy-campus-survey.git
cd healthy-campus-survey
```

2. Place the survey CSV file in the project root directory:
```
HCI survey data.csv
```

3. Open `BhuvanaK-HCI-code.Rmd` in RStudio

4. Install required packages if needed:
```r
install.packages(c("ggplot2", "dplyr", "tidyr"))
```

5. Knit the file to HTML:
```r
rmarkdown::render("BhuvanaK-HCI-code.Rmd")
```

---

## 👩‍💻 Author

**Bhuvana Kotha**  
B.S. Data Science, University of California Riverside  
[GitHub](https://github.com/bhuvanak04) | bhuvanask.bk@gmail.com

