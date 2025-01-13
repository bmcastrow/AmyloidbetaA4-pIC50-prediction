# 🧠 Amyloid-beta A4 potency Prediction

<img src="https://github.com/bmcastrow/AmyloidbetaA4-pIC50-prediction/blob/main/BrainCell.jpg" alt="Banner" style="width:1000px; height:250px;">

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
    - [MLFlow](#mlflow)
- [Optuna insights using MLFlow](#optuna-insights-using-mlflow)
  - [Runs](#runs)
  - [Experiment type](#experiment-type)
  - [LearningRate influence in HistGradientBoostingRegressor](#learningrate-influence-in-histgradientboostingregressor)
  - [Hyperparameter influence in RandomForestRegressor](#hyperparameter-influence-in-randomrorestregressor)
- [Contribution Guidelines](#contribution-guidelines)

## Project overview

📜 Data: Exploration of the ChEMBL database, including the calculation of chemical descriptors using RDKit (Lipinski descriptors), the generation of molecular fingerprints with PaDEL-Descriptor, as well as preprocessing steps and exploratory data analysis (EDA)

🔬 ML Pipeline: A machine learning workflow leveraging molecular fingerprints as input features, with tree-based regressors optimized using Optuna 🧿 for efficient hyperparameter tuning and performance enhancement.

🤖 DL Pipeline: Deep learning method Using Hugging Face's ChemBERTa on SMILES combined with LoRA (Low-Rank Adaptation) for cost-effective fine-tuning with an adaptation for regression purposes (Loading...⌛⚠️) 

🔄 MLflow Integration: Experiments are tracked using MLFlow, in order to track model performance and hyperparameter trials that are optimzed using Bayesian optimization (Optuna for the ML Pipeline).

### Structure

bvkajhbvkajdbvkjabd

## Development

### Prerequisites

- Software(macOS, Windows, Linux...)
  - If using macOS, must have homebrew installed
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
```bash
pip install -r trainingrequirements.txt
```

#### MlFlow
The step "***Training and Evaluation requirements***", was made in order for MLFlow to work correctly. For some reason (reported in several places online) ```port 5000``` sometimes doesn't work. With that in mind it is advised to change to another (i.e. ```port 8080```).

## Optuna insights using MLFlow
Optuna and MLflow offer a powerful combination for hyperparameter optimization and experiment tracking. Optuna's visualization capabilities enable deep insights into the influence of hyperparameters on model performance, while MLflow organizes experiments, making it easier to compare different runs. Below are examples of visualizations generated during the optimization process:

### Runs
<img src="Optuna%20ft.%20MLFlow/mlflow_runorg.png" alt="MLflow Run Organization" style="height:200px;">

### Experiment type
![Experiment Type Overview](Optuna%20ft.%20MLFlow/experiment_type.png)

### i.e (LearningRate influence in HistGradientBoostingRegressor)
![Hyperparameter Influence on R²](Optuna%20ft.%20MLFlow/hyperparameter_influence_r2.png)

### Hyperparameter influence in RandomForestRegressor
![Random Forest Hyperparameter Influence](Optuna%20ft.%20MLFlow/RandomForest_hyperparameter_influence.png)


## Contribution Guidelines

Steps to contribute to the master branch

- [Git](https://git-scm.com/) installed on your local machine.
- (Optional) Direct collaborator access to this repository, otherwise you’ll contribute via your own fork.

1. **Check existing issues**: See if the feature request or bug is already reported.  
2. **Open a new issue** if one does not exist:
   - Provide a clear title (e.g., “Fix data parsing in main script”).
   - Describe the problem, enhancement, or feature request in detail.
   - Assign yourself or someone else if appropriate.
   - Add relevant labels (e.g., `bug`, `enhancement`, `documentation`).
  
---

- Clone the repository:
   ```bash
   git clone https://github.com/bmcastrow/AmyloidbetaA4-pIC50-prediction.git

- Create a new descriptive branch with issue number (i.e: i18_feature_improvement):
  ```bash
  git checkout -b i18_feature_improvement

- Commit:
  ```bash
  git add .
  git commit -m "Fix issue 18: Explore feature improvement X"
  git push --set-upstream origin i18_feature_improvement

- Create a PR:
  - On GitHub, navigate to your repository.
  - Locate your branch and click Compare & pull request.
  - In the PR description:
    - Link the related issue (e.g., “Closes #18).
    - Provide an overview of the changes and why they’re necessary.
    - Assign reviewers if needed and label the PR (e.g., bugfix, enhancement).
    - Tip: Submit your PR once changes are stable to reduce the risk of merge conflicts.

- Review and Merge:
  Await feedback from reviewers.
  If changes are requested, make them in your branch locally, then push again.
  Once approved, merge into master (or the default branch).

Thank you for following these guidelines!
