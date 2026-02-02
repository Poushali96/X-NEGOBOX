

# X-NegoBox

**Explainable Privacy-Budget Negotiation for Secure Peer-to-Peer Energy Data Exchange**

This repository contains a **reference implementation and experimental code** for **X-NegoBox**, an explainable and adaptive privacy-budget negotiation framework for secure peer-to-peer energy data sharing in decentralized energy systems.

X-NegoBox enables **context-aware, utility-preserving negotiation** of differential-privacy (DP) budgets while keeping all raw data confined to a **prosumer-controlled Private DataBox**. The system replaces static allow/deny policies with adaptive negotiation and transparent explanations.

---

## 📌 Key Contributions

* **APBNP (Autonomous Privacy-Budget Negotiation Protocol)**
  Adaptive, per-request DP budget allocation based on sensitivity, trust, purpose, and remaining budget.
* **X-Contract (Explainable Agreement Layer)**
  Human- and machine-readable explanations for approval, rejection, and counter-offers.
* **Run-Code-Not-Data Execution Model**
  Requester code executes locally inside a sandbox; only DP-sanitized outputs are released.
* **Distributed Authorization via Threshold Secret Sharing (TSS)**
  Prevents unilateral or premature data release.
* **Extensive Experimental Evaluation**
  Cross-dataset benchmarks, synthetic smart-grid simulations, and privacy-budget sweep studies.

---

## 📁 Repository Structure

```
.
├── NEGOBOX.ipynb        # Core APBNP negotiation logic and experiments
├── x_nego_test.ipynb   # X-Contract explanations and sandbox behavior
├── data/               # (Optional) Public or synthetic datasets
├── figures/            # Generated plots used in the paper
└── README.md
```

---

## ⚙️ Requirements

* Python ≥ 3.9
* NumPy
* SciPy
* Pandas
* Matplotlib
* Jupyter Notebook

Install dependencies:

```bash
pip install numpy scipy pandas matplotlib jupyter
```

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone https://github.com/<your-org>/x-negobox.git
cd x-negobox
```

2. Launch Jupyter:

```bash
jupyter notebook
```

3. Run notebooks in order:

* `NEGOBOX.ipynb` – APBNP negotiation and evaluation
* `x_nego_test.ipynb` – X-Contract explanations and sandbox validation

All experiments are deterministic and replay identical request streams for reproducibility.

---

## 🔍 What the Code Demonstrates

* Adaptive DP budget selection via one-dimensional optimization
* Sensitivity, trust, and purpose-aware negotiation
* Approval, rejection, and counter-offer generation
* Explainable decision traces aligned with negotiation logic
* Stable acceptance behavior across heterogeneous datasets
* Bounded cumulative privacy loss under repeated interactions

---

## 🧪 Experimental Setup

* Real and proxy-real energy datasets (e.g., UCI Household, national load data)
* Synthetic smart-grid simulation with 100 heterogeneous prosumers
* Privacy-budget sweep experiments over varying initial budgets
* Baseline comparison against fixed-ε differential privacy

---

## 📖 Reference

If you use this code, please cite the corresponding paper:

> **X-NegoBox: An Explainable Privacy-Budget Negotiation Framework for Secure Peer-to-Peer Energy Data Exchange**
> P. Sengupta, S. Maharjan, F. Eliassen, Y. Zhang
> *IEEE ICCCN (under review)*

---

## 🔐 Ethics & Reproducibility

* Raw data never leaves the local execution environment
* Only differentially private outputs are released
* All evaluations use public or synthetic data
* Fixed mappings and deterministic request streams ensure reproducibility

---

## 📬 Contact

For questions or collaboration:

* **Poushali Sengupta** – University of Oslo
* Email: [poushals@uio.no](mailto:poushals@uio.no)


