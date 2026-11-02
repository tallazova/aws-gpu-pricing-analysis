# AWS GPU Instance Pricing Analysis

Analysis of on-demand GPU instance pricing on AWS, with an interactive Tableau Public dashboard.

**Dashboard:** [link to Tableau Public viz]

## Question
How does price per GPU-hour compare across AWS GPU instance families and regions?

## Data
- Source: AWS public Price List bulk file (no credentials needed)
- Region used: eu-central-1 (Frankfurt)
- Pulled: 23 Oct 2026
- The raw file (~434 MB) is not included. Download it from the AWS Price List and place it in `data/raw/`.

## Method
1. Load the price file and extract the products into a pandas DataFrame
2. Filter to GPU instances (Linux, shared tenancy, no preinstalled software)
3. Convert text specs ("61 GiB") to numeric values
4. Remove duplicates (key: instance type, OS, tenancy, license model)
5. Calculate `usd_per_gpu_hr = price / gpu_count`

## Key findings
- (finding 1)
- (finding 2)

## Repository contents
- `notebooks/`: data loading and cleaning notebook
- `data/clean/`: cleaned dataset (CSV)
- `requirements.txt`: Python dependencies

## How to run
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```
Then run the notebook top to bottom.

## Tools
Python, pandas, Jupyter, Tableau Public