# FDS Project — Road Accident Data Analysis

A data science project analysing Nepal road accident data, structured around the full **Data Science Lifecycle**.

---

## Table of Contents

- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Clone the Repository](#1-clone-the-repository)
  - [Create a Virtual Environment](#2-create-a-virtual-environment)
  - [Install Dependencies](#3-install-dependencies)
  - [Launch Jupyter](#4-launch-jupyter-notebook)
- [Notebook Workflow](#notebook-workflow)
- [Dataset](#dataset)

---

## Project Structure

```
FDS_Project/
├── data/
│   ├── 01_raw/             # Original immutable data
│   ├── 02_external/        # Third-party sources
│   ├── 03_interim/         # Cleaned intermediate data
│   ├── 04_processed/       # Final modelling-ready data
│   └── 05_features/        # Engineered feature sets
├── notebooks/
│   ├── 01_business_understanding/
│   ├── 02_data_acquisition/
│   ├── 03_data_cleaning/
│   ├── 04_eda/
│   ├── 05_feature_engineering/
│   ├── 06_modeling/
│   └── 07_evaluation/
├── src/
│   ├── data/               # Ingestion & cleaning scripts
│   ├── features/           # Feature engineering modules
│   ├── models/             # Training & inference
│   ├── evaluation/         # Metrics utilities
│   └── visualization/      # Plotting helpers
├── models/
│   ├── trained/            # Serialised models
│   └── evaluation/         # Evaluation artefacts
├── reports/
│   └── figures/            # Generated charts
├── requirements.txt
└── README.md
```

---

## Prerequisites

| Tool   | Minimum Version | Download                      |
| ------ | --------------- | ----------------------------- |
| Python | 3.10+           | https://python.org/downloads  |
| Git    | any recent      | https://git-scm.com/downloads |

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/FDS_Project.git
cd FDS_Project
```

---

### 2. Create a Virtual Environment

#### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

#### Windows (Command Prompt)

```cmd
python -m venv venv
venv\Scripts\activate
```

#### Windows (PowerShell)

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

> **PowerShell note:** If you see an execution policy error, run this first:
>
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open your browser at **http://localhost:8888** and navigate to the `notebooks/` folder.

---

## Notebook Workflow

Run the notebooks **in order** — each stage feeds the next:

| #   | Notebook                    | Stage                                     |
| --- | --------------------------- | ----------------------------------------- |
| 1   | `01_business_understanding` | Define the problem & success metrics      |
| 2   | `02_data_acquisition`       | Load & snapshot raw data                  |
| 3   | `03_data_cleaning`          | Remove duplicates, fix nulls & outliers   |
| 4   | `04_eda`                    | Explore distributions & correlations      |
| 5   | `05_feature_engineering`    | Encode, scale & select features           |
| 6   | `06_modeling`               | Train & tune models                       |
| 7   | `07_evaluation`             | Evaluate & compare against business goals |

---

## Dataset

| Property | Value                            |
| -------- | -------------------------------- |
| File     | `data/01_raw/dataset.csv`        |
| Rows     | 1,200                            |
| Columns  | 15                               |
| Target   | `Accident_Severity`              |
| Coverage | Nepal road accidents (2023–2026) |

**Columns:**
`Accident_ID`, `Accident_Date`, `Year`, `Month`, `Province`, `District`,
`Road_Type`, `Intersection_Type`, `Time_of_Day`, `Accident_Severity`,
`Weather_Condition`, `Road_Surface`, `Vehicle_Type`, `Speed_Zone`, `Driver_Gender`

---

## Deactivating the Environment

#### macOS / Linux

```bash
deactivate
```

#### Windows

```cmd
venv\Scripts\deactivate
```
