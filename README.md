# 🚗 Used Vehicle Price Predictor | Multi-Source Preprocessing Pipeline

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Status](https://img.shields.io/badge/Status-Data%20Preprocessed-success?style=for-the-badge)

## 📌 Project Overview
An end-to-end Data Engineering and Preprocessing pipeline designed to construct a unified dataset for used vehicle price estimation. 

The original datasets consisted of four separate, raw CarDekho schemas (v1, v2, v3, and v4) with missing values, string units, duplicate records, and conflicting column definitions. This project cleans, standardizes, and consolidates all four sources into a single structured dataset containing **12,364 clean observations** ready for exploratory analysis and model training.

---

## 📊 Dataset Statistics & Schema

* **Original Merged Data Points:** ~14,800+
* **Final Cleaned Records:** 12,364 rows
* **Features:** 16 attributes
* **Missing Values:** 0 (Fully Cleaned & Imputed)

### Consolidated Features
| Feature | Data Type | Description |
| :--- | :--- | :--- |
| `name` | Categorical | Vehicle make and model details |
| `year` | Numeric (Int) | Manufacturing year (1983 - 2022) |
| `selling_price` | Numeric (Int) | **Target Variable:** Resale price |
| `km_driven` | Numeric (Int) | Total distance covered (in KM) |
| `fuel` | Categorical | Petrol, Diesel, CNG, LPG, Electric, etc. |
| `seller_type` | Categorical | Individual, Dealer, Trustmark Dealer, etc. |
| `transmission` | Categorical | Manual vs Automatic |
| `owner` | Numeric (Ordinal) | Ownership count scale (0 to 4) |
| `mileage` | Numeric (Float) | Fuel efficiency rating (kmpl / km/kg) |
| `engine` | Numeric (Int) | Displacement capacity (in CC) |
| `max_power` | Numeric (Float) | Maximum brake horsepower (bhp) |
| `torque` | Numeric (Float) | Engine torque (Nm) |
| `seats` | Numeric (Float) | Seating capacity |
| `Location` | Categorical | Regional market location |
| `Color` | Categorical | Body paint color |
| `Drivetrain` | Categorical | FWD, RWD, AWD |

---

## 🛠️ Data Preprocessing Steps Completed

1. **Multi-Source Data Schema Aggregation:** Concatenated and standardized heterogeneous column naming conventions across 4 raw source files (CarDekho v1 to v4).
2. **Deduplication:** Identified and dropped **1,969 duplicate observations** across the aggregated dataset.
3. **Regex Extraction & Type Casting:** Cleaned numerical metrics wrapped in text formats across `mileage`, `engine`, `max_power`, and `torque` columns into standard numeric types (`float64` / `int64`).
4. **Target Variable Scale Standardization:** Fixed price unit discrepancies across raw sources to align all observations on a single numerical scale.
5. **Missing Value Imputation:** Handled missingness across attributes to achieve zero missing values.

---

## ⏳ Next Steps / Roadmap

- [x] Merge raw multi-source CarDekho datasets (v1 to v4)
- [x] Complete feature cleaning, deduplication & type conversion
- [ ] Exploratory Data Analysis (EDA) & Feature Distribution Analysis
- [ ] Feature Encoding (One-Hot / Ordinal Encoding for categorical variables)
- [ ] Baseline Model Training (Linear Regression)
- [ ] Advanced Regression Models & Hyperparameter Tuning (Random Forest, XGBoost)

---

## 📁 Repository Structure

```text
├── Clean Car Data.csv          # Final preprocessed dataset (12,364 rows)
├── vehicle_preprocessing.ipynb # Data cleaning and wrangling notebook
├── README.md                   # Project documentation
└── requirements.txt            # Python environment dependencies
```

---

## 💻 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/vehicle-price-predictor.git
   cd vehicle-price-predictor
   ```

2. **Install required packages:**
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

---

## 👨‍💻 Author
**Mudassir Khan**  
* Aspiring Data Scientist & Machine Learning Developer  
* GitHub: [@mudassirkhan1249](https://github.com/mudassirkhan1249)

---
*If you find this repository helpful, consider giving it a ⭐️!*
