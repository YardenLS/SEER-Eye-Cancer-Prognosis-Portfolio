# **Ocular Oncology Clinical Registry & Survival Analysis**

## **📌 Overview**

This project serves as a professional portfolio demonstration for a Research & Data Coordinator, showcasing advanced data management, data cleaning, and statistical analysis capabilities using SPSS within a clinical and pharmaceutical research context. The repository models a real-world hospital or pharmaceutical oncology registry, focusing on patient outcomes, prognostic factors, and time-to-event survival analysis.

## **🗄️ Dataset Description**

The analysis is based on a structured ocular oncology dataset (eye_cancer_seer_final.csv) containing 5,000 patient-level records. The dataset mirrors authentic hospital registry data (inspired by SEER standards) and encompasses a diverse range of rare eye cancer subtypes, including Retinoblastoma, Uveal Melanoma, Orbital Lymphoma, and Conjunctival Melanoma.

🛠️ Methodology & SPSS Implementation Highlights

## 🧹 Data Cleaning & Preprocessing (Data Management)

To prepare the raw clinical registry dataset (`eye_cancer_seer_final.csv`) for rigorous statistical analysis in SPSS, standard clinical data management procedures were executed:

*   **Identifier Management:** Preserved authentic patient-level alphanumeric identifiers (`Patient_ID` in `PID000xx` format) to maintain healthcare registry integrity and prevent merging errors.
*   **Variable Recoding & Binary Encoding:** Standardized categorical and logical indicators into binary numeric formats (`0`/`1`) to facilitate multivariate modeling (e.g., converting text-based/boolean indicators like *Gender*, *Surgery Status*, and *Family History* into analytical-ready binary variables).
*   **Scale Verification & Structure:** Verified and locked measurement scales (Nominal, Ordinal, and Scale) across all 16 clinical variables, ensuring proper architecture for descriptive statistics and time-to-event survival analysis (`Survival_Time_Months` and `Outcome_Status`).

## 🎯 Research Question & Hypotheses

### Primary Research Question
Is there a statistically significant association between the primary treatment modality (`Treatment_Type`) and the final clinical outcome status (`Outcome_Status`) in patients with ocular cancer?

---

### Statistical Hypotheses

* **Null Hypothesis ($H_0$):** 
  There is **no association** between the treatment type and the clinical outcome status. The outcome distribution is independent of the treatment modality administered.
  $$H_0: \text{Treatment Type} \perp \text{Outcome Status}$$

* **Alternative Hypothesis ($H_1$):** 
  There is a **statistically significant association** between the treatment type and the clinical outcome status. The outcome distribution differs across treatment modalities.
  $$H_1: \text{Treatment Type} \not\perp \text{Outcome Status}$$

### Methodological Note on Statistical Assumptions
Because both target variables (`Treatment_Type` and `Outcome_Status`) are categorical (nominal), normality tests (such as Kolmogorov-Smirnov or Shapiro-Wilk) are **not applicable**. Instead, the evaluation relies on a **Pearson's Chi-Square Test of Independence ($\chi^2$)**, ensuring that expected cell frequencies meet the mandatory threshold ($\ge 5$ in at least 80% of cells).
