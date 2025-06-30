# Aircraft Safety Intelligence: A Data-Driven Risk Analysis for Strategic Fleet Investment

## Project Overview

This project analyzes historical aviation accident data from the National Transportation Safety Board (NTSB) to help a U.S.-based aviation investment firm identify low-risk aircraft for commercial and private use. The objective is to support data-driven decision-making on aircraft acquisition, operational focus, and safety strategy across domestic and international markets.

---

## Business Objectives

1. **Evaluate Aircraft Risk Profiles by Type, Make, and Model**  
   Identify aircraft associated with higher fatal injuries, substantial damage, or serious incidents to avoid in new investments.

2. **Analyze Contributing Factors to Aircraft Accidents**  
   Understand how conditions like weather, flight phase, and operational purpose influence incident severity.

3. **Assess Geographical and Operational Risk**  
   Identify high-risk states and use cases to inform safer deployment zones and flight purposes.

---

## Data Source

- **Dataset**: [NTSB Aviation Accident Database](https://www.ntsb.gov)
- **Records**: 88,889 aviation events
- **Period**: 1962 to 2022
- **Scope**: Civil aviation accidents in the U.S., territories, and international waters

---

## Data Cleaning & Preparation

- Dropped high-null columns (e.g., `Latitude`, `Longitude`, `Schedule`, `FAR.Description`)
- Standardized categorical fields such as `Engine.Type`, `Weather.Condition`, and `Purpose.of.flight`
- Imputed missing values using median (for numerical data) or `"Unknown"` (for categorical)
- Created a custom `Severity_class` to categorize incidents: **Fatal**, **Serious**, **Non-Fatal**, and **Incident**
- Retained outliers, as filtering removed over 50% of critical data—especially in skewed columns like fatal and serious injuries

---

## Key Visualizations

### Objective 1: Aircraft Risk Profiles
- Top aircraft makes by total fatal injuries and substantial damage
- Boxplot of fatal injuries by aircraft category
![Aircraft Incidents](../images/aircraft_incidents.png)

### Objective 2: Contributing Factors
- Bar chart: Average fatal injuries in IMC vs. VMC conditions
- Fatal injuries by phase of flight: Takeoff, Climb, Cruise, Approach
- Stacked bar: Injury severity across weather types
![Weather Conditions](../images/weather_conditions.png)

### Objective 3: Geographic & Operational Risk
- Incidents by U.S. state (e.g., CA, TX, FL lead in frequency)
- Average fatal injuries by flight purpose (e.g., Skydiving, Executive, Firefighting)
![Purpose of Flight](../images/purpose_of_flight.png)

---


## Tools & Technologies

- **Python 3.11**
- **Pandas, NumPy** – Data processing
- **Seaborn, Matplotlib** – Visualization
- **Jupyter Notebook** – Interactive analysis
- **Tableau** – Interactive dashboard development
- **Markdown, PDF, PowerPoint** – Reporting and presentation

---
## Strategic Recommendations

### 1. Avoid High-Risk Aircraft Types
- Cessna, Piper, and Boeing aircraft account for over 50% of all incidents.
- General aviation models like the Cessna 172 and PA-28 frequently appear in fatality charts.
- **Recommendation**: Avoid these makes for new fleet acquisitions; adopt Airbus for lower risk and modern safety standards.

### 2. Limit Operations in High-Risk Conditions
- IMC (Instrument Meteorological Conditions) lead to 8× more fatalities than VMC.
- High-risk phases include Climb, Cruise, Maneuvering, and Approach.
- **Recommendation**: Choose aircraft with advanced avionics; implement weather-specific crew training and stricter Go/No-Go SOPs.

### 3. Focus on Safer Use Cases and Regions
- Skydiving, Executive, Firefighting, and Air Drop flights show the highest fatal injury rates.
- California, Texas, and Florida report the most incidents nationally.
- **Recommendation**: Prioritize Airbus usage in **commercial, corporate, and public** operations while limiting deployment in high-risk geographies.
---

## Conclusion

This analysis delivers data-backed recommendations for safer aircraft investment. By examining 60 years of aviation incidents, we identify Airbus as the safest manufacturer for commercial use and recommend strategic deployment based on operational, weather, and geographic risk patterns. These insights offer a clear roadmap for launching a safety-focused aviation division.

---

## Contact

**Author**: Brian Kiprop Kibor  
**Email**: kipropbrian26@gmail.com  
**Location**: Nairobi Kenya  
