# mmmusik

Eine Web-App zum Klavierlernen: Songs laden, die Noten fallen als farbige Balken auf eine Klaviatur zu, und du spielst sie auf deinem MIDI-Keyboard mit.

**Direkt im Browser öffnen:** `index.html` (eine einzige Datei, keine Installation). Für die Verbindung zum Keyboard Chrome, Edge oder Opera verwenden.

## Funktionen

- **Notenregen**: farbige Balken über einer Klaviatur, Farben nach Tonhöhe (Quintenzirkel) oder nach Hand.
- **Farbige Noten**: Ansicht als Klaviersystem (Violin- und Bassschlüssel) mit farbigen Notenköpfen, oder beides übereinander.
- **MIDI-Keyboard** per Web MIDI, mit Geräte- und Kanalwahl, Transponierung und Haltepedal. Ohne Keyboard gehen die Bildschirmtasten und die Computertastatur (`A W S E D F T G Z H U J K`, `Y`/`X` für die Oktave).
- **Drei Modi**
  - *Zuhören*: die App spielt alles vor.
  - *Üben*: der Song wartet, bis du die richtigen Tasten drückst; die nächsten Tasten leuchten.
  - *Highscore*: Echtzeit mit Punkten (Perfekt / Gut / Okay), Kombo-Faktor bis ×4, Note S bis D und Bestenliste pro Song (im Browser gespeichert).
- **Zoom auf Tastaturbereiche**: Ausschnitt verschieben und vergrößern (Buttons, Mausrad, Shift+Mausrad, Zwei-Finger-Geste), „Auto“ passt den Ausschnitt an den Song an.
- **Songs**
  - Suche nach frei lizenzierten MIDI-Dateien auf Wikimedia Commons direkt in der App.
  - Eigene `.mid`-Dateien per Drag & Drop, Dateiauswahl oder URL.
  - Sechs eingebaute, gemeinfreie Lieder (Alle meine Entchen bis Für Elise).
  - Pro Stimme wählbar: rechte Hand, linke Hand, Begleitung oder stumm.
- Tempo 25–150 %, Springen, Notennamen (deutsch mit H oder englisch).

## Veröffentlichen mit GitHub Pages

Settings → Pages → *Deploy from a branch* → `main` / `(root)`. Danach läuft die App unter `https://<benutzer>.github.io/mmmusik/`.

## Tastenkürzel

| Taste | Aktion |
| --- | --- |
| Leertaste | Start / Pause |
| Pos1 | Von vorn |
| ← / → | 5 Sekunden springen |
| ↑ / ↓ | Tempo |

`Midi.html` ist die ursprüngliche Keyboard-Testseite.
