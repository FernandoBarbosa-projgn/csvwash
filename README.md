# csvwash

Reusable ETL skeleton for the CSVs I get at work

## Installation

```bash
pip install -r requirements.txt
```

## How to use

```bash
python pipeline.py raw.csv --config config.yaml --out clean.csv
```

## What it does

- Writes a cleaning report next to the output
- Drops duplicates, trims strings, normalizes dates
- Chunked reading for files that do not fit in memory
- Config-driven column renames and type casts

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── development.md
│   ├── roadmap.md
│   └── usage.md
├── tests/
│   └── test_smoke.py
├── .editorconfig
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── config.yaml
├── pipeline.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```
