# 🌍 Exploratory Data Analysis on Global Terrorism

An end-to-end **Exploratory Data Analysis (EDA)** project on the **Global Terrorism Database**, uncovering patterns in terrorist incidents worldwide from **1970 to 2020** — including trends over time, geographic hotspots, attack methods, target types, responsible organizations, and casualty statistics.

---

## 📌 Project Overview

Terrorism is a global security challenge that affects nations, economies, and communities. This project performs a structured EDA on the Global Terrorism Database (GTD) — a dataset with **more than 200,000 records and 130 columns** — to extract meaningful, data-driven insights into how terrorism has evolved across time, geography, and methodology.

The analysis is performed end-to-end in Python: from raw data ingestion and cleaning, to visualization and insight generation.

---

## 🎯 Objectives

- Clean and preprocess a large, real-world, messy dataset (200K+ rows, 130 columns).
- Identify **year-over-year trends** in global terrorist activity.
- Discover **geographic hotspots** — countries and regions most affected.
- Analyze **attack types**, **weapon types**, and **target categories**.
- Identify the **most active terrorist organizations**.
- Compare **casualties (killed vs. wounded)** over time and across countries.
- Derive actionable insights useful for security, policy, and research purposes.

---

## 🗂️ Dataset

- **Source:** [Global Terrorism Database (GTD)](https://www.start.umd.edu/gtd/) — maintained by the National Consortium for the Study of Terrorism and Responses to Terrorism (START), University of Maryland.
- **Original size:** 200,000+ rows × 130 columns
- **Time span:** 1970 – 2020
- **Format:** Excel (`.xlsx`)

### Key Columns Used After Cleaning

| Column | Description |
|---|---|
| `eventid` | Unique identifier for each recorded incident |
| `Year` / `Month` / `Day` | Date of the event |
| `Country` / `Region` / `State` / `City` | Location of the incident |
| `Latitude` / `Longitude` | Geographic coordinates |
| `Attack_Type` | Method used in the attack (bombing, armed assault, etc.) |
| `Target_Type` | Category of target (civilians, military, government, etc.) |
| `Terrorist_Group` | Organization responsible for the attack |
| `Weapon_Type` | Type of weapon used |
| `Killed` / `Wounded` | Casualty counts |
| `Casualties` | Engineered column: `Killed + Wounded` |
| `Success` | Whether the attack was successfully carried out |
| `Summary` | Brief textual description of the event |

> ⚠️ **Note:** The raw dataset is not included in this repository due to its size and licensing terms. Download it directly from the [official GTD website](https://www.start.umd.edu/gtd/contact/) and place it in the `data/` folder before running the notebook.

---

## 🛠️ Tools & Libraries

- **Python 3**
- **Pandas** – data manipulation and cleaning
- **NumPy** – numerical operations
- **Matplotlib** – static visualizations
- **Seaborn** – statistical visualizations
- **Jupyter Notebook** – interactive analysis environment

---

## 📁 Project Structure

```
EDA-Global-Terrorism/
│
├── data/
│   └── globalterrorismdb.xlsx        # (not included — download separately)
│
├── EDA_project_on_GlobalTerrorism.ipynb   # Main analysis notebook
├── README.md                          # Project documentation
└── requirements.txt                   # Python dependencies
```

---

## 🔍 Project Workflow

1. **Import Libraries** – Load pandas, numpy, matplotlib, and seaborn.
2. **Import Dataset** – Read the raw GTD Excel file into a DataFrame.
3. **Data Cleaning**
   - Select 17 relevant columns out of 130.
   - Rename columns to human-readable names.
   - Handle missing values (fill casualty counts with 0, fill missing location/text fields with `"Unknown"`, impute missing coordinates using country-wise mean).
   - Engineer a new `Casualties` column (`Killed + Wounded`).
   - Remove duplicate records.
   - Standardize text fields (trim whitespace, uppercase).
4. **Basic Information** – Inspect structure, data types, and summary statistics.
5. **Accurate Insights** – Compute headline statistics (total incidents, year range, countries, regions, total casualties, etc.).
6. **Data Visualization** – Answer key analytical questions using charts (see below).
7. **Insight Generation** – Summarize key findings and real-world applications.

---

## 📊 Key Analytical Questions Explored

1. What is the year-over-year trend of global terrorist incidents?
2. Where is the highest concentration of global attacks occurring?
3. How are different attack methods distributed?
4. What types of targets are most commonly chosen?
5. Which organizations are responsible for the highest number of incidents?
6. How do the numbers of killed vs. wounded compare over time?
7. Which countries are the most affected in terms of total casualties?
8. How are terrorist attacks distributed across different regions?
9. How does the distribution of attack types vary across regions?

---

## 💡 Key Insights

- Terrorist activity rose sharply after **2004**, peaking around **2014**.
- **Iraq, Afghanistan, and Pakistan** are the most heavily affected countries; **India** also ranks in the top group.
- **Bombings/explosions** are the dominant attack method (~47% of all incidents) — roughly double the rate of armed assaults (~24%).
- **Civilians** are the most frequently targeted group, followed by **police and military**; government and business targets are attacked at similar rates.
- The **Taliban** and **ISIL** are responsible for the highest number of recorded incidents.
- Between 1970–2020, terrorism caused approximately **479,000+ deaths** and **585,000+ injuries** worldwide, with a sharp spike in wounded victims around 2001.
- **Iraq** alone accounts for over **80,000 casualties**, the highest of any country.
- The **Middle East and South Asia** together account for more than half of all global incidents, while **Western Europe and North America** experience comparatively few.
- Across nearly all regions, **bombings/explosives** remain the leading attack type, followed by armed assault.

### Broader Takeaways
- Global terrorism has grown significantly over the past two decades, underscoring the need for stronger international cooperation.
- A relatively small number of countries and regions bear a disproportionate share of global violence.
- Targeting civilians is largely a psychological strategy, aimed at instilling fear in everyday life.

---

## 🌐 Applications of This Analysis

This dataset and analysis are relevant to:

- Government & National Security agencies
- Intelligence & Defense organizations
- Aviation & Transportation industry (risk assessment)
- Insurance sector (risk modeling)
- International organizations (UN, NGOs)
- Academic & policy research
- Corporate risk & business continuity planning
- Media & journalism

---

## 🚀 How to Run This Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/EDA-Global-Terrorism.git
   cd EDA-Global-Terrorism
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Add the dataset**
   - Download the GTD dataset from the [official source](https://www.start.umd.edu/gtd/contact/).
   - Place the file inside the `data/` folder.
   - Update the file path in the notebook if needed.

5. **Run the notebook**
   ```bash
   jupyter notebook EDA_project_on_GlobalTerrorism.ipynb
   ```

---

## 📦 requirements.txt

```
pandas
numpy
matplotlib
seaborn
openpyxl
jupyter
```

---

## 🙋 Author

Created as part of a Data Science / EDA portfolio project.
Feel free to fork, star ⭐, and contribute!

---
