# Multi‑Model Leader Correction for Algorithmic Trading in Forex Market

## 📑 Project Overview
This repository contains the full implementation, datasets, and results of my MSc thesis:

> **"Multi‑Model Leader Correction Consensus Approach for Developing Algorithmic Trading Systems in the Forex Market"**  
> Department of Data Science, Faculty of Mathematical Sciences, Ferdowsi University of Mashhad.

The research develops a dynamic **Leader Correction (LC)** consensus framework that selects the best‑performing predictive trading model in each sliding window based on recent performance and adjusts trading signals to maximize profit and reduce risk. This approach combines statistical technical indicators with data‑driven optimization for enhanced trading robustness.

---

## 🎯 Objectives
- **Maximize Net Profit** in USD for selected currency pairs.
- **Increase Profit‑to‑Risk Ratio** by switching leaders dynamically.
- **Reduce Relative Drawdown** compared to single‑model and static consensus.
- Ensure **robust generalization** to unseen test datasets.

---

## 🛠 Metaheuristics Used
Four metaheuristic optimization algorithms were implemented and compared:
1. Genetic Algorithm (**GA**)
2. Particle Swarm Optimization (**PSO**)
3. Whale Optimization Algorithm (**WOA**)
4. Seagull Optimization Algorithm (**SBO**)

Each algorithm optimizes parameters:
- `n_SMA` – Simple Moving Average window size
- `d11` – PPPL threshold parameter
- `SL` – Stop Loss

- `TP` – Take Profit
- 📊 Outputs & Results
All generated results can be found in the `/output/` folder.  
They include Excel files summarizing:

- **Optimal_Parameters.xlsx** – Optimal values for `n_SMA`, `d11`, `SL`, `TP` obtained via GA, WOA, PSO, SBO.
- **Performance_Comparison.xlsx** – Net Profit, Profit/Risk ratio, and Max Drawdown before and after optimization.
- **Leader_Correction_Summary.xlsx** – Performance of dynamic leader switching across sliding windows.

> GitHub cannot preview `.xlsx` files online. Download them locally to view in Excel or LibreOffice.

📂 Repository Structure
/data → Raw and preprocessed datasets for EURUSD, USDCHF, etc.
/src → Source code for Leader Correction models and optimization algorithms.
/output → Generated results (Excel) from experiments.
## 🚀 How to Run
Clone the repository:
git clone https://github.com/n1e9g9a9rna/ForexLeaderCorrection_GA_WOA_PSO_SBO.git
Navigate into the project folder:
cd ForexLeaderCorrection_GA_WOA_PSO_SBO
Install dependencies:

pip install -r requirements.txt
Run the desired optimization algorithm (example: GA Leader Correction):
python src/ga_leader_correction.py
The results will be generated in the /output/ folder as .xlsx 




