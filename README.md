# 📊 Sales Data Cleaning and Visualization — Technographic Data (Italy)

## 🔍 Project Overview
This project involves cleaning, transforming, and visualizing a real-world B2B technographic dataset of companies in Italy. The dataset provides insight into technologies used by businesses, including deployment status, digital tools, and IT infrastructure. The goal is to demonstrate core data analysis skills: preprocessing, feature engineering, visualization, and communication of insights.

---

## 🧾 Dataset Description

- **Source:** [Techsalerator - Kaggle](https://www.kaggle.com/datasets/techsalerator/b2b-technographic-data-in-italy)
- **Rows:** 308 records
- **Fields Include:**
  - `Website Domain`
  - `Ticker`
  - `Technology Name`
  - `Deployment Dates`
  - `Behind Firewall Status`
  - `Technology ID`

---

## 🧹 Cleaning & Preprocessing Steps

- Loaded and explored the dataset with `pandas`
- Handled missing values (`Ticker` column)
- Converted date strings into datetime format
- Engineered new features:
  - `Last_Year`, `Last_Month` from `Last Seen At`
- Exported the cleaned dataset to CSV

---

## 📊 Visualizations

Created using `matplotlib` and `seaborn`:

- 📈 **Technology Appearances Over Time**
- 🏆 **Top 10 Technologies**
- 🔐 **Behind Firewall Usage**
- 📅 **Trend of Top Technology by Month**
- 🧱 **Technology Mentions by Company**

---

## 📁 Project Structure

📂 Technographic-Analysis-Italy/ │ ├── ItalyB2B.py # Main script ├── Cleaned_Technographic_Data_Italy.csv ├── plots/ # (Optional) Exported figures ├── README.md # Project documentation

---

## 💡 Key Insights

- A few companies dominate technology usage (e.g., `infosys.com`)
- Some technologies are used repeatedly across months
- Most technologies are behind firewalls, indicating strong security posture
- Deployment spikes in specific periods suggest targeted implementation windows

---

## 📌 Tools & Libraries

- Python 3.10+
- pandas
- seaborn
- matplotlib
- Jupyter Notebook / Spyder (local environment)

---

## 📬 Author

**Mohammadamin Jahanimajd**, Data Analysis BSc Student  
University of Messina  
*Aspiring Machine Learning Engineer*

---

## 🔗 License

Dataset credit: [Techsalerator via Kaggle]

---

# Technographic Analysis — Italy (Sales / B2B Tech Data)

This project cleans, analyzes and visualizes a B2B technographic dataset for companies in Italy. The goal is to extract insights about technology adoption, behind‑firewall status, and trends over time.

## Files

- `Cleaned_Technographic_Data_Italy.csv` — cleaned dataset (exported)
- `ItalyB2B.py` — main script for cleaning and visualization
- `plots/` — generated visualizations (top technologies, time trends, behind‑firewall distribution)

## Dataset

Source: Techsalerator (Kaggle) — see `README` in the original dataset for licensing details.

## How to run

1. Install required Python packages (pandas, matplotlib, seaborn):

   pip install pandas matplotlib seaborn

2. Run the main script to produce cleaned CSV and plots:

   python ItalyB2B.py

3. Check the `plots/` folder for the exported charts (PNG files).

## Key outputs

- Top 10 technologies used by companies
- Time series of technology mentions
- Distribution of technologies deployed behind firewalls

## Ideas for extension

- Enrich dataset with company attributes (revenue, size) for deeper segmentation
- Interactive dashboard with Plotly Dash or Streamlit
- Automated monthly refresh and reporting pipeline

## Author

Mohammadamin (Amin) Jahanimajd — BSc Data Analysis
