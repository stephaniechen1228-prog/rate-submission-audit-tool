# Rate Submission Audit Tool

An automated audit testing tool built with Python to detect anomalies in daily interest rate submissions (e.g. TAIBOR or similar benchmarks).

## What This Tool Does

This tool automatically scans rate submission data and flags the following exceptions:

1. **Duplicate Submissions** — same date and tenor submitted more than once
2. **Segregation of Duties (SoD) Violations** — maker and checker are the same person
3. **Deadline Breaches** — submissions after internal deadline (10:30) or regulatory deadline (11:00)
4. **Rate Movement Anomalies** — rate changes exceeding 10% vs. prior day for the same tenor
5. **Missing Submissions** — tenors not submitted on a given day

## Output

Generates an Excel report with separate tabs for each exception type, ready for audit documentation.

## Tools Used

- Python / Jupyter Notebook
- pandas
- openpyxl

## Background

Built as part of an initiative to automate manual audit testing procedures using Python and AI tools, reducing review time and improving exception detection consistency.
