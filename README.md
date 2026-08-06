# Pitlane Log

Eine installierbare Web-App (PWA) zum Erfassen und Vergleichen von Trackday-Daten:
Kopfdaten, Turns, Reifen, Fahrgefühl und Notizen — läuft offline, Daten bleiben nur
auf deinem Gerät (im Browser-Speicher, `localStorage`).

## Enthaltene Dateien

- `index.html` — die App selbst (HTML/CSS/JS, keine Abhängigkeiten)
- `manifest.json` — macht die App "installierbar" (Name, Icon, Farben)
- `sw.js` — Service Worker, damit die App auch offline funktioniert
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` — App-Icons

## Kostenlos online stellen mit GitHub Pages

1. Gehe auf [github.com](https://github.com) und erstelle (falls noch nicht vorhanden)
   einen kostenlosen Account.
2. Erstelle ein neues **Repository**, z. B. `pitlane-log`. Öffentlich reicht.
3. Lade alle Dateien aus diesem Ordner hoch: "Add file" → "Upload files" →
   alle 6 Dateien reinziehen → "Commit changes".
4. Im Repository: **Settings → Pages**. Bei "Source" wähle den Branch `main`
   und Ordner `/ (root)`. Speichern.
5. Nach 1–2 Minuten ist die App erreichbar unter
   `https://DEIN-NUTZERNAME.github.io/pitlane-log/`
   (Link steht auch oben in den Pages-Einstellungen).

## Auf dem iPhone installieren

1. Öffne den Link aus Schritt 5 oben in **Safari** (wichtig: nicht Chrome —
   "Zum Home-Bildschirm" für Web-Apps funktioniert auf iOS nur in Safari).
2. Tippe auf das Teilen-Symbol.
3. "Zum Home-Bildschirm" auswählen.

Die App startet danach wie eine normale App, mit eigenem Icon, ohne Adressleiste,
und funktioniert auch ohne Internetverbindung (dank Service Worker).

## Alternative: Netlify (per Drag & Drop, kein Git nötig)

Falls dir GitHub zu umständlich ist: Auf [app.netlify.com/drop](https://app.netlify.com/drop)
kannst du den ganzen Ordner per Drag & Drop hochladen und bekommst sofort eine Live-URL.

## Wichtig zu wissen

- **Die Daten liegen nur in diesem einen Browser auf diesem einen Gerät.**
  Kein Cloud-Sync. Wenn du Safari-Daten löschst oder die App über einen anderen
  Browser/ein anderes Gerät öffnest, siehst du eine leere App.
- Ein Backup ist aktuell nicht eingebaut. Wenn dir das wichtig wird
  (z. B. Export als CSV/JSON zum Sichern), lohnt sich das als nächster Ausbauschritt.
- Willst du etwas ändern (Felder, Design, neue Funktionen): `index.html` ist eine
  einzelne Datei, die du direkt in einem Editor wie VS Code bearbeiten kannst.
