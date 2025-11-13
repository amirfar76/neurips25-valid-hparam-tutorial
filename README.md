# From Tuning to Guarantees: Statistically Valid Hyperparameter Selection

This repository accompanies the NeurIPS 2025 tutorial:

**“From Tuning to Guarantees: Statistically Valid Hyperparameter Selection.”**

It provides three interactive notebooks demonstrating:
- **Learn-Then-Test (LTT)** — average risk control  
- **Pareto Testing** — multi-objective risk control  
- **Quantile Learn-Then-Test (QLTT)** — quantile-based risk control  

Each notebook is complete, self-contained, and generates its own synthetic CSV dataset so attendees can immediately run them on Google Colab.

---

# 📚 Tutorial Notebooks (Open in Google Colab)

### **1. Learn-Then-Test (LTT)**  
Compute per-hyperparameter empirical risks and control average loss using Hoeffding p-values + Bonferroni/FST.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amirfar76/neurips25-valid-hparam-tutorial/blob/main/notebooks/01_LTT_risk_control.ipynb)

---

### **2. Pareto Testing**  
Identify Pareto-optimal hyperparameters and apply Fixed-Sequence Testing over the frontier to guarantee risk control while optimizing a secondary objective.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amirfar76/neurips25-valid-hparam-tutorial/blob/main/notebooks/02_ParetoTesting.ipynb)

---

### **3. Quantile Learn-Then-Test (QLTT)**  
Control a user-specified quantile of the risk (e.g., 0.1-quantile), using the Howard–Ramdas bound and Bonferroni to guarantee reliability.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amirfar76/neurips25-valid-hparam-tutorial/blob/main/notebooks/03_QLTT_quantile_risk_control.ipynb)

---

# 📁 Repository Structure

```text
.
├── README.md
├── requirements.txt
├── data/
│   ├── sample_LTT_losses.csv         
│   ├── sample_PT_losses.csv          
│   └── sample_QLTT_losses.csv        
└── notebooks/
    ├── 01_LTT_risk_control.ipynb
    ├── 02_ParetoTesting.ipynb
    └── 03_QLTT_quantile_risk_control.ipynb
```

---

# 📄 Data Format

Each synthetic dataset follows a clear format so attendees can easily replace it with their own.

### **LTT dataset (`sample_LTT_losses.csv`)**
- `lambda_id`
- `loss_1, loss_2, ..., loss_M`

### **Pareto Testing dataset (`sample_PT_losses.csv`)**
- `lambda_id`
- `risk_1..risk_M`
- `cost_1..cost_M`

### **QLTT dataset (`sample_QLTT_losses.csv`)**
- `lambda_id`
- `loss_1..loss_M`

---

# ▶️ Running Locally

```bash
pip install -r requirements.txt
jupyter notebook
```

---

# 🙌 Acknowledgments

Prepared for NeurIPS 2025 by  
**Amirmohammad Farzaneh**, **Sangwoo Park**, and **Osvaldo Simeone**.
