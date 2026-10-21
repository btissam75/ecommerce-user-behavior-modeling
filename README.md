# Probabilistic and Reinforcement Learning Models for E-Commerce User Behavior

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/Code%20License-MIT-green.svg)](LICENSE)
[![Academic Project](https://img.shields.io/badge/Type-Academic%20Project-1f4e79)](#academic-context)

An academic study of e-commerce user behavior using the **Yoochoose / RecSys Challenge 2015** dataset. The project develops a progressive modeling framework ranging from Markov chains to hidden-state models, decision processes, reinforcement learning, and deep partially observable models.

> **Project scope:** the DTMC and CTMC chapters provide descriptive models estimated from Yoochoose sessions. The MDP, reinforcement-learning, and POMDP chapters are exploratory experiments conducted with modeled or simulated action effects and rewards.

## Academic context

| Field | Information |
|---|---|
| Institution | École Nationale Supérieure |
| Course | Apprentissage Probabiliste |
| Author | Btissam Arehal |
| Supervisor | Prof. Abdellatif El Afia |
| Academic year | 2025–2026 |
| Dataset | Yoochoose — RecSys Challenge 2015 |

## Research objective

The project studies how probabilistic and sequential models can represent the evolution of an anonymous e-commerce session and support exploratory marketing decisions.

The modeling progression is:

```text
Yoochoose sessions
       │
       ├── DTMC / CTMC ── descriptive transition and absorption analysis
       │
       ├── HMM ────────── latent-state sequence modeling
       │
       ├── MDP ────────── decision modeling under specified assumptions
       │
       ├── RL ─────────── value and policy learning in a modeled environment
       │
       └── POMDP ──────── partial observability and recurrent architectures
```

## Methods covered

- Discrete-Time Markov Chains (DTMC)
- Continuous-Time Markov Chains (CTMC)
- Hidden Markov Models (HMM)
- Policy Iteration and Value Iteration
- TD(0) and TD(λ)
- Q-Learning, SARSA, and R-Learning
- Classical and self-adaptive POMDPs
- Deep POMDP variants using GRU, LSTM, attention, and Transformer models

## Repository structure

```text
.
├── assets/figures/                 # Figures generated during the study
├── data/README.md                  # Dataset acquisition and placement notes
├── docs/                           # Methodology and project notes
├── notebooks/
│   ├── 01_dtmc_ctmc.ipynb
│   ├── 02_hmm.ipynb
│   ├── 03_mdp_policy_iteration.ipynb
│   ├── 04_value_iteration.ipynb
│   ├── 05_reinforcement_learning.ipynb
│   └── 06_pomdp_deep_pomdp.ipynb
├── report/
│   ├── academic_report.pdf
│   ├── presentation.pdf
│   └── report_source.tex
├── CITATION.cff
├── LICENSE
└── requirements.txt
```

## Main reported findings

For the five-state absorbing Markov representation used in the report, the estimated final purchase probabilities are approximately:

| Initial behavioral state | Purchase probability |
|---|---:|
| Browsing | 6.59% |
| Engaged | 9.48% |
| HighIntent | 16.36% |

These values describe the selected sample and the state definitions used in the notebooks. They should not be interpreted as universal conversion rates.

The decision and reinforcement-learning chapters demonstrate how policies such as advertising, promotion, or recommendation can be studied after defining action-dependent transitions and rewards. These experiments are scenario analyses rather than causal estimates from logged interventions.

## Installation

Clone the repository and create an isolated environment:

```bash
git clone <repository-url>
cd ecommerce-user-behavior-modeling
python -m venv .venv
```

Activate the environment, then install the dependencies:

```bash
pip install -r requirements.txt
jupyter lab
```

The original notebooks were developed in Google Colab and currently contain Google Drive paths. Configure the dataset paths in the relevant loading cells before execution.

## Dataset

The raw Yoochoose dataset is **not redistributed in this repository**. Consult [`data/README.md`](data/README.md) for the expected files and directory conventions.

Expected source files:

```text
yoochoose-clicks.dat
yoochoose-buys.dat
```

Users are responsible for obtaining the dataset from an authorized source and complying with its terms of use.

## Notebooks

| Notebook | Purpose |
|---|---|
| `01_dtmc_ctmc.ipynb` | Discrete- and continuous-time transition modeling |
| `02_hmm.ipynb` | Discrete and continuous HMM experiments |
| `03_mdp_policy_iteration.ipynb` | MDP formulation and Howard Policy Iteration |
| `04_value_iteration.ipynb` | Value Iteration and discount-factor comparison |
| `05_reinforcement_learning.ipynb` | TD, Q-Learning, SARSA, and R-Learning |
| `06_pomdp_deep_pomdp.ipynb` | Classical, deep, and non-Markovian POMDP prototypes |

## Reports

- [`report/academic_report.pdf`](report/academic_report.pdf) — complete academic report in French
- [`report/presentation.pdf`](report/presentation.pdf) — project presentation
- [`report/report_source.tex`](report/report_source.tex) — archived LaTeX source supplied with the project

## Scientific interpretation

This repository should be read as an academic modeling study:

- DTMC and CTMC results are descriptive estimates under explicit state definitions.
- HMM experiments investigate hidden-state modeling.
- Action effects and rewards in MDP/RL experiments are modeling assumptions.
- Deep POMDP components are exploratory research prototypes.
- No causal uplift, production readiness, or guaranteed commercial performance is claimed.

See [`docs/METHODOLOGY.md`](docs/METHODOLOGY.md) for additional details.

## Reproducibility notes

- The notebooks retain their original saved outputs.
- Raw data are intentionally excluded from version control.
- Some experiments require substantial memory or a CUDA-capable runtime.
- Randomized experiments may require explicit seeds for exact reproduction.
- The repository preserves the original academic implementation; restructuring does not alter model code or reported results.

## Ethical and privacy considerations

The study uses anonymous session-level interaction data. No attempt should be made to identify individual users. Any operational deployment should include privacy, consent, fairness, budget, and intervention-risk reviews.

## Citation

If this repository supports academic work, cite it using the metadata in [`CITATION.cff`](CITATION.cff).

## License

The source code in this repository is released under the [MIT License](LICENSE). The dataset, third-party papers, and referenced external materials remain subject to their own licenses and terms.

