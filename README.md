# Excel ETL Pipeline for Automotive Inventory Management


## Overview
This project automates the consolidation of thousands of Excel files into a structured multi-sheet workbook, and then merges all sheets into a single unified worksheet for further analysis.

The workflow is designed for industrial environments where operational data is highly fragmented and manual consolidation is time-consuming and error-prone.

---

## Industrial Background
In an automotive manufacturing plant, the inflow and outflow of raw materials must be controlled very carefully.  
Warehouse operations require close monitoring of:

- on-time delivery
- delivered quantities
- material traceability
- production line feeding
- inventory consistency
- production support during critical phases

These controls become even more important during the pilot production stage of a new heavy-duty truck product, where the first production runs are especially sensitive to material shortages, reporting gaps, and operational delays.

---

## Problem Statement
The organizational software used in the factory had limitations in reporting and output generation.  
In particular, it lacked some control modules needed for efficient data verification and aggregation.

As a result, the available information was distributed across thousands of separate Excel files.  
Managing this manually was difficult because:

- the data was fragmented
- consolidation required several days of work
- manual processing increased the risk of human error
- reporting for warehouse and production control was slow
- urgent operational decisions were delayed

In practice, organizing and standardizing these files by other methods would take a lot of time and effort.

---

## Solution
To solve this problem, I developed two automation scripts:

### 1. `sum_sheets`
This script converts thousands of individual Excel files into one Excel workbook, where each file becomes a separate sheet.

### 2. `merge_sheets`
This script takes that multi-sheet workbook and merges all sheets into one single worksheet containing thousands of rows.

### 3. Excel Pivot Analysis
In cases where higher-level aggregation was needed, the merged data was also analyzed using Excel pivot tables to support summary review and control checks.

Together, these steps transform scattered operational data into a structured and usable format.

---

## Why This Project Matters
This project was not only a file-processing task.  
It solved a real operational bottleneck in a high-volume automotive manufacturing environment.

By automating the workflow:

- data organization became much faster
- warehouse and inventory checks became easier
- line-feeding control improved
- delivery and quantity verification became more reliable
- pilot production support became smoother
- several days of manual work were reduced to a much shorter automated process

This was especially valuable because the factory needed fast and accurate reporting, while the enterprise software did not provide all the required control modules.

---

## Workflow
1. Collect thousands of Excel files from operational records
2. Run `sum_sheets` to combine them into one workbook with multiple sheets
3. Run `merge_sheets` to convert the workbook into a single sheet
4. Use pivot tables when needed for higher-level aggregation and control review

---

## Repository Structure
```bash
.
├── sum_sheets.py
├── merge_sheets.py
├── data/
│   └── sample_files/
├── README.md
└── requirements.txt
