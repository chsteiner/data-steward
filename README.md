# Setup für den 16. Oktober

> UK Data Steward, 3. Durchgang. Module C.4 und D.1. Christian Steiner.

Am 16. Oktober arbeiten wir praktisch. Richte deinen Rechner vorher ein, das dauert etwa 30 Minuten.

**Du musst nicht programmieren können.** Der KI-Agent schreibt den Code, du sagst ihm, was er tun soll, und prüfst das Ergebnis.

- **Context Engineering:** einem Sprachmodell den richtigen Kontext geben, statt bessere Prompts zu suchen.
- **Agentic Coding:** mit einem KI-Agenten arbeiten, der Dateien liest, ändert und Befehle ausführt.
- **[Promptotyping](https://dhcraft.org/Promptotyping/):** aus Daten und einer Beschreibung einen Prototyp bauen.

## Teil 1: Grundausstattung

Vier Schritte, für alle, in dieser Reihenfolge.

### 1. Visual Studio Code

Kostenloser Editor. Darin läuft später dein KI-Agent.

- **Download:** [code.visualstudio.com](https://code.visualstudio.com/)
- **Prüfen:** VS Code startet.

> **Tipp:** Das eingebaute Terminal (ein Fenster für Textbefehle) öffnest du über Terminal > New Terminal. Dort gibst du die Prüfbefehle der nächsten Schritte ein.

### 2. Git

Verwaltet Versionsstände. Damit siehst du, was der Agent geändert hat, und kannst es zurücknehmen.

- **Windows:** [git-scm.com/download/win](https://git-scm.com/download/win)
- **macOS:** im Terminal `xcode-select --install`
- **Linux:** `sudo apt install git` oder `sudo dnf install git`
- **Prüfen:** im Terminal `git --version`

### 3. Python

Die Sprache, in der der Agent seinen Code ausführt. Du musst sie nicht lernen.

- **Download:** [python.org/downloads](https://www.python.org/downloads/)
- **Prüfen:** im Terminal `python --version` (macOS und Linux: `python3 --version`)

> **Windows:** bei der Installation das Häkchen **Add Python to PATH** setzen. Ohne dieses Häkchen findet der Rechner Python nicht.

### 4. GitHub-Konto

Plattform, auf der Softwareprojekte liegen. Dort legen wir dein Projekt ab.

- **Konto anlegen:** [github.com](https://github.com/)
- **Prüfen:** Login funktioniert.

## Teil 2: Dein KI-Agent

Such den Eintrag, der auf dich zutrifft, und mach nur diesen. Jeder Agent läuft auf zwei Arten: als Erweiterung in VS Code (Extensions-Symbol links) oder direkt im Terminal. Der Link führt jeweils zur Installationsanleitung des Anbieters, der Befehl startet den Agenten im Terminal.

### Kein Abo, oder unsicher

[**Antigravity**](https://antigravity.google/docs) von Google. Kostenlose Stufe ohne Kreditkarte, nur ein Google-Konto nötig.

- VS Code: Erweiterung **Google Antigravity** installieren. Herausgeber muss **Google** sein; es gibt ähnlich benannte von anderen Anbietern.
- Terminal: `agy`
- Mit dem Google-Konto anmelden.

> Die kostenlose Stufe hat ein Tageskontingent. Verbrauch es nicht am Vortag.

### Claude-Abo (Pro oder Max)

[**Claude Code**](https://code.claude.com/docs/en/quickstart), im Abo enthalten.

- VS Code: Erweiterung **Claude Code** von Anthropic.
- Terminal: `claude`
- Mit dem Claude-Konto anmelden.

### ChatGPT-Abo (Plus oder Pro)

[**Codex**](https://developers.openai.com/codex/cli), im Abo enthalten.

- VS Code: Erweiterung **Codex** von OpenAI.
- Terminal: `codex`
- Mit dem OpenAI-Konto anmelden.

### GitHub Copilot

[**GitHub Copilot**](https://docs.github.com/en/copilot/how-tos/copilot-cli). Jedes GitHub-Konto hat eine kostenlose Stufe mit begrenztem Kontingent.

- VS Code: Erweiterung **GitHub Copilot**.
- Terminal: `copilot`
- Mit dem GitHub-Konto anmelden.

### Perplexity-Abo

Enthält keinen Coding-Agenten. Nimm Antigravity.

### Lokale Modelle (LM Studio)

Bring das mit, wir vergleichen es am Termin. Für agentisches Arbeiten sind lokale Modelle noch deutlich schwächer, richte deshalb zusätzlich einen der Wege oben ein.

## Teil 3: Dein Use Case

Überleg dir, woran du arbeiten willst. Am besten ein reales Projekt, für das du schon Daten hast: eine Tabelle, Texte, ein Datenbankexport, Metadaten. Bring mit:

- **Die Daten** als Datei. Nur, was in einen KI-Dienst darf: keine echten Forschungsdaten, keine personenbezogenen oder vertraulichen Inhalte. Im Zweifel ein anonymisierter Ausschnitt oder erfundene Daten in derselben Struktur.
- **Eine Forschungsfrage** in zwei, drei Sätzen: Was willst du aus den Daten herausfinden?

Hast du nichts Passendes, stelle ich am Termin Beispieldaten mit Forschungsfrage bereit.

## Checkliste

- [ ] VS Code installiert, Terminal geht auf
- [ ] `git --version` zeigt eine Versionsnummer
- [ ] `python --version` zeigt eine Versionsnummer
- [ ] GitHub-Login funktioniert
- [ ] KI-Agent installiert, angemeldet, Testfrage beantwortet
- [ ] Use Case: Daten und Frage, oder Beispieldaten

## Wenn etwas nicht funktioniert

### „python“ oder „git“ wird nicht erkannt

VS Code komplett schließen und neu starten; das Terminal kennt frisch installierte Programme erst dann. Hilft das nicht, fehlt unter Windows meist das Häkchen **Add Python to PATH**: Python neu installieren und das Häkchen setzen.

### Windows: bei „python“ öffnet sich der Microsoft Store

Einstellungen > Apps > Erweiterte App-Einstellungen > App-Ausführungsaliase: `python.exe` und `python3.exe` ausschalten, Terminal neu starten.

### macOS: „von einem nicht verifizierten Entwickler“

Systemeinstellungen > Datenschutz & Sicherheit, nach unten scrollen, **Trotzdem öffnen**.

### Ich finde die Erweiterung nicht

Links in der schmalen Leiste das Symbol mit vier Quadraten anklicken, oben den Namen eintippen, in der Trefferliste auf den Herausgeber unter dem Namen achten.

### Der Agent antwortet nicht mehr

Meist ist das Tageskontingent aufgebraucht. Es füllt sich nach einigen Stunden wieder.

### Ich komme nicht weiter

Schreib mir vor dem Termin: welches Betriebssystem, welcher Schritt.

## Bitte beachten

Alle genannten Dienste verarbeiten deine Eingaben auf Servern der Anbieter. Kostenlose Stufen werden oft mit den Eingaben bezahlt. Deshalb in den Übungen **keine echten Forschungsdaten und keine personenbezogenen Daten**. Wann welcher Weg vertretbar ist, besprechen wir am Termin.

## Fragen

[christian.steiner@dhcraft.org](mailto:christian.steiner@dhcraft.org)

Stand: September 2026. Die Anbieter ändern ihre kostenlosen Angebote häufig; stimmt etwas nicht mehr, schreib mir.
