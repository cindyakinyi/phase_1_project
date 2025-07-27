
# ✈️ Aviation Safety Analysis Project

## 📌 Project Overview

This project analyzes aircraft accident data to identify patterns in aviation safety, determine high-risk models, and highlight the safest aircraft types. The dataset originates from the \[FAA (Federal Aviation Administration)] and covers key attributes such as injury severity, weather conditions, aircraft make/model, and flight phase.

---

## 🧰 Tools & Technologies

* **Python (Pandas, Matplotlib, Seaborn)**: For data cleaning and visualization.
* **Jupyter Notebook**: Environment for exploration and analysis.
* **Git & GitHub**: Version control and project sharing.
* **Tableau**: For interactive dashboards and data storytelling.

---

## 🧼 1. Data Cleaning Steps

* Dropped irrelevant columns like coordinates, registration, and airport info.
* Removed rows with missing key fields (e.g., `Event.Date`, `Make`, `Model`, `Aircraft.damage`).
* Converted `Event.Date` to datetime.
* Handled missing injury data by filling with `0`.
* Standardized column naming (Title Case with underscores).
* Removed duplicate accident records based on `Accident.Number`.

---

## 🔍 2. Handling Missing Values

* Replaced unknown weather conditions (e.g. `UNK`, `Unk`) with `'Unknown'`.
* Filled:

  * `Number.Of.Engines` using the mode.
  * `Purpose.Of.Flight` and `Broad.Phase.Of.Flight` with `'Unknown'`.
* Dropped rows missing key location and severity fields:

  * `Location`, `Country`, `Injury.Severity`, `Amateur.Built`.

---

## 🛠️ 3. Feature Engineering

* Extracted `Year` from `Event.Date`.
* Created a combined column `Total.Injuries` from fatal, serious, and minor injuries.
* Engineered an `Injury.Category` column with the following logic:

  * **Fatal > Serious > Minor > No Injuries**.
* Constructed:

  * `Make_Model` by combining `Make` and `Model`.
  * `Model_Group` by extracting numeric part of `Model` (e.g. "737" from "737-800").
  * `Make_Model_Grouped` by combining `Make` with `Model_Group`, which helps consolidate model variants.

---

## 📊 4. Visual Insights

* **Injury Severity by Flight Phase**:

  > Bar chart showing which phases of flight (e.g., landing, takeoff) have the most injuries.

* **Most Common Aircraft in Accidents**:

  > Top 10 aircraft types by number of accident reports.

* **Most Dangerous Aircraft**:

  > Aircraft models ranked by total fatal injuries.

* **Safest Aircraft**:

  > Models with the highest number of uninjured passengers.

---

## 📁 Project Structure

```bash
phase_1_project/
│
├── Aviation_Data.csv
├── cleaned_aviation_data.csv
├── student.ipynb
├── README.md
├── Aviation_Safety_Presentation.pptx
├── presentation.pdf
├── github.pdf
└── final tableau project phase 1.twb
```

---

##  Outcome

## Summary of Findings
* After analyzing the aviation accident data, several key insights emerged:

* Most accidents occurred during the landing and takeoff phases, highlighting the critical nature of these moments in flight.

* Aircraft types such as Boeing 737 and Cessna 172 appeared most frequently in accident reports, likely due to their widespread use.

* Fatal injuries were most commonly associated with certain variants of McDonnell Douglas and Piper aircraft, suggesting higher risk in those models.

* The safest aircraft models (by number of uninjured passengers) included some variants of Boeing, Airbus, and Beechcraft, which consistently reported high survivability rates.

* Weather conditions and flight purpose also played a notable role in accident severity, with personal or instructional flights being more vulnerable.

## Recommendations
* For airline companies or buyers:
Prioritize aircraft models with strong safety records (e.g., high "Total Uninjured" counts) and consistent performance across different flight phases.

* For pilots and aviation trainers:
Extra emphasis should be placed on training during takeoff and landing phases, as these are statistically the most accident-prone.

* For aviation authorities:
Enhanced regulations or monitoring may be needed for aircraft types or purposes of flight (like recreational or experimental aircraft) that show higher fatality rates.


---

## 👤 Author

**Cindy Akinyi**
*Data Analyst Enthusiast*
GitHub: [@cindyakinyi](https://github.com/cindyakinyi)

