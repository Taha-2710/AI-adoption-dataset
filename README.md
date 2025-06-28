
# 🧠 Project: Global AI Adoption Data QA & Analysis

## 📌 Project Goal

The goal of this project is to apply **Data Quality Assurance (QA)** techniques on a real-world dataset that captures global trends in **AI tool adoption** across countries, industries, demographics, and company sizes. It aims to demonstrate a hands-on approach to identifying data issues, cleaning them, and preparing data for trustworthy analytics and decision-making.

---

## 📊 Dataset Overview

This dataset contains **145,000 records** with the following columns:

| Column Name           | Description |
|-----------------------|-------------|
| `country`             | Country of observation (e.g., USA, UK, India) |
| `industry`            | Industry sector (e.g., Technology, Manufacturing) |
| `ai_tool`             | AI tool in use (e.g., ChatGPT, Midjourney) |
| `adoption_rate`       | AI adoption rate (%) in the respective category |
| `daily_active_users`  | Number of daily active users for the tool |
| `year`                | Year of record |
| `age_group`           | Age group of users (e.g., 18–24, 35–44) |
| `company_size`        | Size category of the organization (Startup, SME, Enterprise) |

---

## 🧠 Tools & Libraries Used

- `Python`
- `pandas` – for data manipulation
- `matplotlib` & `seaborn` – for visual analysis
- `numpy` – for numerical ops
- `Jupyter Notebook` – for step-by-step EDA & QA

---

## 🧹 Data Cleaning Techniques Applied

| Technique | Description |
|----------|-------------|
| Schema validation | Ensured all columns are of expected data types (e.g., float for adoption_rate) |
| Categorical consistency | Unified values for `industry`, `company_size`, and `age_group` |
| Outlier detection | Identified unusually high/low values using box plots and IQR method |
| Duplicate checks 
| Range validation | Ensured `adoption_rate` is between 0–100 and `year` is valid (e.g., 2018–2024) |
| Null checks | Verified no missing values post-cleaning |

---

## 🔍 Before vs After Cleaning Summary

| Checkpoint              | Before QA             | After QA              |
|-------------------------|-----------------------|------------------------|
| Null values             | Some `adoption_rate` and `company_size` values missing | 0 missing values |
| Categorical typos       | Mixed casing and spacing (e.g., "startUp", " SME ") | Cleaned and standardized |
| Outliers in adoption    | Extreme values >100% or <0% | Corrected or removed |
| Duplicates              | Present (based on country+tool+year) | Removed |
| Inconsistent values     | Age groups with dashes, spaces, or numbers only | Cleaned and grouped properly |

---

## 🚨 Outlier Detection

Outliers were flagged in:

- **`adoption_rate`**: Values exceeding 100% or negative were investigated and removed.
- **`daily_active_users`**: Log transformation and box plots were used to identify extremely large user counts which were likely data entry errors or misclassifications.
- **IQR method**: Used to detect numerical anomalies across numerical columns.

---

## 📁 How to Use This Project

1. Clone the repo:
```bash
git clone https://github.com/your-username/ai-adoption-data-qa.git
cd ai-adoption-data-qa
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch the notebook:
```bash
jupyter notebook ai_qa_analysis.ipynb
```

---

## 🎯 Future Enhancements

- Automate schema validation with **Pandera** or **Great Expectations**
- Build a dashboard for QA rule violation summaries
- Add real-time QA logging pipeline with alerts

---

## 👨‍💻 Author

**Mohd Taha Ahmad**  
_Data Analyst • QA Specialist • AI Adoption Tracker_  
📫 [LinkedIn](https://linkedin.com/in/your-profile) | 🌐 [GitHub](https://github.com/your-username)
