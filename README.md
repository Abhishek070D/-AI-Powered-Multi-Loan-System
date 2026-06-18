# 🏦 AI-Powered Multi-Vertical Banking Finance System

An end-to-end intelligent banking ecosystem featuring automated data engineering pipelines, advanced machine learning classification & regression models, and a premium interactive dashboard interface. The system evaluates credit risk, predicts optimal loan amounts, sets dynamic interest rates, and structures automated business guardrails across four distinct banking loan verticals.

---

## 🚀 Key Features

* **Multi-Vertical Evaluation:** Custom risk-modeling architecture built specifically for **Personal, Home, Education, and Gold Loans**.
* **Dual-Stage ML Engines:** Leverages optimized classification models to predict loan approval/rejection combined with secondary regression models to dynamically estimate approved amounts and risk-adjusted interest rates.
* **Advanced Data Diagnostics:** Production-grade pipeline tackling real-world telemetry anomalies, missing value imputations, and outlier smoothing.
* **Business Rule Enforcement:** Embedded algorithmic guardrails ensuring automatic filtration via Debt-To-Income (DTI) thresholds, minimum CIBIL limits, and LTV boundaries.
* **Premium Interactive Portal:** A fully functional Streamlit frontend dashboard simulating a real banking web interface.

---

## 📊 System & Database Architecture

The core data layout is structured to cleanly decouple customer profiles, core assets, and loan-specific evaluations to optimize reporting and storage.
<img width="1393" height="742" alt="image" src="https://github.com/user-attachments/assets/1206cb70-1188-475f-bb8b-8189235aed8e" />
### 📈 Supported Verticals & Datasets
1.  **Personal Loans (`personal_loan_dataset.csv`):** Unsecured lending risk evaluated using 6-month average bank balances, job tenure, past defaults, and application inquiry frequency.
2.  **Home Loans (`home_loan_dataset.csv`):** Asset-backed mortgage underwriting considering co-applicant incomes, asset values, property ages, and builder structural grades. 
3.  **Education Loans (`education_loan.csv`):** Merit-and-means framework matching applicant academic/entrance scores with parental income, course levels, and international/domestic risk matrices.
4.  **Gold Loans (`gold_loan_dataset_with_missing_values.csv`):** Highly collateralized lending emphasizing gold weight, karat purity, estimated live valuations, and Loan-to-Value (LTV) limits.

---

## 🛠️ Tech Stack & Directory Structure

* **Frontend UI:** Streamlit (Custom premium theme architecture)
* **Data Science:** Python, Pandas, NumPy, Scikit-Learn
* **Visualizations:** Matplotlib, Seaborn
* **Model Storage:** Serialization via Pickle

### Repository Breakdown
```text
├── datasets/
│   ├── personal_loan_dataset.csv
│   ├── home_loan_dataset.csv
│   ├── education loan.csv
│   └── gold_loan_dataset_with_missing_values.csv
├── notebooks/
│   ├── Personal_loan.ipynb           # Classification & Regression Pipeline
│   ├── home_loan_complete.ipynb      # EDA, ML Classification/Regression & KMeans Clustering
│   ├── Education_Loan_Complete_ML_FIXED.ipynb
│   └── gold_loan_phase1.ipynb         # Collateral math & predictive evaluation
├── loan_app1.py                      # Multi-page premium Streamlit App
├── ER-Diagram.png                    # Underling relational structural model
└── README.md
⚙️ How It Works (Algorithmic Flow)
[ User Input Data ] 
       │
       ▼
[ Phase 1: Hard Business Rule Audit ] ────► (If Fail) ──► [ Automatic Rejection ]
       │ (Pass)
       ▼
[ Phase 2: Classification Engine ]   ────► (If High Risk) ──► [ Rejection Display ]
       │ (Approved)
       ▼
[ Phase 3: Regression Matrix ] ──────► Predicts Max Approved Amount
       │                                     ► Predicts Risk-Adjusted Interest Rate
       ▼
[ Premium Interactive Visualization & Result Summary ]
🚦 Getting Started
1. Clone the repository
Bash
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name
2. Install dependencies
Bash
pip install -r requirements.txt
(Make sure to export your environment requirements using pip freeze > requirements.txt before uploading).

3. Run the Production Dashboard
Bash
streamlit run loan_app1.py
🔮 Future Enhancements
Database Integration: Transition flat CSV files into live PostgreSQL/MySQL infrastructure based on the provided ER-Diagram.

Advanced Model Deployments: Upgrade from standard Scikit-Learn algorithms to XGBoost/LightGBM pipelines.

Explainable AI (XAI): Integrate SHAP or LIME visualizations in the Streamlit frontend to explicitly tell users why their loan application got rejected or flagged.


---

### 💡 Pro-Tips for your GitHub Repository:
1. **Add a `.gitignore`:** Before you commit anything, add a `.gitignore` file to ensure you don't push bulky log folders, `.ipynb_checkpoints`, or system `.DS_Store` files. 
2. **Include App Screenshots:** Take 1-2 screenshots of your Streamlit application layout (`loan_app1.py`) and paste them into the README under the "Premium Interactive Portal" section. Visuals significantly boost engagement!

Would you like me to help you generate the exact `.gitignore` file or format a `requireme
