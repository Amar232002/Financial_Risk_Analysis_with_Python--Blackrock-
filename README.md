# 📊 BlackRock Financial Transaction Analysis

## 🧾 Project Overview
This project performs a comprehensive financial analysis on BlackRock's 
transaction dataset containing 800 transactions spanning January 2023 
to June 2024. The analysis covers data cleaning, customer profiling, 
risk identification, and statistical hypothesis testing.

---

## 📁 Dataset
- **File:** `blackrock__1_.csv`
- **Records:** 800 transactions
- **Period:** January 2023 – June 2024
- **Key Columns:** TransactionID, CustomerID, AccountID, AccountType,
  TransactionType, TransactionAmount, AccountBalance, RiskScore,
  CreditRating, TenureMonths, TransactionDate

---

## ✅ Tasks Completed

### Task 1 — Data Cleaning & Formatting
- Removed special characters and non-numeric entries
- Converted all financial fields to numeric format
- Validated and standardized date columns (DD-MM-YYYY)
- Standardized AccountType, TransactionType, Region, Product fields

### Task 2 — Descriptive Transactional Analysis
- Calculated monthly and yearly summaries of credits, debits, net volume
- Plotted credit vs debit trends over 18 months
- Identified top 5 and bottom 5 accounts by net inflow
- Flagged dormant accounts with 2+ month gaps between transactions

### Task 3 — Customer Profile Building
**Activity Level Rubric:**
| Level | Criteria |
|-------|----------|
| High | TxnCount ≥ 10 |
| Medium | TxnCount 5–9 |
| Low | TxnCount ≤ 4 |

- Segmented customers by average balance and transaction volume
- Built 3 profiles: High Net Inflow, High-Frequency Low-Balance,
  Negative/Near-Zero Balance accounts

### Task 4 — Financial Risk Identification
- Tracked accounts with frequent large withdrawals (≥ 90th percentile)
- Calculated balance volatility using Coefficient of Variation (CV)
- Detected anomalies using IQR method and Z-Score (threshold = 3)
- Flagged suspicious customers showing both overdraft and large withdrawals

### Task 5 — Visualisation (EDA)
- 8 comprehensive visualizations covering transaction types, regional 
  analysis, correlation heatmap, risk score distribution, and more

### Task 6 — Hypothesis Testing
- **H1 (t-test):** High-volume accounts have statistically higher 
  average balances than low-volume accounts
- **H2 (ANOVA):** Activity level significantly affects average balance
- Both tested at α = 0.05 significance level

---

## 📈 Key Findings
- Several accounts flagged as **dormant** (2+ month inactivity gap)
- **High-frequency low-balance** segment shows churn and stress risk
- Overdraft accounts identified as immediate **credit risk**
- IQR and Z-score methods detected **anomalous transactions**
- Hypothesis testing provided **statistically backed** segmentation insights

---

## 💡 Recommendations
1. **Re-engagement campaigns** for dormant accounts
2. **Savings/investment products** for high-frequency low-balance customers
3. **Enhanced monitoring** for high-volatility and overdraft accounts

---

## 🛠️ Tech Stack
| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Pandas | Data cleaning & manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualizations |
| Seaborn | Statistical plots |
| SciPy | Hypothesis testing |

---

## 🚀 How to Run
```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/blackrock-financial-analysis.git

# 2. Navigate to folder
cd blackrock-financial-analysis

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn scipy

# 4. Run the analysis
python blackrock_analysis.py
```

---

## 📊 Sample Visualizations

### Task 2 — Credits vs Debits Trend
![Task 2](plots/task2_credits_debits_trend.png)

### Task 4 — Risk Dashboard
![Task 4](plots/task4_risk_dashboard.png)

### Task 6 — Hypothesis Testing
![Task 6](plots/task6_hypothesis_testing.png)
