# Einrichtung des AI Email Assistant

Diese Anleitung führt dich Schritt für Schritt durch die Installation.

## Voraussetzungen

- Docker und Docker Compose installiert
- Claude API Key von [anthropic.com](https://console.anthropic.com)
- IMAP-Zugangsdaten deines E-Mail-Postfachs
- (Optional) Slack API Key für Benachrichtigungen

## Schritt 1: Repo klonen

```bash
git clone https://github.com/ceeceeceecee/ai-email-assistant.git
cd ai-email-assistant
```

## Schritt 2: Konfiguration anpassen

```bash
cp config/settings.example.json config/settings.json
```

Bearbeite `config/settings.json` und trage deine Daten ein:

1. **IMAP:** Host, Port, Benutzername und Passwort
2. **Claude:** API Key wird in n8n als Credential hinterlegt
3. **Slack:** (Optional) Channel und API Key

## Schritt 3: Docker starten

```bash
docker compose up -d
```

Prüfe ob alles läuft:

```bash
docker compose ps
docker compose logs -f n8n
```

## Schritt 4: n8n einrichten

1. Öffne `http://localhost:5678` im Browser
2. Erstelle einen Account
3. Hinterlege die Claude API Credentials:
   - Gehe zu **Credentials** → **Add Credential**
   - Wähle **Anthropic API**
   - Trage deinen API Key ein
4. Hinterlege IMAP Credentials (falls nicht im Workflow konfiguriert)
5. Importiere den Workflow aus `workflow/ai-email-assistant.json`

## Schritt 5: Workflow aktivieren

1. Öffne den importierten Workflow
2. Klicke auf **Active** (Schalter oben rechts)
3. Teste mit einer Test-E-Mail

## Fehlersuche

**n8n startet nicht:**
```bash
docker compose logs n8n
```

**IMAP-Verbindung fehlgeschlagen:**
- Prüfe Host und Port
- Prüfe ob App-Passwort statt regulärem Passwort nötig ist (Gmail, Outlook)
- Prüfe SSL/TLS-Einstellungen

**Claude API Fehler:**
- Prüfe API Key
- Prüfe Guthaben bei Anthropic
- Prüfe Modell-Verfügbarkeit

## Sicherheitshinweise

- Speichere `config/settings.json` nie im Git
- Nutze App-Passwörter für E-Mail-Zugang
- Claude API Key nur in n8n Credentials, nicht in JSON-Dateien
- Aktiviere HTTPS für die n8n-Instanz (Reverse Proxy empfohlen)
