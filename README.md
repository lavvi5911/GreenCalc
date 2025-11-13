GreenCalc: Predictive Analysis of India’s Carbon Footprint Using Machine Learning
⚡ A Machine Learning–powered CO₂ forecasting and environmental analytics system for India.

📌 Overview
GreenCalc is a data-driven carbon footprint forecasting project designed to analyze and predict India’s per-capita CO₂ emissions using advanced Machine Learning and Deep Learning models.
The project utilizes historical environmental, economic, and energy data from Our World in Data (OWID) to generate reliable emissions forecasts for 2024–2030 and evaluate economic–environmental decoupling trends.

GreenCalc also integrates SHAP explainability to interpret model behavior and provides a pathway for extending the system into an interactive Streamlit dashboard.

🌍 Key Features

✔️ Multi-source dataset combining CO₂, energy mix, and macroeconomic indicators
✔️ Cleaned and engineered master dataset (1960–2023)
✔️ ML models: XGBoost (tuned) & LSTM
✔️ Forecasts future CO₂ per capita for 2024–2030
✔️ SHAP-based explainability (global + local feature interpretation)
✔️ Decoupling analysis between GDP and carbon emissions
✔️ Visualization-ready outputs for dashboards and research papers

📂 Dataset Information
📘 Primary Source: Our World in Data (OWID)

CO₂ & Greenhouse Gas Emissions dataset

OWID Energy dataset (electricity generation & energy mix)

📅 Time Range:

1960–2023

🧾 Final Combined Master Dataset Columns:

year

gdp

population

energy_per_gdp

co2_per_capita

coal_co2, oil_co2, gas_co2, cement_co2

flaring_co2, land_use_change_co2

energy_per_capita

co2_per_unit_energy

share_global_co2

share_global_cumulative_co2

temperature_change_from_co2

share_coal_elec, share_gas_elec, share_renewables_elec

co2_per_capita_lag1

⚙️ Technologies Used
Category	Tools
Language	Python
Data Handling	Pandas, NumPy
Visualization	Matplotlib, Seaborn, Plotly
Machine Learning	XGBoost, Scikit-learn
Deep Learning	TensorFlow / Keras
Explainability	SHAP
Dashboard (Optional)	Streamlit
Environment	Google Colab / Jupyter Notebook
🧪 Methodology
1️⃣ Data Preprocessing

Extraction of Indian records from OWID datasets

Handling missing values using interpolation

Feature engineering:

Lag feature (co2_per_capita_lag1)

Electricity mix features

Energy intensity features

Outlier handling & normalization (for LSTM)

2️⃣ Exploratory Data Analysis (EDA)

CO₂ per capita trend (1960–2023)

Correlation heatmaps

GDP vs CO₂ relationship

Electricity mix evolution

COVID-19 dip in emissions (2020 anomaly)

🧩 Explainability (SHAP Analysis)
🔍 Key Findings:

GDP is the strongest predictor of CO₂ emissions.

Fossil fuel consumption (oil & coal) also major contributors.

Renewable share has a small but negative impact on CO₂ levels.

SHAP beeswarm plot shows:

High GDP → increases predicted CO₂

Higher renewables → decreases CO₂

Energy efficiency also reduces CO₂

Outputs saved:

shap_values_india.csv (global SHAP data)

Beeswarm & bar plots (for dashboard/report)

📈 Results Summary
Metric	XGBoost	LSTM
R² Score	0.9967	0.982
MAE	0.131	0.164
RMSE	0.155	0.211
📌 Insights:

XGBoost outperforms LSTM due to small dataset size

2020 dip due to COVID-19 economic slowdown

Emissions show a rising trend but slower than GDP growth

🚀 Future Enhancements

Integrate Transformer-based forecasting (TFT)

Include real-time APIs for live emission updates

Build full-fledged web dashboard with simulation tools

Add emissions from agriculture & transport sectors

Deploy model on Streamlit Cloud / HuggingFace Spaces

👩‍💻 Authors

Lovepreet Singh
B.Tech – Artificial Intelligence & Data Science
Chandigarh Engineering College, Jhanjeri
📧 lovepreettushki@gmail.com

Shweta Chakraborty
B.Tech – Artificial Intelligence & Data Science
Chandigarh Engineering College, Jhanjeri
📧 shwetachakraborty709@gmail.com

Under the Guidance of:
Mr. Adil Hussain
Department of Computer Science & Engineering
Chandigarh Engineering College, Jhanjeri
📧 Adil.4359.@cgc.ac.in
