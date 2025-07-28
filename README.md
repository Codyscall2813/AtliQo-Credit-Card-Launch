```markdown
# AtliQo Bank Credit Card Launch Analysis

## 📋 Project Overview
This repository contains the end‑to‑end analysis for AtliQo Bank’s new credit card launch, split into two distinct phases:

- **Phase 1:** Exploratory Data Analysis (EDA) & sample‑size determination to identify target customer segments  
- **Phase 2:** Business analysis and A/B testing of a trial campaign to validate effectiveness  

Our goal is to identify the most promising customer profiles and measure the impact of the new card on transaction behavior.

---

## 📂 Repository Structure

```

├── data/
│   ├── transactions.csv        # Raw transaction data (CSV)
│   └── E\_MasterCardDump.sql    # Raw transaction data (MySQL dump)
│
├── notebooks/
│   ├── phase\_1\_atliqo\_bank.ipynb   # Phase 1: EDA & sample-size analysis
│   └── phase\_2\_atliqo\_bank.ipynb   # Phase 2: A/B test setup & KPI evaluation
│
├── requirements.txt           # Python dependencies
│
├── results/
│   ├── figures/               # Charts and visual outputs
│   └── tables/                # Summary tables and CSV exports
│
└── README.md                  # Project overview and instructions

````

---

## 🛠️ Installation & Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/<your-username>/atliqo-credit-card-launch.git
   cd atliqo-credit-card-launch
````

2. **Create a virtual environment** (recommended)

   ```bash
   python -m venv venv
   source venv/bin/activate       # Linux/Mac
   venv\Scripts\activate          # Windows
   ```
3. **Install requirements**

   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 Usage

1. **Load the data**

   * Option A: Use `data/transactions.csv`
   * Option B: Import `data/E_MasterCardDump.sql` into MySQL and connect via Python

2. **Run Phase 1 analysis**
   Open and execute `notebooks/phase_1_atliqo_bank.ipynb` to:

   * Explore customer transaction patterns
   * Determine optimal sample size for A/B testing

3. **Run Phase 2 A/B test**
   Open and execute `notebooks/phase_2_atliqo_bank.ipynb` to:

   * Segment customers (e.g., age 18–25)
   * Design control and test groups
   * Perform hypothesis testing (e.g., two‑sample Z-test)
   * Evaluate KPI: average transaction value uplift

4. **Review results**

   * Charts and statistical outputs are saved under `results/figures/`
   * Summary tables available in `results/tables/`

---

## 📊 Key Findings

* **Phase 1:**

  * Identified age 18–25 as an under‑served segment (\~25% of base)
  * Calculated that 393 customers are needed for 80% power at 5% significance

* **Phase 2:**

  * Conducted a 2‑month pilot (09‑10‑2023 to 11‑12‑2023)
  * A/B test showed a statistically significant increase in average transaction amount for the new card (p < 0.05)

---

## 📦 Dependencies

All Python packages are listed in `requirements.txt`. Major libraries include:

* `pandas`, `numpy` – data manipulation
* `matplotlib`, `seaborn` – visualization
* `statsmodels`, `scipy` – statistical tests
