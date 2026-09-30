# Linux Log Monitor & Incident Automation

A compact DevOps/SRE project built around Linux-style log analysis, Bash automation, Docker, and GitHub Actions.

## Features
- Parses Linux-style application/authentication logs with Python.
- Detects ERROR, CRITICAL, and failed-login events.
- Produces a concise incident report.
- Uses exit code 2 when error/critical events are detected for automation.
- Includes a Bash wrapper.
- Runs inside Docker.
- Uses GitHub Actions for validation.

## Tech Stack
Linux/Unix, Python, Bash, Docker, Git, GitHub Actions

## Structure
```text
.
├── .github/workflows/ci.yml
├── scripts/log_analyzer.py
├── scripts/monitor.sh
├── sample/app.log
├── Dockerfile
└── README.md
```

## Run
```bash
python3 scripts/log_analyzer.py sample/app.log
bash scripts/monitor.sh sample/app.log
```

## Docker
```bash
docker build -t linux-log-monitor .
docker run --rm linux-log-monitor
```

## DevOps Relevance
Demonstrates Linux log inspection, incident detection, Python/Bash automation, Docker containerization, Git, and CI validation.
