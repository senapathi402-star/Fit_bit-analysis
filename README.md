# 🏃 Fitbit Analysis — Exploratory Data Analysis

> **Tools Used:** Python | NumPy
> **Dataset:** 96 Days of Fitness Tracking | Oct 2017 – Jan 2018

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/senapathi402-star/Fit_bit-analysis/blob/main/Fit_Bit_Analysis.ipynb)

---

## 📌 Objective

Analyze Fitbit fitness tracker data to identify relationships between **sleep hours, step count, mood, and activity status** — uncovering patterns that determine what makes a person active, happy, and healthy.

---

## 🗃️ Dataset Structure

| Column | Type | Description |
|--------|------|-------------|
| `date` | string | Date of tracking (DD-MM-YYYY) |
| `step_count` | int | Total steps walked |
| `mood` | string | Happy / Neutral / Sad |
| `calories_burned` | int | Calories burned |
| `hours_of_sleep` | int | Hours of sleep |
| `activity_status` | string | Active / Inactive |

- **96 rows × 6 columns**
- Date range: **06-Oct-2017 to 09-Jan-2018**

---

## 🔍 Key Insights

### 😴 Sleep vs Mood & Activity

| Mood | Activity | Avg Sleep Hours |
|---|---|---|
| 😊 Happy | Active | **6.0 hrs** |
| 😊 Happy | Inactive | 5.3 hrs |
| 😐 Neutral | Active | 4.7 hrs |
| 😐 Neutral | Inactive | 4.6 hrs |
| 😔 Sad | Active | 4.75 hrs |
| 😔 Sad | Inactive | 4.75 hrs |

> **Insight:** Sleeping 6+ hours keeps a person both active and happy.

---

### 👟 Step Count vs Mood & Activity

| Mood | Activity | Avg Steps |
|---|---|---|
| 😊 Happy | Active | **3,180 steps** |
| 😊 Happy | Inactive | 2,854 steps |
| 😐 Neutral | Active | 3,159 steps |
| 😐 Neutral | Inactive | 2,940 steps |
| 😔 Sad | Active | 2,750 steps |
| 😔 Sad | Inactive | **1,949 steps** |

> **Insight:** Walking 3,000+ steps per day is strongly linked to a happy and active lifestyle.

---

### 📊 Mood Distribution by Step Count

| Step Count | Happy | Neutral | Sad |
|---|---|---|---|
| More than 3,000 steps | 24 days | 14 days | 10 days |
| Less than 2,000 steps | 13 days | 8 days | 18 days |

> When step count > 3,000 → **Happy on 50% of days**
> When step count < 2,000 → **Sad on 46% of days**

---

## 📋 Summary

- Users who slept **6+ hours** and walked **3,000+ steps** → mood was **Happy & Active**
- Users who slept **4–6 hours** and walked **2,000–3,000 steps** → mood was **Neutral or Happy**, possibly Active or Inactive
- Users who slept **less than 4 hours** and walked **less than 2,000 steps** → mood was **Sad**

---

## 💡 Suggestions

For a healthier, stress-free life:
- Sleep at least **8 hours** per night
- Walk a minimum of **5,000 steps** per day
- Maintain a healthy diet

These three habits combined will help keep a person happy, active, and energetic throughout the day.

---

## 🛠️ Python Concepts Used

- `numpy` — loading `.txt` data, array operations
- `data.T` — transposing array to separate columns by variable
- `.astype('int')` — converting string columns to integer for calculations
- **Boolean indexing** — `step_count[mood == 'Happy']`
- **Compound conditions** — `(mood == 'Happy') & (activity_status == 'Active')`
- `np.mean()` — calculating average sleep and step counts per group
- `np.unique()` — counting mood frequency at different step thresholds

---

## 📁 Files in this Repository

| File | Description |
|------|-------------|
| `Fit_Bit_Analysis.ipynb` | Jupyter Notebook with full EDA |
| `fit.txt` | Raw Fitbit tracking data |
| `README.md` | Project documentation |

---

## ▶️ How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install numpy
   ```
3. Open `Fit_Bit_Analysis.ipynb` in Jupyter Notebook or Google Colab
4. Run all cells from top to bottom

---

## 👤 Author

**Senapathi Krishna Sai**
Data Analyst | SQL | Python | Tableau | Excel

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/senapathi-krishna-sai-a54721388)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/senapathi402-star)
