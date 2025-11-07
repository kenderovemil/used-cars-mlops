# Used-Cars-MLOps Repository Exploration Report

**Date:** October 31, 2025  
**Repository:** kenderovemil/used-cars-mlops  
**Purpose:** Comprehensive exploration to identify all `.py`, `.ipynb`, `.pkl`, and `.csv` files

---

## Executive Summary

The `used-cars-mlops` repository was explored to identify all Python files, Jupyter notebooks, pickle model files, and CSV data files. The current repository state contains **only the README.md file** with no actual project implementation files present.

---

## Current Repository Structure

### Files Present (Actual State)
```
used-cars-mlops/
├── .git/                    # Git metadata directory
└── README.md                # Project documentation (11,646 bytes)
```

### Search Results
- **Python files (.py):** 0 files found
- **Jupyter Notebooks (.ipynb):** 0 files found
- **Pickle files (.pkl):** 0 files found
- **CSV files (.csv):** 0 files found

---

## Expected Repository Structure (from README.md)

The README.md describes a comprehensive MLOps project that should contain the following structure:

### Python Files (.py)

#### Data Science Source Files (`data-science/src/`)
1. `prep.py` - Data preparation script
2. `prep.py.amltmp` - Temporary version of prep script
3. `prepare.py` - Alternative preparation script
4. `prepare.py.amltmp` - Temporary version of prepare script
5. `register.py` - Model registration script
6. `register.py.amltmp` - Temporary version of register script
7. `train.py` - Model training script
8. `train.py.amltmp` - Temporary version of train script

#### Model Training (`model_training/`)
9. `train_model.py` - Main model training script
10. `train_model.py.amltmp` - Temporary version

### Jupyter Notebooks (.ipynb)

1. `Week-17_Project_FullCode_Notebook .ipynb` - Complete project notebook
2. `week-17_project_fullcode_notebook .ipynb.amltmp` - Temporary version

### CSV Data Files (.csv)

#### Original Data (`data/`)
1. `used_cars.csv` - Raw dataset with used car information

#### Processed Data (`outputs/test/`)
2. `test.csv` - Test dataset

#### Processed Data (`outputs/train/`)
3. `train.csv` - Training dataset

#### Artifact Outputs (`outputs_cool_market_ptblwpcn61/artifacts/outputs/test/`)
4. `test.csv` - Test data artifact

#### Artifact Outputs (`outputs_cool_market_ptblwpcn61/artifacts/outputs/train/`)
5. `train.csv` - Train data artifact

#### Temporary Outputs (`tmp_test/`)
6. `test.csv` - Temporary test data

#### Temporary Outputs (`tmp_train/`)
7. `train.csv` - Temporary train data

### Pickle Model Files (.pkl)

#### Model Artifacts (`outputs/model/`)
1. `model.pkl` - Trained Random Forest Regressor model

---

## Expected Directory Structure (Complete)

Based on the README.md, the complete project structure should be:

```
used-cars-mlops/
├── Week-17_Project_FullCode_Notebook .ipynb
├── data/
│   └── used_cars.csv
├── data-science/
│   ├── components/
│   │   ├── prep_component.yml
│   │   ├── prep_component.yml.amltmp
│   │   ├── prep_job.yml
│   │   └── prep_job.yml.amltmp
│   ├── environment/
│   │   ├── train-conda.yml.amltmp
│   │   ├── train_conda.yml
│   │   └── train_conda.yml.amltmp
│   └── src/
│       ├── prep.py
│       ├── prep.py.amltmp
│       ├── prepare.py
│       ├── prepare.py.amltmp
│       ├── register.py
│       ├── register.py.amltmp
│       ├── train.py
│       └── train.py.amltmp
├── github_working/
│   ├── custom-create-compute.yml
│   ├── custom-register-dataset.yml
│   ├── custom-register-environment.yml
│   ├── custom-run-pipeline.yml
│   └── deploy-model-training-pipeline-classical.yml
├── mlops/
│   └── azureml/
│       └── train/
│           ├── data.yml
│           ├── newpipeline.yml
│           ├── newpipeline.yml.amltmp
│           ├── prep.yml
│           ├── prep.yml.amltmp
│           ├── register.yml
│           ├── register.yml.amltmp
│           ├── train-env.yml
│           ├── train-env.yml.amltmp
│           ├── train.yml
│           └── train.yml.amltmp
├── model_training/
│   ├── train_model.py
│   └── train_model.py.amltmp
├── outputs/
│   ├── model/
│   │   ├── MLmodel
│   │   ├── conda.yaml
│   │   ├── model.pkl
│   │   ├── python_env.yaml
│   │   └── requirements.txt
│   ├── model_info/
│   │   └── model_info.json
│   ├── test/
│   │   └── test.csv
│   └── train/
│       └── train.csv
├── tmp_test/
│   └── test.csv
├── tmp_train/
│   ├── prep_diagnostics.json
│   └── train.csv
└── README.md
```

---

## Project Description Summary

According to the README.md, this is an **end-to-end MLOps pipeline for predicting used car prices** designed for an automobile dealership in Las Vegas. The pipeline should include:

### Pipeline Components:
1. **Data Preparation** (`prepare.py`)
   - Reads raw CSV
   - Splits into train/test
   - Writes outputs and diagnostics

2. **Model Training** (`train_model.py`)
   - Trains Random Forest Regressor
   - Logs MSE in MLflow
   - Saves model as MLflow artifact

3. **Model Registration** (`model_register.py`)
   - Loads best model
   - Registers in MLflow registry

4. **End-to-End Workflow** (`pipeline_definition.py`)
   - Assembles all steps into a unified pipeline
   - Executes in AzureML Studio

### Technologies:
- Azure Machine Learning
- MLflow
- GitHub Actions
- Python (pandas, scikit-learn)
- YAML for CI/CD workflows

### Dataset Features:
- Segment (Luxury/non-luxury classification)
- Kilometers_Driven
- Mileage (km/l)
- Engine (cc)
- Power (BHP)
- Seats
- Price (₹100,000 units)

---

## Conclusions

1. **Current State:** The repository is in an initial/minimal state with only documentation (README.md) present.

2. **Missing Components:** All implementation files are missing, including:
   - 10 Python scripts (.py files)
   - 2 Jupyter notebooks (.ipynb files)
   - 1 trained model file (.pkl file)
   - 7 CSV data files (original and processed)

3. **README Status:** The README.md is comprehensive and well-documented, describing the complete intended project structure, but represents a future/planned state rather than the current repository contents.

4. **Next Steps:** To implement this project, the following would need to be added:
   - Source data file (used_cars.csv)
   - Python implementation scripts for data prep, training, and registration
   - Jupyter notebook with complete project code
   - Configuration files for Azure ML and GitHub Actions
   - Trained model artifacts after pipeline execution

---

## Search Commands Used

```bash
# Search for specific file types
find . -type f -name "*.py" -o -name "*.ipynb" -o -name "*.pkl" -o -name "*.csv"

# List all files excluding .git
find . -type f ! -path './.git/*' | sort

# List all tracked files in git
git ls-tree -r --name-only HEAD

# Display directory structure
tree -L 3 -a 2>/dev/null || find . -maxdepth 3 -print
```

---

**Report Generated:** October 31, 2025  
**Repository State:** Empty (documentation only)  
**Files Found:** 1 (README.md)  
**Target Files Found:** 0 (.py, .ipynb, .pkl, .csv)
