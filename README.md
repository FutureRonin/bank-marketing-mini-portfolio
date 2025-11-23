# Bank Marketing – Mini Portfolio (Google Colab)

Mini portfolio based on a common Bank Marketing case study:
- K-Means clustering (`balance`, `age`, `campaign`)
- Simple charts (bar, pie, scatter)
- Correlations (numeric subset)
- Cleaned CSV export for reproducibility (and optional Tableau use)

This project uses **matplotlib only** (no seaborn) and does **not** set custom colors.

---

## 1) How to Run (Google Colab)

1. Download the notebook from this repo.
2. Open **Google Colab** → **File → Upload Notebook** → select the `.ipynb`.
3. Run the cells from top to bottom.
4. When prompted in the **Upload your CSV** cell, choose the CSV file (`bank.csv`).

**Outputs you’ll get:**
- Cleaned CSV: `bank_clean.csv`
- K-Means cluster labels (`cluster` column) in the DataFrame
- Charts: bar, pie, scatter (matplotlib)
- Correlation tables/prints

---

## 2) File / Column Notes

- Common numeric columns used:
  - `age`, `balance`, `campaign`, `day`, `duration`, `pdays`, `previous`
- If the CSV has a `y` column (yes/no outcome), this notebook can compute correlations to `y` (converted to `0/1`).

---

## 3) Minimal Workflow

1. **Upload Dataset** (Kaggle Bank Marketing).
2. **Clean**:
   - Drop duplicates
   - Fill numeric with median, categorical with `"Unknown"`
   - Create simple buckets (`age_bucket`, `balance_bucket`)
3. **Save processed CSV** → `bank_clean.csv`
4. **Clustering**:
   - Scale (`StandardScaler`)
   - K-Means (`n_clusters=5`, `n_init=10`, `random_state=42`)
   - Add `cluster` to DataFrame
5. **Visualize**:
   - Bar: customers per `age`
   - Pie: distribution by `previous` (if exists)
   - Scatter: `age` vs `balance`
6. **Correlations**:
   - Subset numeric columns, show correlation matrix
   - Correlation to binary `y` if present

---

## 4) Author

Kurnia Akbar Archa Prasetyo — Data Analyst (Beginner)  
LinkedIn: (https://www.linkedin.com/in/archaprasetyo/) · Email: archaprasetyo@gmail.com
