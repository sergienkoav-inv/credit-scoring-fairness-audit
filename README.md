# Statistical Verification and Ethical Audit of Credit Scoring AI Models

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Reproducibility](https://img.shields.io/badge/Open%20Science-Reproducible-brightgreen.svg)

## Overview
This repository contains the reproducible experimental pipeline, statistical hypothesis testing scripts, and algorithmic fairness mitigation modules developed within the Master's research at **Pryazovskyi State Technical University (PSTU)**, Department of Computer Science.

The project evaluates **XGBoost** against a **Logistic Regression** baseline across 30 cross-validation folds ($N = 1000$) and resolves subgroup Recall disparities using post-processing **Threshold Adjustment**.

## Key Experimental Results

| Model / Configuration | Mean F1-score | 95% CI | Disparate Impact | Subgroup $\Delta$Recall |
| :--- | :---: | :---: | :---: | :---: |
| Logistic Regression (Baseline) | 0.7434 ± 0.0315 | [0.7317; 0.7552] | 0.8412 | 0.0890 |
| XGBoost (Standard $\tau=0.50$) | 0.8066 ± 0.0261 | [0.7969; 0.8163] | 1.0968 | 0.1894 |
| **XGBoost + Threshold Adjustment** | **0.8012 ± 0.0274** | **[0.7910; 0.8114]** | **0.9640** | **0.0245** |

## Installation & Usage

1. Clone the repository:
   ```bash
   git clone [https://github.com/ivanenko-cs/credit-scoring-fairness-audit.git](https://github.com/ivanenko-cs/credit-scoring-fairness-audit.git)
   cd credit-scoring-fairness-audit
   ```
2. Install pinned dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run statistical verification and fairness audit:
   ```bash
   python src/stats_evaluation.py
   python src/fairness_mitigation.py
   ```

## Citation
If you use this codebase or methodology in your research, please cite:
```bibtex
@inproceedings{ivanenko2026credit,
  author    = {Ivanenko, Oleksandr and Dehtiarova, Larysa},
  title     = {Statistical Verification and Algorithmic Fairness Mitigation of Gradient Boosting Models in Credit Scoring Tasks},
  booktitle = {Proceedings of the PSTU Student & Master Scientific Conference},
  year      = {2026},
  address   = {Dnipro, Ukraine}
}
```

## AI Disclosure
Generative AI (Anthropic Claude 3.5 Sonnet) was used solely for English language polishing and Markdown table formatting in accordance with the PSTU Responsible AI Policy (Yellow Level). All code logic, statistical computations, and conclusions were authored and verified by the researchers.

## License
This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
