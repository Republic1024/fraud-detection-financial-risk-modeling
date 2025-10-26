
# 🧠 Fraud Detection and Financial Risk Modeling
**End-to-end fraud detection system for transactional data (13M+ records) integrating EDA, feature engineering, LightGBM modeling, and SHAP interpretability.**

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)]()
[![LightGBM](https://img.shields.io/badge/LightGBM-4.x-green.svg)]()
[![SHAP](https://img.shields.io/badge/SHAP-ExplainableAI-orange.svg)]()
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)]()

---

## 📘 Overview
This project builds a **data-driven fraud detection pipeline** capable of identifying suspicious financial transactions from over **13 million records**.  
It combines **exploratory data analysis**, **feature engineering**, **imbalanced learning**, and **interpretable machine learning** to deliver actionable business insights.

![img_3.png](img_3.png)
![img_2.png](img_2.png)
---

## ⚙️ Workflow Architecture
```

Data Loading → EDA → Feature Engineering → Class Balancing →
LightGBM Training → Threshold Optimization → SHAP Interpretability → Risk Report

```
![img_1.png](img_1.png)
![img.png](img.png)
### 🧩 Core Steps
| Stage | Description |
|-------|--------------|
| **Data Preparation** | Cleaned and merged `transactions`, `users`, `cards`, and `MCC` data (13M+ rows). |
| **EDA & Visualization** | Distribution, outlier, and geographic/industry-level fraud analysis. |
| **Feature Engineering** | Constructed 20+ numerical, categorical, and time-based features (`amount_log`, `is_refund`, `hour`, `mcc_desc`, etc.). |
| **Class Balancing** | Undersampling strategy (10× ratio) to stabilize LightGBM training. |
| **Model Training** | Tuned LightGBM (GBDT) with early stopping and AUC optimization. |
| **Explainability (SHAP)** | Interpreted feature contributions globally and locally (fraud driver visualization). |
| **Threshold Tuning** | Optimized precision–recall trade-off with decision curve visualization. |
| **Business Application** | Exported Top-200 high-risk transactions for manual verification. |

---

## 📊 Model Performance
| Metric | Value |
|:--|--:|
| **AUC (Validation)** | 0.9718 |
| **Precision** | 0.0379 |
| **Recall** | 0.4941 |
| **F1 Score** | 0.0704 |
| **Detection Coverage** | 2.28% of transactions flagged as high risk |

**Interpretation:**  
- The model correctly detects ~49.4% of all fraud cases with only 2.28% alerts —  
  efficient enough for business audit workflows with limited human verification capacity.

---

## 🌍 Explainability
- **Global Importance:** `amount_log`, `hour`, `mcc_desc`, and `client_mean` drive fraud prediction.  
- **Local Explanation:** SHAP force plots reveal how transaction timing and amount deviations trigger risk alerts.  
- **Interpretability Goal:** bridge **model confidence** and **financial analyst reasoning**.

---

## 📦 Exported Deliverables
| Output File | Description |
|--------------|-------------|
| `main.ipynb` | Full pipeline notebook with 19 modular cells |
| `main.html` | Rendered analysis report |
| `high_risk_transactions_top200.csv` | Top 200 suspicious transactions ranked by fraud probability |
| `.gitignore` | Excludes large data files (JSON/CSV over 100 MB) |

---

## 🧰 Tech Stack
- **Python 3.10 + Pandas + NumPy**
- **LightGBM 4.x** (with callbacks for early stopping & AUC logging)
- **Matplotlib / Seaborn** (visual analytics)
- **SHAP 0.43.0** (explainable AI)
- **Scikit-learn 1.4+** (precision-recall & threshold tuning)

---

## 💡 Business Impact
This project demonstrates a **scalable, interpretable fraud detection framework** ready for integration into financial risk control systems.  
By combining model precision with SHAP-based transparency, it allows compliance teams to **prioritize high-value alerts** and **rationalize AI decisions** to stakeholders.

---

## 📈 Author
**Yao Wu** (GitHub: [Republic1024](https://github.com/Republic1024))  
Westlake University · Research Assistant (AI & Data Science)  
📚 Projects: [HierCVAE](https://doi.org/10.48550/arXiv.2508.18922), [J6 Framework](https://github.com/Republic1024/J6-Prompt-Optimization)

---

## 🪪 License
This project is released under the [MIT License](LICENSE).

---
```

