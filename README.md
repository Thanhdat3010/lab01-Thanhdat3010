# Study Assistant — starter

A starter repository for the CSC10014 Smart Virtual Assistant project.

## Setup
Prerequisites: Python 3.10+, Git.

```bash
git clone https://github.com/Thanhdat3010/lab01-Thanhdat3010.git
cd lab01-Thanhdat3010
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\Activate.ps1
pip install -r requirements.txt
pip install -e .
```

## Run
```bash
python -m assistant "where is the library?"
# -> Library: room B.201, open Mon-Sat 07:00-20:00.
```

## Test
```bash
pytest -q                          # -> 5 passed
```

## Project structure
- `data/`: CSV data files (campus office locations and hours).
- `docs/`: project documentation, reports, and architecture decision records.
- `scripts/`: developer utility scripts including environment sanity check.
- `src/`: source code package for the virtual assistant.
- `tests/`: automated test suite for pytest.
- `ui/`: user interface assets and components.

## Troubleshooting
- "No module named assistant" -> you forgot `pip install -e .` or the venv is not active.
- PowerShell blocks Activate.ps1 -> `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`
