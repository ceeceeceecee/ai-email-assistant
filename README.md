# Ai Email Assistant

<p align="center">
<img src="https://raw.githubusercontent.com/ceeceeceecee/ai-document-analyzer/main/docs/coletrading-banner.svg" alt="ColeTrading" width="600">
</p>

![n8n](https://img.shields.io/badge/n8n-Workflow-FF6D5A?logo=n8n) ![Claude](https://img.shields.io/badge/Claude-AI Engine-9945FF?logo=anthropic) ![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker) ![License](https://img.shields.io/badge/License-MIT-blue) ![DSGVO](https://img.shields.io/badge/DSGVO-Konform-brightgreen)

> Intelligenter E-Mail-Assistent mit natürlicher Sprachverarbeitung

## Overview

Automatisiert E-Mail-Verarbeitung mit Claude AI und n8n. Klassifiziert eingehende E-Mails, generiert Antworten und erstellt Zusammenfassungen — DSGVO-konform über Ollama.

## Features

- E-Mail-Klassifizierung mit Claude AI
- Automatische Antwort-Generierung
- E-Mail-Zusammenfassungen
- n8n-Workflow-Integration
- DSGVO-konforme Verarbeitung
- Konfigurierbare Kategorien und Regeln

## Tech Stack

| Tech | Zweck |
|------|-------|
| n8n | Workflow-Orchestrierung |
| Claude AI | NLP-Verarbeitung |
| Ollama | Lokale KI-Verarbeitung |
| Docker Compose | Deployment |

## Quick Start

```bash
docker compose up -d
# Oeffne http://localhost:5678
```

## Screenshots

**n8n Workflow zur E-Mail-Verarbeitung**

<img src="screenshots/n8n-workflow.png" alt="n8n Workflow zur E-Mail-Verarbeitung" width="800">

**Laufende n8n-Instanz mit importiertem Workflow**

<img src="screenshots/setup-running.png" alt="Laufende n8n-Instanz mit importiertem Workflow" width="800">

**Generierte E-Mail-Zusammenfassung**

<img src="screenshots/email-summary-output.png" alt="Generierte E-Mail-Zusammenfassung" width="800">

**Claude AI Antwort-Generierung**

<img src="screenshots/claude-response.png" alt="Claude AI Antwort-Generierung" width="800">

---

## Contributing

Beiträge sind willkommen! Bitte erstelle einen Issue oder Pull Request.

## License

MIT License — siehe [LICENSE](LICENSE).

<p align="center">
<a href="https://github.com/ceeceeceecee">ColeTrading</a> &bull; DSGVO-konform &bull; Self-Hosted &bull; Open Source
</p>