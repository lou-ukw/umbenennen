# umbenennen?!

Interaktive Ausstellungs-App für die Ausstellung *umbenennen?!* im Mitte Museum, Berlin.

## Deployment auf GitHub Pages

### Erstmalige Einrichtung (einmalig, ca. 5 Minuten)

1. **GitHub-Konto anlegen** (falls noch nicht vorhanden): https://github.com/signup

2. **Neues Repository anlegen:**
   - Auf github.com: „New repository"
   - Name: z.B. `rename-the-street`
   - Sichtbarkeit: **Public** (für GitHub Pages kostenlos erforderlich)
   - „Create repository" klicken

3. **Datei hochladen:**
   - Im Repository auf „Add file" → „Upload files" klicken
   - `index.html` in das Fenster ziehen
   - „Commit changes" klicken

4. **GitHub Pages aktivieren:**
   - Im Repository: „Settings" → „Pages" (linke Seitenleiste)
   - Source: „Deploy from a branch"
   - Branch: `main`, Ordner: `/ (root)`
   - „Save" klicken

5. **URL:** Nach ca. 1–2 Minuten ist die App erreichbar unter:
   `https://[dein-benutzername].github.io/rename-the-street/`

---

## Inhalte anpassen

Alle Texte befinden sich direkt in der `index.html`. Öffne die Datei in einem Texteditor (z.B. VS Code, Notepad++) und suche nach:

### Szenarien-Texte
Suche nach `const SCENARIOS = [` — dort findest du alle drei Szenarien mit:
- `intro`: Einleitungstext
- `timeline`: Prozess-Chronologie
- `histFindings`: Gutachten-Befunde
- `voices`: Stimmen aus der Debatte
- `results`: Ergebnistexte je nach Entscheidung

### Galerie-Personen
Suche nach `const GALLERY_PERSONS = [` — dort stehen alle Personen für den Schildgestalter mit Kurzbiografien.

### Farben ändern
Suche nach `:root {` — dort stehen alle Farbvariablen:
- `--teal`: Primärfarbe (aktuell: umbenennen.berlin-Türkis)
- `--sign-blue`: Farbe der Straßenschilder (Berliner Blau)

---

## Kiosk-Modus auf Android-Tablet

Empfehlung: **Fully Kiosk Browser** (kostenlos im Play Store)
- URL der App eintragen
- Autostart aktivieren
- Display-Timeout deaktivieren
- Inaktivitäts-Reset läuft automatisch nach 120 Sekunden

---

## DSGVO

Die App speichert keinerlei Daten außerhalb des Browser-Arbeitsspeichers. Schilder in der Galerie existieren nur für die Dauer der Browser-Session (kein Server, kein Backend, keine Cookies). Bei Seitenneuladung oder Tablet-Neustart ist die Galerie leer.

Wenn eine session-übergreifende Galerie gewünscht wird, kann `localStorage` eingebaut werden — diese Daten bleiben dann lokal auf dem Gerät und werden nicht übertragen.

---

## Quellen

Alle historischen Inhalte basieren auf:
- Bezirksamt Mitte von Berlin, Fachbereich Kunst, Kultur und Geschichte
- berlin.de/kunst-und-kultur-mitte/geschichte/
- BVV-Beschlüsse und Amtsblatt Berlin (dokumentiert in der App)
