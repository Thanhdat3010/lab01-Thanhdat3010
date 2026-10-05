# Study Assistant — starter

A starter repository for the CSC10014 Smart Virtual Assistant project.

## Setup

Follow these steps to set up the development environment from a fresh machine:

1. **Prerequisites**: Ensure that **Python 3.10+** and **Git** are installed.
2. **Clone the repository**:
   ```bash
   git clone https://github.com/Thanhdat3010/lab01-Thanhdat3010.git
   cd lab01-Thanhdat3010
   ```
3. **Create and activate the virtual environment**:
   - On Windows (PowerShell):
     ```powershell
     python -m venv .venv
     .venv\Scripts\Activate.ps1
     ```
     *(In Command Prompt: `.venv\Scripts\activate.bat`)*
   - On Linux/macOS:
     ```bash
     python3 -m venv .venv
     source .venv/bin/activate
     ```
4. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   pip install -e .
   ```
5. **Verify setup**:
   ```bash
   python scripts/check_env.py
   ```

## Run

Run the assistant in one-shot mode or interactive mode:

- **One-shot mode** (ask a single question):
  ```bash
  python -m assistant "where is the IT helpdesk?"
  ```
- **Interactive mode** (chat session):
  ```bash
  python -m assistant
  ```
  *(Type `quit` or `exit` to end the session)*

## Test

Run automated smoke tests using pytest:

```bash
pytest -q
```

## Project structure

```text
├── data/
│   └── offices.csv            # Campus office locations and working hours
├── docs/                      # Project documentation, team reports and ADRs
├── scripts/
│   └── check_env.py           # Verification script for developer environment
├── src/
│   └── assistant/
│       ├── __init__.py        # Package initialization
│       ├── __main__.py        # Assistant CLI entrypoint
│       └── rules.py           # Rule-based response logic and office lookup
├── tests/
│   └── test_smoke.py          # Smoke tests for greeting and lookup functions
├── ui/                        # UI assets and code for subsequent phases
├── .gitignore                 # Files and directories ignored by Git
├── pyproject.toml             # Packaging configuration and project metadata
├── README.md                  # Project setup and usage instructions
└── requirements.txt           # Project dependencies (pytest)
```
