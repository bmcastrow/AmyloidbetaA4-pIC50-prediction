# 🧠 Amyloid-beta A4 potency Prediction

## Context

Alzheimer's disease is one of the most widespread neurodegenerative disorders, affecting millions worldwide. 
A key hallmark of Alzheimer's pathology is the accumulation of amyloid-beta plaques in the brain, which are thought to disrupt cell function, leading to cognitive decline and dementia. 

💊 Developing therapies to inhibit the aggregation of amyloid-beta or reduce its production has been a major focus of Alzheimer's research. In this project, the aim is to predict the inhibitory concentration (pIC50) of chemical compounds against Amyloid-beta A4, using both traditional machine learning and GenAI technology. By  predicting pIC50 values, the hope is to identify chemical compounds that could potentially inhibit the production or aggregation of amyloid-beta, providing a valuable starting point for therapeutic development.

## Table of Contents

- [Context](#context)
- [Table of contents](#table-of-contents)
- [Project overview](#project-overview)
  - [Strucure](#structure)
- [Development](#development)
  - [Prerequisites](#prerequisites)
  - [Requirements](#requirements)
- [Optuna insights](#optuna-insights)
- [Contribution Guidelines](#contribution-guidelines)

## Project overview

📜 Data: Exploration of the ChEMBL database, including the calculation of chemical descriptors using RDKit (Lipinski descriptors), the generation of molecular fingerprints with PaDEL-Descriptor, as well as preprocessing steps and exploratory data analysis (EDA)

🔬 ML Pipeline: A machine learning workflow leveraging molecular fingerprints as input features, with tree-based regressors optimized using Optuna 🧿 for efficient hyperparameter tuning and performance enhancement.

🤖 DL Pipeline: Deep learning method Using Hugging Face's ChemBERTa on SMILES combined with LoRA (Low-Rank Adaptation) for cost-effective fine-tuning with an adaptation for regression purposes (Loading...⌛⚠️) 

🔄 MLflow Integration: Experiments are tracked using MLFlow, in order to track model performance and hyperparameter trials that are optimzed using Bayesian optimization (Optuna for the ML Pipeline).

<br><br>

### Structure

bvkajhbvkajdbvkjabd

<img src="https://github.com/bmcastrow/AmyloidbetaA4-pIC50-prediction/blob/main/Design%20sem%20nome.jpg" alt="Banner" style="width:1000px; height:250px;">

## Development

### Prerequisites

- Software(macOS, Windows, Linux...)
- Conda or miniconda (with your environment)
- Python == 3.8.19

### Requirements

To ensure smooth execution and avoid dependency conflicts, this project uses two separate sets of requirements for different stages of the workflow:

### Data Requirements
Before processing and saving the dataset, install the dependencies listed in datarequirements.txt. This ensures the required tools and libraries for data handling are correctly installed.

Run the following command in the terminal:
```bash
pip install -r datarequirements.txt
```

### Training and Evaluation requirements
For the model training phase, create a new environment in the same script and install the dependencies listed in trainingrequirements.txt. Using a separate environment ensures no conflicts between libraries used in data preparation and those required for model training.

Run the following command in the terminal after activating your new environment:
```
pip install -r trainingrequirements.txt
```

## Optuna insights


## Contribution Guidelines

Steps to contribute to the master branch

- Clone the repository:
   ```bash
   git clone https://github.com/bmcastrow/AmyloidbetaA4-pIC50-prediction.git

Create an issue for each new bug/feature/update that you want to contribute. In the issue description, be as detailed as possible with what the expected inputs and outputs should be, and if possible what the process to solve the issue will be.
Assign someone, as well as apply the respective tags (documentation, enhacement, etc.)
On your local machine

If you haven't already, accept the invite to be a member of wri-dssg! Then clone the repository using git clone https://github.com/wri-dssg/policy-data-collector.git
If you're going to work on issue #69 which is about extracting text, then create a branch for that issue:
git checkout -b i69_text_extraction
Once work is done, commit and push:
git push --set-upstream origin i69_text_extraction
Back on Github

Once issue is solved, make a Pull Request (PR) on Github to merge to the master branch, and link the issue in the PR description and assign people to review. If possible, do one PR once a week to avoid merge conflicts.
If the PR gets approved and merged, you can close the issue and delete the branch!

<img src="https://github.com/bmcastrow/AmyloidbetaA4-pIC50-prediction/blob/main/Design%20sem%20nome.jpg" alt="Banner" style="width:1000px; height:250px;">

