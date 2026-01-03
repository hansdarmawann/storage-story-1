# Exploratory Data Analysis of Personal Media Storage Metadata

**Google Data Analytics Capstone Case Study**

**Author:** Hans Darmawan
**Tools:** Python (pandas, numpy, matplotlib, seaborn)
**Framework:** Ask • Prepare • Process • Analyze • Share • Act
**Analysis Type:** Exploratory Data Analysis (EDA)

---

## Project Overview

This project analyzes **personal media storage metadata** derived from multiple hard disks used to archive photography and videography files. Over time, increasing shooting frequency and file sizes have resulted in rapid storage growth, making storage planning and file management more complex.

Using the **Google Data Analytics Capstone framework**, this case study applies exploratory data analysis (EDA) to understand **how storage is consumed**, **which file types contribute most to usage**, and **how shooting behavior changes over time**.

The analysis is **descriptive and insight-driven**, with no predictive modeling.

---

## Business Task

The primary business task is:

> **How is media storage being consumed over time, and what patterns in file type, size, and shooting frequency explain the growth in storage usage?**

This analysis aims to support:

* Better storage planning
* Improved archive organization
* Data-informed decisions about future storage needs

---

## Stakeholders

* The content creator (photographer / videographer)
* Anyone managing large personal media archives
* Data analysts reviewing EDA case studies

---

## Dataset Description

The dataset consists of **anonymized file-level metadata** extracted from personal media archives.
To prevent data leakage and privacy issues, all identifiers and filenames have been masked.

### Columns Included

* **storage_id**
  Identifier representing a physical storage device (hard disk)

* **album_id**
  Identifier representing a folder or album within a storage device

* **file_name**
  Masked filename (sequential, non-identifiable)

* **file_extension**
  File type (e.g., JPG, MP4, MOV, RAW)

* **file_size_bytes**
  File size in bytes

* **file_date**
  File date truncated to year–month–day (hours, minutes, seconds removed)

The dataset was intentionally limited to date granularity at the day level to reduce sensitivity while preserving analytical value .

---

## Analysis Framework

This project follows the **six phases of the Google Data Analytics process**.

---

## 1. Ask

### Business Questions

* Which file types contribute the most to total storage usage?
* Does shooting frequency correlate with storage growth?
* How does storage usage change over time (yearly, monthly)?
* Are weekends or weekdays associated with higher shooting activity?
* Do fewer large RAW/video files outweigh many small JPEG files?

### Success Criteria

* Clear understanding of storage composition
* Evidence-based insights into shooting and storage behavior
* Actionable recommendations for archive management

---

## 2. Prepare

* Loaded metadata from CSV format
* Inspected schema, row counts, and data types
* Verified anonymization and scope limitations
* Assessed missing values and data consistency

A column-level data dictionary and completeness check are included in the notebook.

---

## 3. Process

* Preserved original data wherever possible
* Standardized date fields to support temporal analysis
* Ensured numeric fields (file size) were correctly typed
* Created derived fields where necessary (e.g., year, month, weekday)

All processing steps are documented for transparency.

---

## 4. Analyze

The EDA focuses on:

* **Univariate analysis**

  * Distribution of file sizes
  * Frequency of file extensions

* **Bivariate analysis**

  * File type vs total storage contribution
  * Time vs storage growth

* **Temporal analysis**

  * Yearly and monthly shooting trends
  * Weekday vs weekend shooting behavior

This phase directly addresses whether **many small files** or **few large files** dominate storage usage, a key concern raised in the project motivation .

---

## 5. Share

### Key Insights

* A small number of high-resolution photo or video files can outweigh hundreds of compressed images
* Storage growth accelerates during periods of increased shooting intensity
* Certain days or periods show consistently higher activity
* File type composition strongly influences storage efficiency

Insights are presented using clear visuals and non-technical explanations.

---

## 6. Act

### Recommendations

* Plan future storage purchases based on file type composition, not file count
* Separate large RAW/video files into dedicated archives
* Monitor shooting frequency trends to anticipate storage needs
* Standardize folder structures to simplify long-term management

### Next Steps

* Deeper time-series analysis of storage growth
* File lifecycle analysis (active vs cold storage)
* Optional predictive modeling for future storage forecasting

---

## Repository Structure

```text
.
├── data/
│   └── dataset.csv
├── eda_google_capstone_style.ipynb
└── README.md
```

---

## Reproducibility Notes

* Relative paths are used throughout
* All transformations are explicitly documented
* Notebook can be run end-to-end given the dataset

---

## Disclaimer

This project uses **personal but anonymized metadata** and is shared strictly for **educational and portfolio purposes**.
No original media files or identifiable information are included.