# 🧠 Causal Inference in Python: DAGs, Bayesian Networks & Propensity Score Matching


### Short Description of the project:

> **A practical Causal Inference project implementing Pearl's causal framework, DAGs, Bayesian Networks, backdoor adjustment, propensity score estimation, treatment-control matching, and Average Treatment Effect (ATE) using Python and bnlearn.**


<p align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Causal Inference](https://img.shields.io/badge/Causal-Inference-purple?style=for-the-badge)
![Bayesian Networks](https://img.shields.io/badge/Bayesian-Networks-orange?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</p>

---

## 📖 Project Overview

This project explores practical **Causal Inference** using the classic *Sprinkler* dataset and demonstrates two complementary approaches to estimating treatment effects.

The first notebook applies **Pearl's causal inference framework** using a **Directed Acyclic Graph (DAG)** and Bayesian Network to model causal relationships between weather conditions, sprinkler usage, and wet grass. The causal effect of the sprinkler is estimated using **backdoor adjustment** and the **Average Treatment Effect (ATE)**.

The second notebook demonstrates **Propensity Score Matching**, beginning with treatment-control group analysis, estimating propensity scores based on the confounding variable, matching treated observations with comparable control observations, and calculating the resulting ATE.

Together, the notebooks provide a practical introduction to moving from **observational data and statistical associations toward causal effect estimation**.

---

## 🎯 Aim

The primary objectives of this project are to:

- Understand the fundamentals of Causal Inference
- Represent causal assumptions using DAGs
- Identify and handle confounding variables
- Estimate causal effects using Pearl's framework
- Calculate propensity scores
- Match treated and control observations
- Estimate the Average Treatment Effect (ATE)

---

## ✨ Project Highlights

✅ Directed Acyclic Graph (DAG) Construction  
✅ Bayesian Network Modeling  
✅ Maximum Likelihood Parameter Learning  
✅ Causal Inference using Pearl's Framework  
✅ Backdoor Adjustment  
✅ Confounding Variable Analysis  
✅ Conditional Probability Inference  
✅ Propensity Score Estimation  
✅ Treatment-Control Matching  
✅ Average Treatment Effect (ATE) Estimation  

---

## ⚙️ Workflow

```text
                    CAUSAL INFERENCE
                           │
             ┌─────────────┴─────────────┐
             │                           │
        Pearl's Framework          Propensity Matching
             │                           │
             ▼                           ▼
      Define Causal DAG           Analyze Treatment/
             │                    Control Groups
             ▼                           │
      Bayesian Network                  ▼
             │                    Calculate Propensity
             ▼                         Scores
      Learn Parameters                    │
             │                           ▼
             ▼                    Match Similar Units
    Identify Confounders                  │
             │                           ▼
             ▼                    Estimate Treatment
     Backdoor Adjustment                  Effect
             │
             ▼
       Calculate ATE
