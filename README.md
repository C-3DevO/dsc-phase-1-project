
#  Aircraft Safety Intelligence: A Data-Driven Risk Analysis for Strategic Fleet Investment

##  Project Overview

This project conducts a comprehensive data analysis of aviation accidents and incidents using the NTSB Aviation Accident Database. The goal is to uncover actionable insights that support safer and more strategic aircraft investment decisions by evaluating risk across aircraft types, operational conditions, and geography.

---

## Business Objectives

1. **Evaluate Aircraft Risk Profiles by Type, Make, and Model**  
   Identify aircraft with higher frequencies of fatal injuries, substantial damage, and serious incidents.

2. **Analyze Contributing Factors to Aircraft Accidents**  
   Explore the relationship between accident severity and operational factors like weather conditions and flight phases.

3. **Assess Geographical and Operational Risk**  
   Determine high-risk regions and flight purposes to better allocate investment and operational focus.

---

## Data Source

- **Dataset**: [NTSB Aviation Accident Database](https://www.ntsb.gov)
- **Records**: 88,889 aviation events from 1962 to 2022
- **Scope**: Civil aviation events involving aircraft within the United States, its territories, and international waters

---

## Data Cleaning & Preparation

- Removed irrelevant and high-null columns (e.g., `Latitude`, `FAR.Description`, `Air.carrier`)
- Standardized categorical values (e.g., `Engine.Type`, `Weather.Condition`, `Purpose.of.flight`)
- Imputed missing values using median (for skewed numerical data) and "Unknown" (for categorical)
- Removed extreme outliers based on 0.005–0.995 quantile range for numerical columns
- Engineered a new `Severity_class` feature to classify injury outcomes into: **Fatal**, **Serious**, **Non-Fatal**, **Incident**

---

##  Key Visualizations

### Objective 1: Aircraft Risk Profiles

- **Top Aircraft with Highest Fatal Injuries**  
- **Aircraft Types with Highest Substantial Damage**  
- **Top Models by Serious/Fatal Incidents**  
- **Boxplot: Fatal Injuries by Aircraft Category**

### Objective 2: Contributing Factors

- **Average Fatal Injuries by Weather Conditions** (`IMC` vs `VMC`)
- **Fatality Distribution by Phase of Flight** (Takeoff, Landing, Cruise, etc.)
- **Stacked Bar: Accident Severity vs Weather**
- **Scatter: Fatal vs Serious Injuries**

### Objective 3: Geographic & Operational Risk

-  **Distribution of Incidents by U.S. State**
- **Distribution of Flight Purposes** (Personal, Instructional, Business, etc.)

---

## Strategic Recommendations

### 1. Avoid High-Risk Aircraft Types
- Cessna and Piper consistently appear in the top 10 aircraft types with the highest total fatal injuries. On the other hand Airbus and Boeing have relatively lower fatality rate and damages
- **Recommendation**: For strategic fleet investment, prioritize high-volume general aviation models like the Boeing and Airbus.

### 2. Limit Operations in High-Risk Conditions
- IMC conditions average ~2.0 fatalities per incident vs. 0.25 in VMC.
- Landing and Takeoff phases are the most dangerous.
- **Recommendation**: Enhance SOPs for poor weather, invest in pilot training, and adopt better avionics.

### 3. Focus on Safer Use Cases and Regions
- Personal and instructional flights have higher incident counts.
- CA, TX, FL show the highest incident rates
- **Recommendation**: Target aircraft usage for commercial, corporate, and ferry purposes; reduce exposure in high-risk states.

---

## Tools & Technologies

- **Python 3.11**
- **Pandas, NumPy** – Data processing
- **Seaborn, Matplotlib** – Visualization
- **Jupyter Notebook** – Interactive analysis
- **Markdown / PDF** – Documentation & presentation


---

## Conclusion

This project provides a structured, data-driven foundation for making smarter, safer aircraft investment decisions. Through historical analysis of accidents, we deliver actionable recommendations that reduce operational risk and support more resilient aviation strategy.

---

## Contact

**Author**: Brian Kiprop Kibor
**Email**: kipropbrian26@gmail.com 
**Location**: Kenya  

