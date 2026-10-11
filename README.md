# ADGM Tokenized RWA Liquidity Engine & Terminal

An institutional-grade **Power BI Crypto-Liquidity Terminal** designed for tracking tokenized Real World Assets (RWA) within the **Abu Dhabi Global Market (ADGM)** regulatory framework.

![Power BI](https://img.shields.io/badge/Power_BI-F2C94C?style=for-the-badge&logo=powerbi&logoColor=black)
![ADGM Compliance](https://img.shields.io/badge/ADGM_FSRA-Aligned-003366?style=for-the-badge)
![Data Model](https://img.shields.io/badge/Star_Schema-DAX-blue?style=for-the-badge)

---

## Executive Summary & Dashboard Preview
<img width="1177" height="663" alt="Screenshot 2026-10-11 at 3 14 39 PM" src="https://github.com/user-attachments/assets/2a4c5bd1-362b-4edd-8c67-12141036265f" />


This terminal monitors **secondary market liquidity**, **FSRA investor compliance**, **SPV asset valuations**, and **net rental yield distributions** across $196M USD (~719.9M AED) of tokenized real estate assets in Abu Dhabi.

---

## Key Metrics (KPI Stack)
- **Total Value Locked (TVL):** AED 719.92M ($196.03M USD)
- **Total Net Yield Distributed:** AED 35.54M ($9.68M USD)
- **Target Annual Yield (Avg):** 8.27%
- **KYC Verification Rate:** 86.00% (43 / 50 Verified)
- **Avg Secondary Trading Slippage:** -0.02%

---

## Data Architecture & Star Schema
The project relies on an optimized Star Schema data model:
- `Dim_SPV_Asset`: Asset-level metadata, valuations, target yields, and location tiers across Abu Dhabi (Al Maryah Island, Yas Island, Reem Island, Saadiyat Island, Al Raha Beach).
- `Dim_Investor`: FSRA investor categories (Institutional, Professional, Retail), KYC status, and maximum allowed tickets.
- `Fact_Secondary_Trades`: Automated Liquidity Pool and OTC trading logs, trade execution prices, volumes, and slippage.
- `Fact_Yield_Distributions`: Gross rental income, management fees, and net yield payouts.

---

## Tech Stack & Calculations
- **BI Platform:** Power BI Desktop / Power BI Service (Dark Terminal UI theme `#0B1329`)
- **Data Modeling:** DAX measures, Star Schema modeling, automated currency conversion (1 USD = 3.6725 AED)
- **Visualizations:** Funnel chart (Liquidity Depth), Scatter plot (Yield vs KYC), Custom Azure Map, Donut charts.
  ---

---

## Disclaimer
This repository and its accompanying Power BI dashboard (`ADGM_Tokenized_RWA_Project.pbix`) are strictly built for **academic, educational, and portfolio demonstration purposes**. 

- **Data Origin:** All raw CSV datasets (`Dim_Investor`, `Dim_SPV_Asset`, `Fact_Secondary_Trades`, `Fact_Yield_Distributions`) were **synthetically AI-generated / simulated** to model real-world institutional tokenization workflows without disclosing sensitive data.
- All property names, SPV registry numbers, token quantities, transaction logs, investor names, and yield values contained within the dataset files are **entirely fictional**.
- This project is **not** affiliated with, endorsed by, or representing the Abu Dhabi Global Market (ADGM), Financial Services Regulatory Authority (FSRA), or any of their registered entities.
