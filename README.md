# Specification Explicitness and Failure Structure in LLM Coding
The artifact includes all materials necessary to **reproduce the results**, including datasets, scripts, and analysis code.

## Abstract
LLMs turn natural-language descriptions into executable code, making requirements specifications directly operational. When specifications are incomplete, missing assumptions and constraints are immediately translated into incorrect behavior, turning a latent requirements problem into a direct source of system failure. We present a controlled empirical study that treats specification explicitness as a first-class variable. Participants implemented software tasks with an LLM under three specifications: emergent, structured, and constraint-complete. We evaluate correctness using hidden tests, analyze failure modes, measure regression under requirement change, and assess developer calibration.
Our results show that specification explicitness has a strong but non-uniform effect. Constraint-complete specifications significantly reduce failures and suppress dominant error classes such as invariant violations and assumption injection, while even a lightweight structure eliminates tie-breaking errors. However, explicitness does not monotonically reduce regressions; instead, it reshapes the regression profile, trading off between frequency and severity. We further find that not all requirement content contributes equally to correctness. Finally, explicit specifications substantially improve calibration, reducing overconfidence from 34.38\% to 5.21\% in Phase~I and to 4.35\% after the requirement change. 
These findings show that specification explicitness is a key control dimension in LLM-assisted development, shaping not only correctness but also failure structure, robustness to change, and developer judgment.


---

## Purpose
The goal of this artifact is to:
- Enable **reproducibility** of experimental results  
- Provide **transparent access** to data and analysis  
- Support **independent validation** of findings  

---

##  Repository Structure

├── Datasets/ # Datasets used in the study
├── Extraction_Schema/ # Schema used to extract data from paper surveys using Airparser
├── Hidden_test/ # contains hidden tests used in the experiments. 
├── analysis/ # Reproducibility for the results
├── Failure_mode_mapping/  # mapping schema for failure modes covered by hidden tests
├──implementations/ #contains code implemented by the participants
| ├──Phase1_codes.zip
| ├──Phase2_codes.zip
├──surveys # contains survey templates used to gather data from participants
| ├──Phase1 # contains prediction sheet 
| ├──Phase2 # contains change rationale and impact predictions
| ├──demographics # contains demographic survey, data, and analysis
└── README.md # This file
