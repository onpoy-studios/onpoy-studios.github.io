# OnPoy Studios – Website

Statische Website (nur HTML/CSS/JS, kein Build) für GitHub Pages.

## Ordnerstruktur → URLs

Nach dem Deployment unter `https://<DEIN-GITHUB-NAME>.github.io/onpoy-studios/`:

| Datei | URL |
|---|---|
| `index.html` | `.../onpoy-studios/` |
| `games/trend-or-flop/index.html` | `.../onpoy-studios/games/trend-or-flop/` |
| `games/trend-or-flop/datenschutz.html` | `.../onpoy-studios/games/trend-or-flop/datenschutz.html` |
| `games/trend-or-flop/nutzungsbedingungen.html` | `.../onpoy-studios/games/trend-or-flop/nutzungsbedingungen.html` |
| `games/trend-or-flop/impressum.html` | `.../onpoy-studios/games/trend-or-flop/impressum.html` |

## Deployment (GitHub Pages)

1. github.com → **New repository** → Name: `onpoy-studios` → **Public** → Create.
2. **Add file → Upload files** → den kompletten Inhalt dieses Ordners hochladen
   (index.html, favicon.svg, README.md und den Ordner `games/` mit Unterordnern).
   Wichtig: die Ordnerstruktur beibehalten.
3. **Settings → Pages** → Source: „Deploy from a branch" → Branch `main` / `/ (root)` → Save.
4. ~1 Minute warten. Seite ist live unter der oben genannten URL.
5. Jede spätere Änderung: Datei im Repo ersetzen → nach ~1 Min live.

## Kontaktformular aktivieren (Web3Forms, kostenlos)

Das Formular auf der Startseite (`index.html`, Abschnitt „Kontakt") braucht einen Access Key:

1. Auf **https://web3forms.com** die E-Mail `onpoy.studios@gmail.com` eingeben → „Create Access Key".
2. Key aus der Bestätigungs-E-Mail kopieren.
3. In `index.html` die Zeile suchen:
   `<input type="hidden" name="access_key" value="DEIN_WEB3FORMS_ACCESS_KEY">`
   und `DEIN_WEB3FORMS_ACCESS_KEY` durch den echten Key ersetzen.
4. Datei speichern / im Repo aktualisieren.

Nachrichten kommen dann als E-Mail an onpoy.studios@gmail.com (Free-Tarif: 250 / Monat).
Bis der Key gesetzt ist, zeigt das Formular einen Hinweis auf die E-Mail-Adresse.

## App Store Connect

- **Datenschutz-URL (Pflicht):** `https://<name>.github.io/onpoy-studios/games/trend-or-flop/datenschutz.html`
- **Support-URL (Pflicht):** `https://<name>.github.io/onpoy-studios/games/trend-or-flop/`
- **Marketing-URL (optional):** `https://<name>.github.io/onpoy-studios/`

## Neues Spiel hinzufügen

1. Ordner `games/<neues-spiel>/` anlegen, `index.html` + Rechtstexte hineinlegen
   (Aufbau wie bei `trend-or-flop`).
2. In `index.html` im Abschnitt `<section ... id="apps">` eine weitere
   `<a class="game-card" href="games/<neues-spiel>/"> … </a>` ergänzen.

## Eigene Domain (später)

Settings → Pages → Custom domain → z. B. `onpoystudios.com`.
Danach die URLs in App Store Connect anpassen.
