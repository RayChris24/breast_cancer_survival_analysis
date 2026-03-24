# Breast Cancer Survival Analysis: Clinical Risk Factor Modeling

## 📌 Project Overview
This repository contains an end-to-end survival analysis workflow using the **German Breast Cancer Study Group (GBSG2)** clinical dataset. The objective of this project is to apply time-to-event modeling techniques to identify key clinical predictors of patient survival and quantify the effectiveness of treatments like Hormone Therapy. 

By translating raw clinical data into predictive statistical metrics, this analysis provides a framework for risk-based patient stratification and data-driven healthcare decision-making.

## 🚀 Key Insights & Results
* **Treatment Efficacy:** Hormone Therapy was identified as a highly significant protective factor. Patients receiving this treatment saw a **29% reduction in the hazard of death** (HR = 0.71).
* **Survival Benchmark:** Kaplan-Meier estimation established a cohort **median survival time of 1,807 days** (approximately 4.9 years).
* **High-Risk Indicators:** Advanced tumor grades (Grade III) more than double the hazard risk (HR = 2.18) compared to baseline, while each standardized unit increase in positive lymph nodes increases risk by 31%.
* **Model Accuracy:** The final multivariate Cox Proportional Hazards model achieved a strong **Concordance Index of 0.69**.
* **Statistical Rigor:** The model passed all Schoenfeld residual tests, confirming the Proportional Hazards assumption was strictly met for all variables.

## 📂 Repository Structure
* `survival_analysis_breast_cancer.ipynb`: The main Jupyter Notebook containing the full analysis, visualizations, and statistical modeling.
* `requirements.txt`: The list of Python dependencies required to run the notebook locally.
* `README.md`: Project documentation and summary of findings.

## 🛠️ Installation & Usage
To keep the notebook clean and professional, library installations are handled externally. To run this project on your local machine, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install required dependencies:**
   Use the included requirements file to install the necessary packages.
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the notebook:**
   Open the `survival_analysis_breast_cancer.ipynb` file in Jupyter Notebook, JupyterLab, or your preferred IDE.

## 🔬 Methodology
1. **Data Preprocessing:** Handled continuous clinical variables using `StandardScaler` and applied One-Hot Encoding for categorical features (avoiding the dummy variable trap). Transformed the censoring indicator into a clear "Event" format.
2. **Exploratory Data Analysis (EDA):** Visualized distributions of age, tumor size, and lymph node involvement, alongside a correlation matrix to check for multicollinearity.
3. **Kaplan-Meier Estimation:** Plotted baseline survival curves and compared treatment versus control groups to visually establish the prognostic advantage of Hormone Therapy.
4. **Cox Proportional Hazards:** Built a multivariate regression model to calculate Hazard Ratios for all clinical predictors.
5. **Assumption Validation:** Evaluated Schoenfeld residuals to guarantee the statistical integrity of the model's coefficients.
