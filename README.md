# Predicting and Preventing Theme Park Incidents 🎢

## Overview

This project explores how machine learning can be used to predict and prevent guest incidents at Orlando theme parks by analyzing 20 years of reported safety events and weather conditions. By combining structured data (temperature, precipitation) and unstructured data (incident descriptions), the project seeks to identify risk patterns that could support smarter operational planning and enhanced guest safety.

This is a data-driven exploration—not a final solution—but it offers a promising foundation for proactive safety strategies in large public environments.

## Author

[@miles-alexander](https://github.com/miles-alexander)

---

## Research Questions

      1. Are theme park incidents more likely to occur under certain weather conditions?
      2. Can we predict which incidents are likely to be more severe?
      3. Which rides or attractions report the most frequent incidents?
      4. Are there specific symptoms or keywords commonly associated with reported incidents?
      5. How might this model help with staffing and ride operations?

---

## Approach

**Data Cleaning**

* Standardized attraction and park names
* Merged incident and weather datasets by date
* Tokenized and cleaned incident descriptions for NLP

**Exploratory Data Analysis (EDA)**

* Identified top attractions by incident count
* Analyzed temperature and precipitation on incident vs. non-incident days
* Ran statistical tests (t-tests) for significant differences

**Machine Learning**

* Trained a Random Forest classifier to predict severity of incidents
* Evaluated precision, recall, and F1-score

**NLP (Natural Language Processing)**

* Applied TF-IDF to identify common keywords
* Created visualizations to highlight trends in descriptions (e.g., “fainted,” “dizzy,” “pain”)

---

## Data Sources & Preparation

This project uses publicly available data from state records and weather services.

**FDACS Incident Reports**

   * Source: \[Florida Department of Agriculture & Consumer Services (FDACS)]
   * Range: 2002–2022
   * Total: 682 incidents at Walt Disney World and Universal Studios Orlando

**Weather Data**

   * Source: \[Florida State University Climate Center]
   * Location: Orlando International Airport station
   * Includes: Daily precipitation, min/max/mean temperatures

---

## How to Use

To replicate or review the analysis:

- Download the notebook 
   ```bash
   PredictingAndPreventingThemeParkIncidents.ipynb
   ```
      
- Ensure you have Python 3.x and the following libraries installed:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn nltk
   ```
   
- Open the notebook in Jupyter and run all cells to view full analysis and results

- Visualizations and model outputs will appear inline

---

## Key Findings

**Hot weather matters:**
14.98% of all incidents occurred on the hottest 10% of days. Statistically significant.

**Rain doesn't:**
Incident frequency on rainy days was not meaningfully different from average.

**Severity prediction is possible:**
A Random Forest model using ride, park, and weather features could classify incidents as “severe” with strong accuracy.

**Most common symptoms:**
Keywords like "pain," "fainted," and "chest" were frequently used in reports—many related to heat or medical events.

---

## Limitations

* No data on guest attendance or crowd size
* Incident descriptions are often vague or inconsistent
* Weather data lacks humidity and heat index
* No time-of-day available for reports

---

## Ethical Considerations

* Models should not be used to exclude guests or penalize based on health or demographics
* Full transparency is necessary for real-time deployment
* Systems should be regularly audited for bias

---

## Conclusion

This project highlights how historical data and machine learning can work together to help prevent future incidents. While not perfect, the findings underscore the importance of heat-related planning and the potential for proactive safety alerts in high-traffic environments like theme parks.

---

## Future Work

* Add crowd-level data from mobile apps or ride wait times
* Deploy real-time dashboards using tools like Power BI or Tableau
* Expand model to other locations like concerts, airports, or cruises
* Fine-tune severity classifications with labeled outcomes
