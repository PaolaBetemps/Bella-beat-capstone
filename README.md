# Bellabeat Capstone
*Data analysis and insights from the Bellabeat Capstone Project, including data cleaning, visualization, and recommendations.*

## 🔗 Quick Links
- 📊 [Advanced HTML report (download/view)](./bellabeat_advanced.html)
- 📄 [Basic HTML report](./02_report.html)

> **Tip:** To host the HTML as a live web page, enable **GitHub Pages** (Settings → Pages).  
> Rename `bellabeat_advanced.html` to `index.html` and choose branch `main` / root.  
> Your report will then be available at the URL that GitHub Pages shows after you enable it.

---

## 📚 Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Visual Highlights](#visual-highlights)
- [Recommendations](#recommendations)
- [Repository Structure](#repository-structure)
- [Reproducibility](#reproducibility)
- [Acknowledgements](#acknowledgements)

---

## Project Overview
This project analyzes Fitbit daily activity and sleep logs to uncover usage patterns and derive actionable insights for **Bellabeat**, a smart wellness company.  
The analysis includes data cleaning, KPI computation, exploration, and visual storytelling.

**Objectives**
- Understand users’ daily steps and sleep behavior.  
- Identify weekday/weekly patterns and correlations.  
- Provide data-driven recommendations for product and marketing.

---

## Data Source
Fitbit Fitness Tracker data (public Kaggle dataset).  
Period covered in the sample: **2016-04-12 to 2016-05-12**.  
Tables used include daily activity, sleep, and weight logs (weight used only where available).

> **Note:** The sample is small (~30 users / 31 days). Insights illustrate an approach rather than population-level conclusions.

---

## Methodology
- **Cleaning:** remove duplicates, standardize column names and dates, derive helper features (weekday, week).  
- **KPIs:** unique users, rows, median/mean steps, median/mean sleep (hours), correlation (steps vs. sleep).  
- **Exploration & Viz:** distribution of steps, steps × sleep relationship, weekday and weekly trends, top users.  
- **Communication:** RMarkdown reports with Cosmo theme, floating TOC, and code folding.

---

## Key Findings
- Most users **did not reach 10,000 steps/day** on average.  
- **Sleep averages ≈ 7 hours**, with considerable variability across days/users.  
- **Steps vs. sleep shows a weak negative correlation** in this sample.  
- Activity tends to **vary by weekday**; weekly medians fluctuate across ISO weeks.  
- Only a **subset** of users logged weight.

---

## Visual Highlights
- **Distribution of Daily Steps** – long right tail with some very high-activity days.  
- **Sleep (hours) vs. Steps** – weak linear trend, substantial scatter.  
- **Average Steps by Weekday** – visible differences across days.  
- **Median Steps by ISO Week** – week-to-week variability.  
- **Top 10 Users by Average Steps** – leaderboard of the most active users.

See the full visuals in the **[advanced HTML report](./bellabeat_advanced.html)**.
> (or via GitHub Pages after you enable it).

---

## Recommendations
- Set **weekday-specific goals** and nudges to address variability.  
- Provide **sleep coaching nudges** after unusually high/low activity days.  
- Send **weekly summaries** to sustain engagement and highlight progress.

---

## Repository Structure
```
project.Rproj                # RStudio project file
bellabeat_advanced.Rmd       # Advanced report (RMarkdown)
bellabeat_advanced.html      # Advanced HTML report
02_report.Rmd                # Basic report (RMarkdown)
02_report.html               # Basic HTML report
bellabeat-capstone/          # Zipped folder with project files
```

---

## Reproducibility
**Environment:** R (Posit/RStudio).  
**Core packages:** `tidyverse`, `lubridate`, `janitor`, `here`, `skimr`, `scales`, `forcats`, `knitr`, `rmarkdown`.

Install essentials:
```r
install.packages(c("tidyverse","lubridate","janitor","here","skimr","scales","forcats","knitr","rmarkdown"))
rmarkdown::render("bellabeat_advanced.Rmd", output_format = "html_document")
```
---

## Acknowledgements
- [Fitbit Fitness Tracker dataset](https://www.kaggle.com/datasets/arashnic/fitbit) (Kaggle)  
- [Google Data Analytics Capstone](https://www.coursera.org/professional-certificates/google-data-analytics) framework


