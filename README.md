# Seasonal Agriculture Performance Analysis

**VOIS AICTE Batch1 2026-2027 — Major Project**

Analysis of a seasonal agriculture performance dataset covering **4,000 farm-level records** across
**8 Indian states**, **8 crops**, and **3 seasons** (Kharif, Rabi, Zaid), investigating how yield, cost,
revenue, profit, water efficiency and disease/pest risk vary by season — and what drives those differences.

## Repository Structure

```
├── README.md                                          # This file
├── requirements.txt                                   # Python dependencies
├── .gitignore
├── seasonal_agriculture_performance_analysis.py        # Standalone analysis script
├── Seasonal_Agriculture_Performance_Analysis.ipynb     # Full documented analysis notebook (required deliverable)
└── data/
    └── seasonal_agriculture_performance_dataset.csv    # Source dataset (4,000 rows x 28 columns)
```

Charts are **generated on the fly** when the notebook or script is run (saved to a local `outputs/charts/`
folder, which is git-ignored) rather than committed to the repo — they're fully reproducible from the code.

## How to Run

```bash
pip install -r requirements.txt

# Option A: run the notebook (primary deliverable, with full explanations)
jupyter notebook Seasonal_Agriculture_Performance_Analysis.ipynb

# Option B: run the plain script (same analysis, no explanations, faster to execute)
python seasonal_agriculture_performance_analysis.py
```

Both read the dataset from `data/seasonal_agriculture_performance_dataset.csv` and save all 10 charts to
`outputs/charts/` (created automatically).

## Notebook / Script Contents

1. Import Libraries & Load Data
2. Dataset Overview
3. Data Cleaning & Preparation (seasonal/crop-wise median imputation for missing values)
4. Exploratory Data Analysis — seasonal comparisons (yield, profit, rainfall/temperature, water
   efficiency, disease/pest risk, crop x season heatmap)
5. Relationships Between Variables — correlation analysis, irrigation method mix
6. Crop & State Level Insights — cost/revenue/profit breakdown, top profitable states
7. Key Findings
8. Conclusions & Recommendations

## Key Findings

- **Kharif** is the best-performing season overall — highest yield (5.63 t/ha), highest profit
  (₹1.79L avg.), and highest water-use efficiency — backed by the highest rainfall.
- **Zaid** is the weakest season — lowest yield and a small average **loss**, driven by high
  temperatures and lower rainfall.
- Disease/pest risk tracks rainfall closely (correlation 0.62) — Kharif's rainfall advantage comes
  with higher pest pressure.
- **Sugarcane** is the top-yielding crop across all three seasons among the 8 crops studied.
- **Flood irrigation** dominates (~33% of farms) in every season; drip/sprinkler remain a minority.
- Fertilizer usage shows almost no correlation with yield or profit — a sign of possibly
  unoptimized application.
- **Punjab, Maharashtra, and Karnataka** are the most profitable states on average.
- Nearly **49%** of all farm records show a negative profit, pointing to widespread cost-control issues.

## Tech Stack

- Python 3
- Pandas & NumPy — data cleaning and aggregation
- Matplotlib & Seaborn — visualization
- Jupyter Notebook — documented, reproducible analysis

## Author

Add your name, college, and AICTE Student ID here.
