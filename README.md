# 🧠 Causal Inference in Python: DAGs, Bayesian Networks & Propensity Score Matching


### Short Description of the project:

> **A practical Causal Inference project implementing Pearl's causal framework, DAGs, Bayesian Networks, backdoor adjustment, propensity score estimation, treatment-control matching, and Average Treatment Effect (ATE) using Python and bnlearn.**

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Causal Inference](https://img.shields.io/badge/Causal-Inference-8A2BE2?style=for-the-badge)
![Bayesian Networks](https://img.shields.io/badge/Bayesian-Networks-FF6F00?style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-success?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</p>

---

# 📖 Project Overview

This project provides a practical introduction to **Causal Inference** using Python, focusing on the difference between **correlation and causation** in observational data.

Unlike traditional machine learning models that primarily focus on predicting outcomes, causal inference attempts to answer a deeper question:

> **"What would happen to the outcome if we actively changed the treatment or condition?"**

The project uses the classic **Sprinkler dataset** to study the relationship between weather conditions, sprinkler usage, and wet grass. It demonstrates how causal relationships can be represented using **Directed Acyclic Graphs (DAGs)** and analyzed through **Bayesian Networks**.

The project also explores **Propensity Score Matching (PSM)** as a second approach for estimating causal effects by creating comparable treatment and control groups.

By combining graphical causal modeling, probabilistic reasoning, and matching-based methods, the project demonstrates a practical workflow for estimating treatment effects from observational data.

---

# 🎯 Aim

The primary objectives of this project are to:

- Understand the fundamentals of **Causal Inference**.
- Distinguish between **correlation and causation**.
- Represent causal relationships using **Directed Acyclic Graphs (DAGs)**.
- Build and analyze **Bayesian Networks**.
- Identify and handle **confounding variables**.
- Understand the **Backdoor Criterion and Backdoor Adjustment**.
- Perform causal reasoning using interventions.
- Calculate **Propensity Scores**.
- Match treated and control observations.
- Estimate the **Average Treatment Effect (ATE)**.
- Understand how causal inference differs from conventional predictive modeling.

---

# 💡 Why Causal Inference?

Traditional machine learning generally asks:

```text
"What is likely to happen?"
```

Causal inference asks:

```text
"What will happen if we change something?"
```

For example, if sprinkler usage and wet grass are correlated, we cannot immediately conclude that the sprinkler caused the grass to become wet.

Weather conditions such as **cloudiness and rain** may influence both variables.

Therefore, causal analysis requires us to consider the underlying causal structure and potential confounding factors before estimating the true treatment effect.

---

# ✨ Project Highlights

✅ Causal Inference Fundamentals

✅ Correlation vs Causation

✅ Directed Acyclic Graphs (DAGs)

✅ Bayesian Network Construction

✅ Conditional Probability Analysis

✅ Probabilistic Inference

✅ Confounding Variable Identification

✅ Backdoor Adjustment

✅ Intervention-Based Causal Reasoning

✅ Propensity Score Estimation

✅ Treatment-Control Group Analysis

✅ Propensity Score Matching

✅ Average Treatment Effect (ATE)

✅ Comparison of Causal Inference Approaches

---

# 🔬 Causal Problem Formulation

The project considers:

```text
Treatment  →  Sprinkler

Outcome    →  Wet Grass

Confounder →  Cloudy
```

Weather conditions can affect sprinkler usage and grass wetness, making it important to account for these variables when estimating the causal effect.

The project therefore focuses on estimating:

```text
Effect of Sprinkler → Wet Grass
```

while accounting for relevant confounding relationships.

---

# 🔗 Directed Acyclic Graph (DAG)

The causal structure is represented using a **Directed Acyclic Graph**, allowing relationships between variables to be explicitly modeled.

A simplified representation is:

```text
             Cloudy
             /    \
            ▼      ▼
        Sprinkler  Rain
            │        │
            ▼        ▼
                 Wet Grass
```

The DAG provides a visual representation of the assumptions about how the variables influence one another.

This is important because causal inference depends not only on observed data but also on the assumed causal structure.

---

# 🌐 Bayesian Network

The project uses a **Bayesian Network** to represent probabilistic dependencies between variables.

The Bayesian Network allows the model to:

- Represent dependencies between variables
- Learn probability distributions
- Perform conditional probability queries
- Analyze relationships between treatment and outcome
- Support causal reasoning

This provides a bridge between **probabilistic modeling** and **causal analysis**.

---

# 🚪 Backdoor Adjustment

One of the important concepts explored in the project is **Backdoor Adjustment**.

A simple observational comparison between:

```text
Sprinkler = ON
```

and

```text
Sprinkler = OFF
```

may produce a biased estimate because weather conditions can influence the observed outcome.

Backdoor adjustment addresses this issue by conditioning on an appropriate confounding variable before estimating the causal effect.

Conceptually:

```text
Observed Association
        │
        ▼
Identify Confounder
        │
        ▼
Block Backdoor Path
        │
        ▼
Estimate Causal Effect
```

This demonstrates why causal modeling is more than simply calculating correlations.

---

# ⚖️ Propensity Score Matching

The project also implements **Propensity Score Matching (PSM)**.

Propensity Score Matching is a technique used with observational data to create more comparable treatment and control groups.

The process involves:

```text
Identify Treatment & Control
            │
            ▼
Estimate Propensity Scores
            │
            ▼
Find Similar Observations
            │
            ▼
Match Treatment & Control
            │
            ▼
Compare Outcomes
            │
            ▼
Estimate Treatment Effect
```

The goal is to reduce differences between the treatment and control groups caused by observed confounding variables.

---

# 🎯 Average Treatment Effect (ATE)

The **Average Treatment Effect (ATE)** represents the average causal impact of a treatment on an outcome across the population being studied.

Conceptually:

```text
ATE = E[Y | Treatment = 1]
      -
      E[Y | Treatment = 0]
```

The project demonstrates how treatment effects can be estimated using causal modeling and propensity-score-based matching.

---

# ⚙️ Complete Workflow

```text
                    CAUSAL INFERENCE
                           │
                           ▼
                    Dataset Analysis
                           │
                           ▼
                  Identify Variables
                           │
                           ▼
             Define Treatment & Outcome
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
       DAG & Bayesian Network    Propensity Score
              │                       Matching
              ▼                         │
     Identify Confounders               ▼
              │                  Treatment-Control
              ▼                       Analysis
     Define Causal Structure             │
              │                          ▼
              ▼                   Estimate Propensity
      Backdoor Adjustment                 Scores
              │                          │
              ▼                          ▼
      Causal Probability            Match Similar
          Analysis                   Observations
              │                          │
              ▼                          ▼
      Estimate Intervention        Compare Outcomes
              │                          │
              └────────────┬─────────────┘
                           ▼
                  Calculate ATE
                           │
                           ▼
                  Causal Interpretation
```

---

# 🧪 Methodology

## 1️⃣ Data Understanding

The dataset is examined to understand the variables involved in the causal system and identify the treatment, outcome, and potential confounders.

---

## 2️⃣ Causal Graph Construction

A DAG is constructed to represent the assumed causal relationships between weather conditions, sprinkler activity, rain, and grass wetness.

---

## 3️⃣ Bayesian Network Analysis

A Bayesian Network is used to represent probabilistic dependencies and perform inference over the variables.

---

## 4️⃣ Confounding Analysis

Potential confounding relationships are identified to understand why direct observational comparisons may not represent the true causal effect.

---

## 5️⃣ Backdoor Adjustment

The appropriate confounding variable is incorporated into the causal analysis to block non-causal paths and estimate the treatment effect more reliably.

---

## 6️⃣ Propensity Score Matching

Propensity scores are estimated and observations from treatment and control groups are matched based on their similarity.

---

## 7️⃣ Treatment Effect Estimation

The outcomes of matched observations are compared to estimate the **Average Treatment Effect (ATE)**.

---

# 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Data Manipulation | Pandas, NumPy |
| Causal Modeling | bnlearn |
| Bayesian Networks | Bayesian Networks, CPDs |
| Statistical Analysis | SciPy |
| Visualization | Matplotlib |
| Development Environment | Jupyter Notebook |

---

# 📊 Results

The project demonstrates two complementary approaches for understanding and estimating causal effects from observational data.

### 🔗 DAG & Bayesian Network Approach

The causal structure is explicitly represented using a DAG and Bayesian Network. This makes it possible to reason about dependencies, confounding variables, and intervention-based effects.

### ⚖️ Propensity Score Matching Approach

Propensity Score Matching creates comparable treatment and control observations before comparing their outcomes. This provides an alternative approach for estimating treatment effects when randomized experimental data is unavailable.

### 🎯 Overall Insight

The project demonstrates that **observed correlation alone is not sufficient to establish causality**. Incorporating causal assumptions, confounding analysis, and treatment-control comparison provides a stronger framework for understanding the effect of an intervention.

---

# 📚 Key Concepts

The project provides practical exposure to:

- 🧠 Causal Inference
- 🔗 Directed Acyclic Graphs
- 🌐 Bayesian Networks
- 🔍 Confounding Variables
- 🚪 Backdoor Adjustment
- 🎯 Causal Interventions
- 📊 Conditional Probability
- ⚖️ Propensity Scores
- 🔄 Treatment-Control Matching
- 📈 Average Treatment Effect
- 🔬 Observational Data
- 🧮 Probabilistic Inference

---

# 📂 Repository Structure

```text
📦 Causal-Inference-Python
│
├── 📁 notebooks
│   ├── Causal_Inference_DoWhy_Example.ipynb
│   └── Causal_Inference_MatchingExample.ipynb
│
├── 📁 data
│   └── sprinkler_dataset.csv
│
├── 📁 images
│   ├── causal_dag.png
│   ├── bayesian_network.png
│   ├── propensity_scores.png
│   ├── treatment_control.png
│   └── causal_effect.png
│
├── requirements.txt
├── LICENSE
└── README.md
```

---

# 🚀 Future Improvements

The project can be extended further by implementing more advanced causal machine learning techniques:

- 🔄 Inverse Probability Weighting (IPW)
- 🌳 Causal Forests
- 🤖 Causal Machine Learning
- 📊 Doubly Robust Estimation
- 🧪 Sensitivity Analysis
- 🔬 Instrumental Variable Methods
- 📈 Heterogeneous Treatment Effect Analysis
- 🌐 Application to Real-World Healthcare & Business Data
- 🚀 Interactive Causal Analysis Dashboard

---

# 🎓 Learning Outcomes

Through this project, you will gain practical understanding of:

- Causal vs Correlational Analysis
- DAG-based causal reasoning
- Bayesian Network modeling
- Conditional probability and inference
- Confounding and causal bias
- Backdoor adjustment
- Intervention-based reasoning
- Propensity Score Matching
- Treatment and control groups
- Average Treatment Effect estimation
- Causal analysis of observational datasets

---

# 💼 Real-World Applications

The techniques demonstrated in this project have applications across multiple domains:

### 🏥 Healthcare
Estimating whether a treatment or medication actually improves patient outcomes.

### 💰 Business & Marketing
Measuring whether a marketing campaign causes an increase in sales.

### 🎓 Education
Studying the causal impact of educational interventions on student performance.

### 🏦 Finance
Analyzing the impact of financial policies or interventions.

### 🤖 AI & Machine Learning
Building models that move beyond prediction toward **causal reasoning and decision-making**.

---

# 📌 Project Significance

This project demonstrates an important transition from traditional predictive machine learning toward **causal reasoning**.

While predictive models answer:

> **"What is likely to happen?"**

causal models attempt to answer:

> **"What happens if we intervene?"**

Understanding this distinction is particularly important for modern **AI/ML systems, decision-making models, experimentation, policy analysis, and responsible AI**.

---

# 👨‍💻 Author

**Ambuj Tripathi**

🎓 Pre-Final Year B.Tech (Electronics & Computer Science)

🤖 Aspiring AI/ML Engineer

💡 **Interests:** Machine Learning • NLP • Deep Learning • LLMs • Causal AI

---

⭐ **If you found this project useful, consider giving it a star!**
