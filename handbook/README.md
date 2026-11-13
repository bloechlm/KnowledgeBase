# KnowledgeBase · Service-Handbuch

## Lokal starten

Node.js 22 oder neuer. Im Terminal in diesen Ordner wechseln. In macOS mit zsh:

```zsh
read -rs 'OPENAI_API_KEY?OpenAI API-Schlüssel: '
export OPENAI_API_KEY
node server.mjs
```

In Safari http://127.0.0.1:8765 öffnen. Der Server lauscht nur lokal. Der KI-Button sendet Titel und die drei Stichwortfelder an die OpenAI API. Fotos und Verweise werden in der Projektdatei gespeichert. Der API-Schlüssel gehört in die Serverumgebung. Für Live-KI braucht der Schlüssel API-Zugriff und verfügbares API-Guthaben. Mit Ctrl+C beendest du den Server. Mit `unset OPENAI_API_KEY` entfernst du den Schlüssel aus der Terminal-Umgebung.

## Handbuch bearbeiten

Kapitel und Fehlerfälle anlegen, sortieren und verschieben. Stichwörter eingeben und bei Bedarf **Mit KI ausformulieren** wählen. Den vorgeschlagenen PDF-Text prüfen und im Eintrag bearbeiten. Mit **Projekt speichern** lädst du eine JSON-Datei samt Texten, Stichwörtern, Reihenfolge und Fotos herunter. Öffne diese Datei für spätere Änderungen.

**PDF erstellen** öffnet den Druckdialog für das gesamte Handbuch. Dort **Als PDF sichern** wählen. Jeder Fehlerfall beginnt auf einer neuen Seite. Das Inhaltsverzeichnis folgt der Kapitel- und Eintragsreihenfolge.

GitHub Pages kann die statische Oberfläche ausliefern. Der KI-Button verwendet den gleichnamigen Endpunkt `/api/draft` auf demselben Server. Für einen Onlinebetrieb braucht dieser Endpunkt serverseitige Anmeldung und Zugriffsbeschränkung.
