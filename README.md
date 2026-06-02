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

##Notes
stocker -> all maps -> jump shocks, landing boost, wings
stocker -> mountain -> wings, winter tires, wheele boost
muscle car -> Forest -> magnet, wings, overcharged turbo
muscle car city -> wings, magnet, thrusters
muscle car -> mountain -> wings, winter tires, wheelie boost
muscle car -> unter wasser -> wings, Overcharged Turbo, jump shocks
muscle car -> winter -> wings, Overcharged Turbo, jump shocks
muscle car -> bergwerk kangaroo
buscle car -> wüste/sand -> wings, winter tires, Overcharged Turbo
buscle car -> Schlamm -> wings, winter tires, Overcharged Turbo
buscle car -> harter winter -> kangoroo
muscle car -> beim rest der welten ist auch kangoroo zu nehmen
off-roader -> Countryside -< nitro, wheelie boost, wings
off-roader  -> Forest ->  magnet, wings, nitro
off-roader ->stadt -> magnet, wings, nitro
off-roader -> mountain -> magnet, wheelie boost, wings
off-roader -> unter wasser -> magnet, wings, nitro
off-roader ->  winter -> magnet, wings, nitro
off-roader -> Berg -> magnet, wings, nitro
off-roader -> dessert einfache map?-> wheelie boost, wings, nitro
off-roader -> sandstrand -> wheelie boost, wings, nitro
off-roader -> schlamm -> wheelie boost, wings, nitro
off-roader -> harter winter-> wheelie boost, wings, nitro
off-roader -> robotter -> wheelie boost, wings, nitro
off-roader -> karusel-> magnet, wings, nitro
off-roader -> savanna-> magnet, wings, nitro
off-roader -> wunderland -> wheelie boost, wings, nitro
off-roader -> canyon -> wheelie boost, wings, nitro
off-roader -> stadt bei nacht -> wheelie boost, wings, nitro
off-roader -> Spring Falls -> magnet, wings, nitro
off-roader -> moon -> wheelie boost, wings, nitro
rock bouncer -> Countryside -> wings, coin boost, wheelie boost
rock bouncer -> Forest -> magnet, wings, (wheelie boost, oder fume boost)
rock bouncer -> stadt -> wings, thrusters, magnet
rock bouncer -> mountain -> jump shocks, wings, fume boost
rock bouncer -> wasser -> wings, fume boost,  magnet
rock bouncer -> winter -> wings, fume boost,  magnet
rock bouncer -> bergwert -> wings, jump shocks, fume boost
rock bouncer -> dessert -> wings, jump shocks, fume boost
rock bouncer -> sand  -> wings, fume boost,  magnet
rock bouncer -> schlamm  -> wings, fume boost,  magnet
rock bouncer -> harter winter-> wings, jumps, wheelie boost
rock bouncer ->robot -> kangoroo
rock bouncer -> mystic-> wings, wheelie boost, jump shocks
rock bouncer -> karusell-> nitro, jump shocks, wings
rock bouncer -> canyon -> kangoroo
rock bouncer ->finstere stadt -> wings, jump shocks, wheelie boost
rock bouncer -> moon -> kangoroo

GitHub Pages ist ein **Static Site Hosting Service** für HTML-, CSS- und JavaScript-Dateien direkt aus einem GitHub-Repository. Für dein Projekt ist das ideal, weil du keine Datenbank und keinen Server brauchst, solange deine Inhalte in `data.json` liegen. [web:105][web:84]
