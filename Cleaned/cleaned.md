# 🧹 Data Cleaning Log — River Water Quality Dataset

> **File:** `cleaned.csv`
> **Source:** CPCB via NITI Aayog NDAP
> **Original Rows:** ~12,000+ | **Post-Cleaning Rows:** 11,718

---

## 📋 Column-wise Changes

| Column | Changes Made |
|--------|-------------|
| **Country** | No Changes |
| **Year** | Renamed from `"Calendar Year (Jan - Dec), YEAR"` to `YEAR` |
| **State Name** | No Changes |
| **Station Code** | Removed rows where station code isn't mentioned |
| **Monitoring Location** | No Changes |

---

## 🌡️ Temperature

| Column | Action |
|--------|--------|
| Minimum Temperature For River Water `(UOM: °C)` | Imputed missing values with **median → 19** |
| Maximum Temperature For River Water `(UOM: °C)` | Imputed missing values with **median → 29** |

---

## 💧 Dissolved Oxygen (DO)

| Column | Action |
|--------|--------|
| Minimum Value of Dissolved Oxygen `(UOM: mg/L)` | Imputed missing values with **median → 6** |
| Maximum Value of Dissolved Oxygen `(UOM: mg/L)` | Imputed missing values with **median → 8** |

---

## 🧪 pH

| Column | Action |
|--------|--------|
| Minimum Potential of Hydrogen `(UOM: pH)` | Imputed missing values with **median → 7.2** |
| Maximum Potential of Hydrogen `(UOM: pH)` | Imputed missing values with **median → 8.2** |

---

## ⚡ Conductivity

| Column | Action |
|--------|--------|
| Minimum Conductivity Level `(UOM: µmho/cm)` | Imputed missing values with **median → 206** |
| Maximum Conductivity Level `(UOM: µmho/cm)` | Imputed missing values with **median → 476** |

---

## 🦠 Biochemical Oxygen Demand (BOD)

| Column | Action |
|--------|--------|
| Minimum BOD `(UOM: mg/L)` | Imputed missing values with **median → 1.3** |
| Maximum BOD `(UOM: mg/L)` | Imputed missing values with **median → 2.8** |

---

## 🌿 Nitrate (N)

| Column | Action |
|--------|--------|
| Minimum Nitrate (N) `(UOM: mg/L)` | Imputed missing values with **median → 0.3** |
| Maximum Nitrate (N) `(UOM: mg/L)` | Imputed missing values with **median → 1.34** |

---

## 🧫 Fecal Coliforms

| Column | Action |
|--------|--------|
| Minimum Fecal Coliforms `(UOM: MPN/100ml)` | Imputed missing values with **median → 45** |
| Maximum Fecal Coliforms `(UOM: MPN/100ml)` | Imputed missing values with **median → 400** |

---

## 🔬 Total Coliform

| Column | Action |
|--------|--------|
| Minimum Total Coliform `(UOM: MPN/100ml)` | Imputed missing values with **median → 225** |
| Maximum Total Coliform `(UOM: MPN/100ml)` | Imputed missing values with **median → 1600** — also renamed from `"Minimum"` to `"Maximum"` *(original column was mislabelled)* |

---

## ❌ Removed Columns

| Column | Reason |
|--------|--------|
| Minimum Fecal Streptococci `(UOM: MPN/100ml)` | Removed due to large number of missing values |
| Maximum Fecal Streptococci `(UOM: MPN/100ml)` | Removed due to large number of missing values |

---

## ✅ New Columns Created

| Column | Description |
|--------|-------------|
| `BOD_Avg` | Average of Minimum and Maximum BOD values |
| `DO_Avg` | Average of Minimum and Maximum DO values |
| `pH_Avg` | Average of Minimum and Maximum pH values |
| `Nitrate_Avg` | Average of Minimum and Maximum Nitrate values |
| `Pollution_Flag` | Binary flag — `1` if BOD_Avg exceeds threshold, `0` otherwise |
| `Pollution_Category` | Categorizes record as `Clean`, `Moderate`, or `Polluted` |
| `Water Quality Index` | Composite index created from key water quality parameters |

---

## 📝 Notes

- All imputations used **median** values to reduce the effect of outliers
- Rows with missing **Station Codes** were dropped entirely as they could not be reliably identified or georeferenced
- The `Maximum Total Coliform` column was discovered to be mislabelled as `"Minimum"` in the raw dataset and was corrected
- Fecal Streptococci columns were dropped as the volume of missing data made imputation unreliable and potentially misleading