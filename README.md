# Olympic Data Preprocessing with Python & Pandas 🏅📊

This project focuses on cleaning and transforming an Olympic athlete dataset using Python and pandas. The goal is to convert raw, inconsistent data into a clean format ready for analysis and visualization.

---

## 🚀 What’s Included

- ✅ String parsing and feature extraction (`.str.split()`, `.str.contains()`, regex)
- ✅ Handling units (e.g., `"cm"`, `"kg"`) and converting to floats
- ✅ Resolving ranges (e.g., `"73-75 kg"` → `74.0`)
- ✅ Creating clean `height_cm` and `weight_kg` columns
- ✅ Managing missing or malformed entries

---

## 📁 Files

| File | Description |
|------|-------------|
| `Olympic_Data_Cleaning.ipynb` | Main Jupyter notebook with preprocessing steps |
| `README.md` | This file — project overview and usage instructions |

---

## ⚙️ Environment Setup

To run this project locally:

1. Clone the repo:
   ```bash
   git clone https://github.com/haoranwang99/Data-Processing-with-Python-Pandas-.git
   cd Data-Processing-with-Python-Pandas-
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

> 💡 If no `requirements.txt` is present yet, just manually install:
```bash
pip install pandas jupyter
```

4. Launch Jupyter:
   ```bash
   jupyter notebook
   ```

---

## 🔍 Sample Output

Here’s a simplified example of the preprocessing outcome:

| Measurements     | height_cm | weight_kg |
|------------------|-----------|-----------|
| 180 cm/75 kg     | 180.0     | 75.0      |
| 165 cm           | 165.0     | NaN       |
| 90 kg            | NaN       | 90.0      |
| 172 cm/73-75 kg  | 172.0     | 74.0      |

---

## 📈 Next Steps

- [ ] Clean additional fields (e.g., sport, country, medal)
- [ ] Basic summary statistics and distributions
- [ ] Visualizations using `matplotlib` or `seaborn`
- [ ] Export clean dataset to CSV

---

## 💡 Ideas for Expansion

- Integrate external data sources (e.g., medal records, historical performance)
- Analyze trends by gender, sport, country
- Build a lightweight dashboard using `Streamlit` or `Plotly Dash`

---

## 🤝 Contributing

If you'd like to collaborate, feel free to fork the repo and submit a pull request. Suggestions are always welcome!

---

Made with 🐼 by [@haoranwang99](https://github.com/haoranwang99)
