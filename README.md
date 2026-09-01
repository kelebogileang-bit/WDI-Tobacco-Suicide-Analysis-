# WDI-Tobacco-Suicide-Analysis-
Cross-national analysis investigating tobacco prevalence vs suicide mortality 
# Cross-National Analysis: Tobacco Prevalence vs. Suicide Mortality Rates (2015–2025)

## Executive Summary
This project delivers a cross-national empirical analysis investigating whether adult tobacco prevalence (evaluated as a potential behavioral proxy for substance usage and coping mechanisms for psychological distress) shares a directly proportional or linear relationship with national suicide mortality rates.

Utilizing World Development Indicators (WDI) from the World Bank across 265 global entities, raw data was engineered in **Supabase PostgreSQL** and visualized using **Google Looker Studio**.

**Core Analytical Finding:** There is **no direct linear or proportional relationship** between national adult tobacco prevalence and suicide mortality rates at the country level. High-tobacco nations frequently exhibit low suicide mortality rates (e.g., Lebanon, Timor-Leste), demonstrating that single behavioral proxies cannot serve as direct predictors or standalone risk factors for national suicidality.

---

## Data Pipeline & SQL Transformation
Due to system compatibility constraints, **Google Looker Studio** was selected as the cloud BI solution. Raw, wide-format WDI data was unpivoted, standardized, and pre-aggregated in **Supabase PostgreSQL**.

The SQL scripts used for staging and unpivoting are available in the [`/sql/`](./sql/) directory.

## Visual Analytics & Key Outliers

Visual analytics were executed in Looker Studio using an **Inner Join** data blend (`Tobacco_vs_Suicide_Blend`) on `country_name` to isolate entities with concurrent data for both primary indicators (`SH.PRV.SMOK` and `SH.STA.SUIC.P5`).

* **Absence of Proportionality:** A dual-axis combo chart revealed that as suicide rates decrease monotonically across ranked countries, adult tobacco prevalence fluctuates erratically.
* **Empirical Outliers Highlighted:**
* **Lebanon:** Tobacco Prevalence = **44.94%** | Suicide Mortality Rate = **0.74 per 100k**
* **Timor-Leste:** Tobacco Prevalence = **48.52%** | Suicide Mortality Rate = **3.56 per 100k**
* **Bulgaria:** Tobacco Prevalence = **39.28%** | Suicide Mortality Rate = **9.76 per 100k**

---

## Deliverables & Links

* **Analytical Report (PDF):** Available in [`/deliverables/`](./deliverables/)
* **Interactive Cloud Dashboard:** [View Live Looker Studio Dashboard]([https://datastudio.google.com/reporting/8216fdf2-85f2-4aed-b7a4-a4a426e25e0b])
* **Demo Presentation Video:** [Watch Video Presentation](https://drive.google.com/file/d/1fTj4FDT77FRtdH0Ws3a2KHsE8S8WO4s-/view?usp=drive_link)
