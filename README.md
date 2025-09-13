# 🏥 Healthcare Readmission & Mortality

## Project Overview

This project analyzes **hospital readmission and mortality rates** across different healthcare providers in the United States.
The goal is to create an **interactive Power BI dashboard** that provides insights into hospital performance, patient outcomes, and geographic trends in healthcare quality.

---

## 📊 Dataset Description

The dataset includes hospital-level performance metrics from Medicare on readmissions and mortality.

**Key Columns:**

* **Hospital Information:** `Provider ID`, `Hospital Name`, `Address`, `City`, `State`, `ZIP Code`, `County Name`, `Phone Number`
* **Measure Details:** `Measure Name`, `Measure ID`, `Measure Type` (Readmission / Mortality)
* **Performance Indicators:** `Score`, `Lower Estimate`, `Higher Estimate`, `Compared to National`, `Performance`
* **Dates:** `Measure Start Date`, `Measure End Date`, `Measure Duration`
* **Geographic Info:** `Latitude`, `Longitude`

---

## 🎯 Objectives

1. Analyze **readmission and mortality rates** across hospitals.
2. Compare hospital performance **against national benchmarks**.
3. Visualize **trends over time** (2012–2015).
4. Identify **top and bottom-performing hospitals**.
5. Enable **geographic insights** using hospital location data.

---

## 🛠️ Tools & Technologies

* **Data Cleaning & Processing:** Python (pandas, numpy)
* **Data Visualization:** Power BI
* **Dashboard Design:** Power BI Service / Desktop

---

##  KPIs (Key Performance Indicators)

* 📌 **Average Readmission Rate (%)**
* 📌 **Average Mortality Rate (%)**
* 📌 **Total Hospitals Analyzed**
* 📌 **Hospitals Worse than National Benchmark**
* 📌 **Trend of Hospital Performance (2012–2015)**

---

## 📈 Dashboard Features

1. **Overview Page**

   * KPI cards (Avg Readmission, Avg Mortality, Total Hospitals, Benchmark Comparison)
   * Year filter (2012–2015)

2. **Performance Trends**

   * Line/Area chart showing readmission & mortality trends over time
   * Drill-down by Measure Type (Readmission vs Mortality)

3. **Geographic Insights**

   * Map visualization of hospitals by state/county
   * Performance color-coded (Better, Same, Worse than National)

4. **Hospital Comparison**

   * Table/Matrix with filters for hospital name, measure type, and state
   * Conditional formatting for high vs low scores

---

## Implementation Steps

1. **Data Cleaning (Python)**

   * Removed duplicates, handled missing values, standardized dates.
   * Saved cleaned file: `cleaned_healthcare_data.csv`.

2. **Data Import (Power BI)**

   * Imported `cleaned_healthcare_data.csv`.
   * Created **Date Table** for time intelligence.

3. **DAX Calculations**

   * `Avg Readmission Rate = AVERAGE(cleaned_healthcare_data[Score])`
   * `Avg Mortality Rate = CALCULATE(AVERAGE(cleaned_healthcare_data[Score]), FILTER(cleaned_healthcare_data, cleaned_healthcare_data[Measure_Type] = "Mortality"))`
   * `Total Hospitals = DISTINCTCOUNT(cleaned_healthcare_data[Hospital Name])`

4. **Dashboard Design**

   * Built pages for **Overview**, **Trends**, **Geography**, **Comparison**.
   * Added slicers for Year, State, Measure Type.
---

## 📊 Dashboard Preview
  * <img width="1351" height="733" alt="Healthcare Readmission   Mortality" src="https://github.com/user-attachments/assets/878cb6e1-14bc-460a-b362-77d35eb4465e" /> *

