# 🧠 Amyloid-beta A4 potency Prediction

## 📝 Contextual Introduction

Alzheimer's disease is one of the most widespread neurodegenerative disorders, affecting millions worldwide. 
A key hallmark of Alzheimer's pathology is the accumulation of amyloid-beta plaques in the brain, which are thought to disrupt cell function, leading to cognitive decline and dementia. 

💊 Developing therapies to inhibit the aggregation of amyloid-beta or reduce its production has been a major focus of Alzheimer's research. In this project, the aim is to predict the inhibitory concentration (pIC50) of chemical compounds against Amyloid-beta A4, using both traditional machine learning and GenAI technology. By accurately predicting pIC50 values, the hope is to identify chemical compounds that could potentially inhibit the production or aggregation of amyloid-beta, providing a valuable starting point for therapeutic development.

## 📁 Repository Overview

📜 Data: ChEMBL database exploration containing bioactivity data, chemical descriptors calculated using RDKit (including Lipinski descriptors), PaDEL-Descriptor to generate molecular fingerprints, preprocessing steps and EDA.

🔬 ML Pipeline: Machine learning approach using molecular fingerprints, with models tuned using Optuna for hyperparameter optimization.

🤖 DL Pipeline: Deep learning method Using Hugging Face's ChemBERTa on SMILES combined with LoRA (Low-Rank Adaptation) for cost-effective fine-tuning.

📊 MLflow Integration: Experiments are tracked using MLFlow, in order to track model performance and hyperparameter trials.

