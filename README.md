# AI Email Assistant

[![n8n](https://img.shields.io/badge/n8n-Workflow-FF6D5A?logo=n8n)](https://n8n.io)
[![Claude](https://img.shields.io/badge/Claude-AI%20Engine-9945FF?logo=anthropic)](https://anthropic.com)
[![Lizenz](https://img.shields.io/badge/Lizenz-MIT-green.svg)](LICENSE)
[![DSGVO](https://img.shields.io/badge/DSGVO-konform-brightgreen.svg)]()

> KI-gestützter E-Mail-Assistent, der eingehende E-Mails zusammenfasst und Antwortentwürfe erstellt — perfekt für KMU im DACH-Raum.

An AI-powered email assistant that summarizes incoming emails and generates draft responses — ideal for SMBs in the DACH region.

---

## ✨ Features

- 📧 **E-Mail-Zusammenfassung** — Eingehende E-Mails automatisch zusammengefasst
- 🤖 **Antwort-Generierung** — Professionelle Antwortentwürfe auf Deutsch
- 🏷️ **Kategorisierung** — E-Mails nach Priorität und Typ sortiert
- 📢 **Slack-Integration** — Wichtige E-Mails direkt an Slack senden
- 🔄 **Template-Builder** — Anpassbare Antwort-Templates
- 🔒 **DSGVO-konform** — Selbstgehostet, keine Datenweitergabe

## 🎯 Use Cases für KMU

| Szenario | Nutzen |
|----------|--------|
| Kundenanfragen | Sofortiger Überblick über Anliegen |
| Terminanfragen | Automatische Entwürfe für Bestätigungen |
| Beschwerden | Vorgeschlagene deeskalierende Antworten |
| Angebote | Strukturierte Zusammenfassung für Vertrieb |

> Demo-GIF wird nachgereicht.
> <!-- ![Demo](docs/demo.gif) -->

## 🚀 Voraussetzungen

- Docker & Docker Compose
- Claude API Key ([anthropic.com](https://anthropic.com))
- IMAP-Zugang (E-Mail-Postfach)
- (Optional) Slack Workspace für Benachrichtigungen

## 📦 Schnellstart

```bash
git clone https://github.com/ceeceeceecee/ai-email-assistant.git
cd ai-email-assistant
cp config/settings.example.json config/settings.json
# settings.json anpassen
docker compose up -d
```

Siehe [docs/setup-guide.md](docs/setup-guide.md) für die Schritt-für-Schritt-Anleitung.

## 📁 Projektstruktur

```
ai-email-assistant/
├── workflow/                    # n8n Workflow JSON
├── prompts/                     # Claude System-Prompts
│   ├── email-summary.txt        # Zusammenfassungs-Prompt
│   └── email-response.txt       # Antwort-Generierungs-Prompt
├── config/
│   └── settings.example.json    # Konfigurations-Vorlage
├── docs/
│   └── setup-guide.md           # Installationsanleitung
├── docker-compose.yml           # n8n + Redis
├── .env.example
└── LICENSE
```

## 🛠️ Konfiguration

Die wichtigste Datei ist `config/settings.json`:

```json
{
  "imap": {
    "host": "imap.example.com",
    "port": 993,
    "user": "deine@email.de"
  },
  "claude": {
    "model": "claude-3-5-sonnet-20241022"
  },
  "filtering": {
    "minPriority": "normal",
    "excludeDomains": ["newsletter.example.com"]
  }
}
```

## 🗺️ Roadmap

- [ ] Outlook/Exchange IMAP Support
- [ ] Mehrsprachige Antwort-Generierung (DE/EN/FR)
- [ ] Anlern-Feature für firmenspezifische Antwort-Templates
- [ ] Web-Dashboard für E-Mail-Statistiken
- [ ] Auto-Send nach Freigabe

## 📄 Lizenz

[MIT](LICENSE) — frei verwendbar, auch kommerziell.

---

Erstellt von [Cela](https://github.com/ceeceeceecee) — Freelancer für Automatisierung & KI-Lösungen.
