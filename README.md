# logmere

Opinionated log housekeeping tool with dry-run support

Side project, maintained when I have time.

## Usage

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## Installation

```bash
pip install -r requirements.txt
python -m logwash --help
```

## Features

- Dry-run mode shows what would happen, touches nothing
- Exit codes friendly for cron and CI
- Scan directories for log files by glob pattern
- Filter by age (--older-than) or size (--larger-than)
- Archive matched logs into a timestamped .tar.gz

## Project structure

```text
├── .github/
│   └── dependabot.yml
├── docs/
│   ├── development.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   ├── cli.py
│   └── errors.py
├── tests/
│   ├── test_cli.py
│   └── test_smoke.py
├── .editorconfig
├── .gitattributes
├── .gitignore
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── Makefile
├── SECURITY.md
├── pyproject.toml
└── requirements.txt
```
