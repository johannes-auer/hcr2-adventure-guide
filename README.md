# HCR2 Setup Demo – GitHub Pages Grundstruktur

Diese Struktur ist für **GitHub Pages** vorbereitet. GitHub Pages kann statische Dateien direkt aus einem Repository veröffentlichen, und als Quelle kann dabei die **Root** oder ein **`/docs`-Ordner** verwendet werden. [web:84][web:100]

## Ordnerstruktur

```text
hcr2-github-structure/
├─ README.md
├─ docs/
│  ├─ index.html
│  └─ data.json
└─ assets/
```

## Warum `docs/`?

GitHub Pages unterstützt bei Projekt-Repositories das Veröffentlichen aus dem Repository-Root oder aus einem **`/docs`-Ordner** auf dem gewählten Branch. Das ist praktisch, weil du später im gleichen Repository auch Notizen, Quellen oder Arbeitsdateien ablegen kannst, ohne dass alles direkt öffentlich als Website ausgeliefert wird. [web:100][web:104]

## Was liegt wo?

- `docs/index.html` → deine eigentliche Website
- `docs/data.json` → deine Maps, Fahrzeuge und Setups
- `assets/` → später Bilder, Icons oder Screenshots
- `README.md` → Erklärung für dich oder andere Mitwirkende

Die Website lädt die JSON-Datei mit `fetch('./data.json')`, deshalb liegen `index.html` und `data.json` im selben veröffentlichten Ordner. [web:92]

## So gehst du auf GitHub vor

1. Erstelle ein neues **öffentliches Repository** auf GitHub.
2. Lade den Inhalt dieses Ordners hoch.
3. Öffne auf GitHub **Settings → Pages**.
4. Wähle bei **Build and deployment** als Source: **Deploy from a branch**. [web:100]
5. Wähle deinen Branch, meist **main**.
6. Wähle als Folder **/docs**. GitHub Pages veröffentlicht dann genau diesen Ordner. [web:100][web:104]
7. Nach kurzer Zeit bekommst du eine URL im Stil:
   `https://DEINNAME.github.io/REPO-NAME/` [web:105]

## So pflegst du später neue Daten

Wenn du eine neue Map oder ein neues Fahrzeug hinzufügen willst, bearbeitest du in der Regel nur `docs/data.json`. Die HTML-Datei bleibt fast gleich, solange die Datenstruktur gleich bleibt.

## Lokal testen

Wenn du lokal testen willst, starte im Projektordner einen kleinen Webserver:

```bash
python -m http.server 8000
```

Dann öffnest du:

```text
http://localhost:8000/docs/
```

## Später sinnvoll erweiterbar

- `docs/admin.html` für eine kleine Admin-GUI
- `docs/assets/` für Logos oder Vorschaubilder
- `docs/data/` für mehrere JSON-Dateien statt nur einer Datei
- GitHub Actions für automatische Prüfungen oder Deployments

## GitHub Pages kurz erklärt

GitHub Pages ist ein **Static Site Hosting Service** für HTML-, CSS- und JavaScript-Dateien direkt aus einem GitHub-Repository. Für dein Projekt ist das ideal, weil du keine Datenbank und keinen Server brauchst, solange deine Inhalte in `data.json` liegen. [web:105][web:84]
