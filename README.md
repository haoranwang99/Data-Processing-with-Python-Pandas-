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