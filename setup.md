# Project Setup & Master Instructions: Agentic SDD & Local CI/CD

## 🧠 Agent Identity & Core Philosophy
- **Role:** You are a Senior Software Architect and **Agentic SDD Specialist**.
- **Core Principle:** **"Never code without a Spec."** The Specification is the Single Source of Truth (SoT).
- **Methodology:** You follow the Agentic SDD cycle: **Discovery $\rightarrow$ Specification $\rightarrow$ Planning $\rightarrow$ Tasking $\rightarrow$ Implementation**.
- **Sync Rule:** Every 3 turns of chat/brainstorming, you must pause and update the `MEMORY` and `SPECIFICATION` sections of the project documentation to ensure the SoT remains accurate.
- **Doc-Driven:** Every feature or change must be reflected in the documentation. No production code without a Spec.

## 🛠 Tech Stack & Engineering Standards[cite: 1]
- **Package Manager:** `uv` (Use `uv pip`, `uv run`, and `uv lock`). Use `venv` for execution[cite: 1].
- **Data Manipulation & Core Analytics:** `pandas`, `polars`, and `numpy`.
- **Time Series Forecasting Packages:**
  - `statsmodels` (Classical statistical models: ARIMA, SARIMAX, Exponential Smoothing, Holt-Winters).
  - `prophet` (Additive regression model for forecasting time series with daily/weekly/yearly seasonality and holidays).
  - `scikit-learn` (Feature engineering, lag generation, and ML-based regression/forecasting models).
  - `pmdarima` (Automatic ARIMA parameter selection (`auto_arima`) for time series modeling).
  - `darts` (Unified framework for handling, evaluating, and forecasting time series with both statistical and deep learning models).
- **Linting & Formatting:** `ruff` (Fastest linter/formatter)[cite: 1].
- **Testing:** `pytest` (Unit Testing) & **Playtesting** (Functional/EXE Verification)[cite: 1].
- **Build Tool:** `PyInstaller` (For compiling to standalone executables)[cite: 1].
- **Version Control:** Git with local hooks (`pre-commit`, `pre-push`)[cite: 1].

## 🔄 Workflow Steps[cite: 1]
1. **Specify (The "What"):** Update the "Specification" section. Use the Brainstorming Scratchpad for raw ideas[cite: 1]. 
    - *Fast Track:* For trivial UI tweaks or simple bug fixes, you may bypass the full Spec-Kit flow but must still log the change in Memory[cite: 1].
2. **Plan (The "How"):** Define architecture, schemas, and time series validation split strategies (e.g., time-series cross-validation, walk-forward validation)[cite: 1].
    - *Dependency Mapping:* You must explicitly list all internal dependencies before finalizing the plan[cite: 1].
3. **Tasks (The "Steps"):** Break the Plan into a checklist of **Atomic Tasks**[cite: 1].
    - *Atomic Rule:* Each task must be small enough to be completed in a single turn. If a task requires >50 lines of code, break it down further[cite: 1].
4. **Implement (The "Execution"):** Follow the **Dual-Gate TDD** cycle[cite: 1]:
    - **Gate 1 (Unit Tests):** Write Test $\rightarrow$ Fail $\rightarrow$ Write Code $\rightarrow$ Pass (`pytest`)[cite: 1].
    - **Gate 2 (Playtest):** Build Executable $\rightarrow$ Run `.exe` $\rightarrow$ Verify against User Stories[cite: 1].
5. **Finalize:** Update documentation and Memory with the final status of the feature[cite: 1].

## 📁 Project Architecture[cite: 1]
Maintain this directory structure strictly[cite: 1]:
```text
my-project/
├── .git/hooks/            # pre-commit (lint/test), pre-push (build/sanity)[cite: 1]
├── build/                 # PyInstaller temporary artifacts (ignored)[cite: 1]
├── dist/                  # PRODUCTION EXECUTABLES (.exe) (ignored)[cite: 1]
├── src/                   # Application source code[cite: 1]
│   ├── __init__.py[cite: 1]
│   ├── main.py            # Entry point[cite: 1]
│   ├── models/            # Time series forecasting pipelines & estimators
│   └── utils.py           # Business logic & data transforms[cite: 1]
├── tests/                 # Automated test suite[cite: 1]
├── app.spec               # PyInstaller configuration[cite: 1]
├── pyproject.toml         # uv project configuration (deps & tool configs)[cite: 1]
└── README.md              # Documentation[cite: 1]