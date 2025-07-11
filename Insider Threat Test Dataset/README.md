# Insider Threat Detection Project

## Project Overview

This project demonstrates a complete, practical data analysis workflow using a real-world insider threat dataset. The primary goal is to detect suspicious insider activities through data exploration, cleaning, and insightful reporting. The project shows how to handle raw logs, process them for analysis, identify anomalies, and build an actionable dashboard.

---

## Project Structure

- `data_raw/`: Original raw CSVs (local only — **too large to include in repo**)
- `data_processed/`: Cleaned, trimmed versions of the raw data
- `jupyter_notebooks/`: All EDA and cleaning notebooks
- `excel_dashboard/`: Final Excel pivot table with suspicious login counts
- `output/`: Example output CSVs for top user logons and activity scores
- `Screenshots/`: Screenshots captured during the project steps

---


The original dataset includes CSVs that exceed **GitHub’s file size limit of 100 MB**:
- `logon.csv` (~290 MB)
- `http.csv` (~290 MB)
- `http_cleaned.csv` (~283 MB)

These files are **NOT included** in this repository to comply with GitHub’s storage rules.

You can download the full raw dataset directly here:  
[https://kilthub.cmu.edu/articles/dataset/Insider_Threat_Test_Dataset/12841247/1](https://kilthub.cmu.edu/articles/dataset/Insider_Threat_Test_Dataset/12841247/1)

If you want to version-control large files yourself, consider using **Git Large File Storage (Git LFS)**.

## Author

Copyright © [BackdoorAli](https://github.com/BackdoorAli)

---

## Dataset

**Source:**  
[Insider Threat Test Dataset - Carnegie Mellon University](https://kilthub.cmu.edu/articles/dataset/Insider_Threat_Test_Dataset/12841247/1)

- Raw logs include: LDAP records, logon events, device logs, and HTTP activity.
- Original data files generated using ExactData Dynamic Data Generator (DDG).
- Usage governed by the ExactData End User Agreement (see LICENSE).

---

## Folder Structure

```
Insider Threat Detection Project/
│
├── data_raw/               # Original raw files
│   └── r1/
│       ├── device.csv
│       ├── http.csv
│       ├── logon.csv
│       ├── LDAP/          # Monthly LDAP files
│
├── data_processed/         # Cleaned, merged outputs
│   ├── ldap_cleaned.csv
│   ├── logon_cleaned.csv
│   ├── device_cleaned.csv
│   └── http_cleaned.csv
│
├── jupyter_notebooks/      # Full exploration and cleaning notebooks
│   ├── 01_data_exploration.ipynb
│   ├── 02_logon_exploration.ipynb
│   ├── 03_device_exploration.ipynb
│   ├── 04_http_exploration.ipynb
│   ├── 05_data_cleaning.ipynb
│   └── 06_eda_dashboard_preparation.ipynb
│
├── output/                 # Sliced callout tables for dashboard
│   ├── logon_counts_per_user.csv
│
├── excel_dashboard/        # Final wireframe dashboard
│   ├── logon_counts_per_user.xlsx
│
├── README.md
└── LICENSE
```

---

## Methodology

**Phase 1: Data Exploration**
- Individual analysis for LDAP, logon, device, and HTTP logs.
- Documented findings for row counts, missing values, timestamp structure, merge keys.

**Phase 2: Data Cleaning**
- Merged multiple monthly LDAP files into a single dataset.
- Parsed timestamps for logon, device, and HTTP logs.
- Dropped corrupted rows, removed duplicates.
- Saved cleaned files for downstream use.

**Phase 3: Insight Generation**
- Identified suspicious logins per user (abnormally high counts).
- Highlighted outliers based on a logical threshold.
- Saved callout table for dashboard reporting.

**Phase 4: Dashboard Wireframe**
- Built a simple executive chart using Apple Numbers:
  - Suspicious Logins chart (Top 12 outliers).
- Chart formatted for clear axis labels, proper sorting, and final export as `.xlsx`.

---

## References & Useful Links

- [Insider Threat Test Dataset](https://kilthub.cmu.edu/articles/dataset/Insider_Threat_Test_Dataset/12841247/1)
- [SEI CERT Division - Carnegie Mellon University](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=541644)
- [ExactData LLC - Dynamic Data Generator (DDG)](http://www.exactdata.net/)


---

## Disclaimers

- This repository is for educational and demonstration purposes only.
- All raw data remains under its original license and usage terms.
- Derivative works may only include minimal excerpts as needed for analysis, in compliance with the End User Agreement.
- Copyright © 2011 ExactData, LLC, All Rights Reserved.

See `LICENSE` for full details.

---