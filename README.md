# OnPoy Studios – Website

Statische Website (nur HTML/CSS/JS, kein Build) für GitHub Pages. Zweisprachig (DE/EN) – jede Sprache hat ihre eigene URL.

## Ordnerstruktur → URLs

Nach dem Deployment unter `https://onpoy-studios.github.io/web/`:

| Datei | URL |
|---|---|
| `index.html` | leitet automatisch auf `/de/` weiter |
| `de/index.html` | `.../web/de/` (Startseite, Deutsch) |
| `en/index.html` | `.../web/en/` (Startseite, Englisch) |
| `games/trend-or-flop/index.html` | leitet automatisch auf `.../de/` weiter |
| `games/trend-or-flop/de/index.html` | `.../web/games/trend-or-flop/de/` |
| `games/trend-or-flop/en/index.html` | `.../web/games/trend-or-flop/en/` |
| `games/trend-or-flop/de/datenschutz.html` | `.../web/games/trend-or-flop/de/datenschutz.html` |
| `games/trend-or-flop/en/datenschutz.html` | `.../web/games/trend-or-flop/en/datenschutz.html` |
| `games/trend-or-flop/de/nutzungsbedingungen.html` | `.../web/games/trend-or-flop/de/nutzungsbedingungen.html` |
| `games/trend-or-flop/en/nutzungsbedingungen.html` | `.../web/games/trend-or-flop/en/nutzungsbedingungen.html` |
| `games/trend-or-flop/de/impressum.html` | `.../web/games/trend-or-flop/de/impressum.html` |
| `games/trend-or-flop/en/impressum.html` | `.../web/games/trend-or-flop/en/impressum.html` |

Jede Seite hat oben rechts einen **DE / EN**-Umschalter, der auf die jeweilige Sprachversion der gleichen Seite verlinkt (echte URL, kein Umschalten per JavaScript).

Die alten flachen Pfade (`games/trend-or-flop/datenschutz.html` etc., ohne `/de/`) existieren weiterhin als reine Weiterleitungen auf die deutsche Version, damit alte Links nicht ins Leere laufen.

## Deployment (GitHub Pages)

1. github.com → **New repository** → Name frei wählbar (z. B. `web`) → **Public** → Create.
2. **Add file → Upload files** → den kompletten Inhalt dieses Ordners hochladen
   (index.html, favicon.svg, README.md, die Ordner `de/`, `en/` und `games/` mit allen Unterordnern).
   Wichtig: die Ordnerstruktur beibehalten.
3. **Settings → Pages** → Source: „Deploy from a branch" → Branch `main` / `/ (root)` → Save.
4. ~1 Minute warten. Seite ist live unter der oben genannten URL.
5. Jede spätere Änderung: Datei im Repo ersetzen → nach ~1 Min live.

## Kontaktformular aktivieren (Web3Forms, kostenlos)

Das Formular auf der Startseite (`de/index.html` **und** `en/index.html`, Abschnitt „Kontakt" / „Contact") braucht einen Access Key:

1. Auf **https://web3forms.com** die E-Mail `onpoy.studios@gmail.com` eingeben → „Create Access Key".
2. Key aus der Bestätigungs-E-Mail kopieren.
3. In **beiden** Dateien (`de/index.html` und `en/index.html`) die Zeile suchen:
   `<input type="hidden" name="access_key" value="DEIN_WEB3FORMS_ACCESS_KEY">`
   und `DEIN_WEB3FORMS_ACCESS_KEY` durch den echten Key ersetzen.
4. Dateien speichern / im Repo aktualisieren.

Nachrichten kommen dann als E-Mail an onpoy.studios@gmail.com (Free-Tarif: 250 / Monat).
Bis der Key gesetzt ist, zeigt das Formular einen Hinweis auf die E-Mail-Adresse.

## App Store Connect

- **Datenschutz-URL (Pflicht):** `https://onpoy-studios.github.io/web/games/trend-or-flop/de/datenschutz.html`
- **Support-URL (Pflicht):** `https://onpoy-studios.github.io/web/games/trend-or-flop/de/`
- **Marketing-URL (optional):** `https://onpoy-studios.github.io/web/de/`

Die englische Version ist über den DE/EN-Umschalter auf jeder dieser Seiten erreichbar.

## Neues Spiel hinzufügen

1. Ordner `games/<neues-spiel>/de/` und `games/<neues-spiel>/en/` anlegen, jeweils `index.html` + Rechtstexte
   hineinlegen (Aufbau wie bei `trend-or-flop`).
2. Optional eine `games/<neues-spiel>/index.html` als Weiterleitung auf `de/` anlegen (siehe `games/trend-or-flop/index.html` als Vorlage).
3. In `de/index.html` und `en/index.html` im Abschnitt `<section ... id="spiele">` jeweils eine weitere
   `<a class="game-card" href="../games/<neues-spiel>/de/"> … </a>` (bzw. `en/`) ergänzen.

## Eigene Domain (später)

Settings → Pages → Custom domain → z. B. `onpoystudios.com`.
Danach die URLs in App Store Connect anpassen.
