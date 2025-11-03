# HIV CSV Example Repository

This repository contains a single dataset file used for examples and small data experiments:

- `hiv.csv` — a CSV data file included with this repo.

Use this repository as a starting point for data exploration, analysis, or small demos.

## Contents

- `hiv.csv` — the dataset (CSV). Inspect it locally to see the exact columns and rows.

## Quick start

Below are a few quick ways to inspect and load the CSV on Windows (PowerShell) and with Python (pandas).

### Inspect with PowerShell

Open a PowerShell prompt in the repository folder and run:

```powershell
# Show the first 10 lines
Get-Content .\hiv.csv -TotalCount 10

# Parse the CSV and show the first 5 records as objects
Import-Csv .\hiv.csv | Select-Object -First 5 | Format-Table -AutoSize
```

### Load with Python (pandas)

Recommended: create a virtual environment and install pandas before running the example.

```powershell
# Windows PowerShell (create venv and install pandas)
python -m venv .venv; .\.venv\Scripts\Activate.ps1; pip install --upgrade pip pandas
```

Then a short Python example to read and preview the CSV:

```python
import pandas as pd

df = pd.read_csv('hiv.csv')
print(df.shape)
print(df.head())
```

Name: Alazar Yared