# **Ocular Oncology Clinical Registry & Survival Analysis**

## **📌 Overview**

This project serves as a professional portfolio demonstration for a Research & Data Coordinator, showcasing advanced data management, data cleaning, and statistical analysis capabilities using SPSS within a clinical and pharmaceutical research context. The repository models a real-world hospital or pharmaceutical oncology registry, focusing on patient outcomes, prognostic factors, and time-to-event survival analysis.

## **🗄️ Dataset Description**

The analysis is based on a structured ocular oncology dataset (eye_cancer_seer_final.csv) containing 5,000 patient-level records. The dataset mirrors authentic hospital registry data (inspired by SEER standards) and encompasses a diverse range of rare eye cancer subtypes, including Retinoblastoma, Uveal Melanoma, Orbital Lymphoma, and Conjunctival Melanoma.

🛠️ Methodology & SPSS Implementation Highlights

## 🧹 Data Cleaning & Preprocessing (Data Management)

To prepare the raw clinical registry dataset (`eye_cancer_seer_final.csv`) for rigorous statistical analysis in SPSS, standard clinical data management and cleaning procedures were executed:

*   **Identifier Management:** Preserved authentic patient-level alphanumeric identifiers (`Patient_ID` in `PID000xx` format) to maintain standard healthcare registry integrity and prevent merging errors.
*   **Variable Recoding & Binary Encoding:** 
    *   **Gender:** Recoded categorical gender values into binary numerical format (`0` = Male, `1` = Female) to facilitate multivariate regression modeling.
    *   **Surgery Status:** Converted logical boolean indicators (`True`/`False`) into binary indicator variables (`0` = No Surgery, `1` = Surgery Performed).
    *   **Family History:** Standardized family history indicators into binary numeric format (`0` = No Family History, `1` = Positive Family History).
*   **Clinical & Outcome Structuring:** Verified measurement scales (Nominal, Ordinal, and Scale) across all variables, ensuring proper data types for descriptive statistics, subgroup comparisons, and time-to-event survival analysis (`Survival_Time_Months` and `Outcome_Status`).
