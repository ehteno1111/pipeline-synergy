# Pipeline Synergy — Secure CI/CD Demo
**Flow:** tests → SAST → Docker build → container scan → DAST. (IaC optional)

## Stack
Python/Flask + pytest • GitHub Actions • Bandit • Flake8 • Docker + GHCR • Trivy • OWASP ZAP

## Run local
```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
pytest
python app/app.py  # http://localhost:8000
```bash
docker build -t pipeline-synergy:dev .
docker run -p 8000:8000 pipeline-synergy:devmd
md
