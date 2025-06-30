# Olympic Data Preprocessing with Python & Pandas 🏅📊

This project focuses on cleaning and transforming an Olympic athlete dataset using Python and pandas. The goal is to convert raw, inconsistent biographical data into a clean format ready for analysis and visualization.

---

## 🚀 Key Features

- ✅ **String parsing** from `Used name` (e.g., removing bullet points)
- ✅ **Measurement normalization**:
  - Split and clean `height_cm` and `weight_kg` from the `Measurements` column
  - Handles irregular formats or missing delimiters
- ✅ **Date extraction**:
  - Uses regex to extract `Born` and `Died` information
  - Supports formats like `5 June 1995`, `June 1995`, `circa 1985`, etc.
- ✅ Missing value handling and basic sanity checks
- ✅ Intermediate DataFrame copies to preserve original data

---

## 📁 Files

| File                      | Description                                |
|---------------------------|--------------------------------------------|
| `Untitled4.ipynb`         | Main Jupyter notebook with preprocessing   |
| `README.md`               | This file — project overview & usage       |

---

## ⚙️ Environment Setup

To run this project locally:

1. Clone the repo:
   ```bash
   git clone https://github.com/haoranwang99/Data-Processing-with-Python-Pandas-.git
   cd Data-Processing-with-Python-Pandas-
   ```

2. Install dependencies:
   ```bash
   pip install pandas
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook
   ```

---

## 📊 Sample Workflow

```python
import pandas as pd
import re

# Load data and copy to preserve original
df = pd.read_csv('./Olympic/bios.csv')
df_clean = df.copy()

# Clean names
df_clean['name'] = df_clean['Used name'].str.replace("•", " ")

# Handle Measurements column
def split_measurements(df):
    df['height_cm'] = None
    df['weight_kg'] = None
    mask_both = df['Measurements'].str.contains(" cm", na=False) & df['Measurements'].str.contains(" kg", na=False)
    split_df = df.loc[mask_both, 'Measurements'].str.split('/', expand=True)
    df.loc[mask_both, 'height_cm'] = split_df[0]
    df.loc[mask_both, 'weight_kg'] = split_df[1]
    return df

df_clean = split_measurements(df_clean)

# Extract dates using regex
date_pattern = r'(?i)(?:circa\s*)?(\d{1,2} \w+ \d{4}|\w+ \d{4}|\d{4})'
df_clean['born_date'] = df_clean['Born'].str.extract(date_pattern)
df_clean['died_date'] = df_clean['Died'].str.extract(date_pattern)
```

---

## 🧼 Notes

- This project demonstrates real-world data cleaning with many edge cases.
- For more advanced NLP and entity extraction, libraries like `spaCy` or `dateparser` could enhance recognition.

---

## 📬 Feedback

Open to suggestions! Fork, star, or raise an issue.
