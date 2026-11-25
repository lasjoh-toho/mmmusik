# mmmusik

Eine Web-App zum Klavierlernen: Songs laden, die Noten fallen als farbige Balken auf eine Klaviatur zu, und du spielst sie auf deinem MIDI-Keyboard mit.

**Direkt im Browser öffnen:** `index.html` (eine einzige Datei, keine Installation; für die Notenansicht wird VexFlow vom CDN geladen). Für die Verbindung zum Keyboard Chrome, Edge oder Opera verwenden.

## Funktionen

- **Notenregen**: farbige Balken über einer Klaviatur, Farben als Regenbogen pro Oktave (C rot bis H violett, Halbtöne dunkler) oder nach Hand.
- **Regen / Straße**: ein Knopf für beides. Fährst du darüber, öffnet sich ein Schieberegler: ganz oben fallen die Noten als Regen von oben, je weiter du ihn nach unten ziehst, desto flacher kommen sie wie auf einer Straße aus der Tiefe auf dich zu. Der Knopf heißt dann „Straße“, ganz oben „Regen“. Der Knopf „Tasten“ darunter wählt, ob die Klaviatur die Perspektive fortsetzt oder senkrecht bleibt.
- **Farbnoten**: Klaviersystem mit kräftig-dunklen farbigen Notenköpfen und Längen-Schweifen. Eine kommende Note kündigt sich wie eine brennende Lunte an: ab Höhe der schwarzen Tasten wandert ihre Farbe die Taste hinauf und wird dabei kräftiger; den Vorlauf stellt in den Notenansichten derselbe Mini-Knopf ein, der im Notenregen die Ziellinie regelt.
- **Leuchtstreifen**: Ist die Note fällig, kommt die Farbe oben an und bleibt als kräftiger Streifen mit Leuchten nach oben stehen, solange die Taste gehalten werden soll; triffst du sie richtig, blitzt das Leuchten auf.
- **Noten**: echter Notensatz (VexFlow) mit Notenwerten, Balken, Pausen, Vorzeichen und farbigen Notenköpfen; Swing-Achtel werden wie in Jazz-Noten gerade notiert.
- **MIDI-Keyboard** per Web MIDI, mit Geräte- und Kanalwahl, Transponierung und Haltepedal. Ziellinie und Vorlauf sitzen als kleiner Knopf in der unteren Leiste. Ohne Keyboard gehen die Bildschirmtasten und die Computertastatur (`A W S E D F T G Z H U J K`, `Y`/`X` für die Oktave).
- **Drei Modi**
  - *Zuhören*: die App spielt alles vor.
  - *Üben*: der Song wartet, bis du die richtigen Tasten drückst; die nächsten Tasten leuchten.
  - *Highscore*: Echtzeit mit Punkten (Perfekt / Gut / Okay), Kombo-Faktor bis ×4, Note S bis D und Bestenliste pro Song (im Browser gespeichert).
- **Links / Beide / Rechts**: Übe nur eine Hand; die andere spielt die App als Begleitung.
- **Drehregler in der Kopfleiste** für Tempo und drei Lautstärken: *Du* (dein Spiel), *Vorlage* (wie es klingen soll) und *Begleitung*. Sie zeigen den Wert in Prozent und werden beim Darüberfahren zum senkrechten Schieberegler.
- **Zoom auf Tastaturbereiche**: Ausschnitt verschieben und vergrößern (Buttons, Mausrad, Shift+Mausrad, Zwei-Finger-Geste), „Auto“ passt den Ausschnitt an den Song an. War zu stark gezoomt, wächst der Bereich beim Start automatisch auf den Umfang des Liedes.
- **Songs**
  - Suche nach frei lizenzierten MIDI-Dateien auf Wikimedia Commons direkt in der App.
  - Eigene `.mid`-Dateien per Drag & Drop, Dateiauswahl oder URL.
  - Eingebaute Lieder: sechs gemeinfreie Klassiker und Kinderlieder plus Jazz & Ragtime (Swing-Blues mit Walking Bass, When the Saints Go Marching In, The Entertainer).
  - Pro Stimme wählbar: rechte Hand, linke Hand, Begleitung oder stumm.
- Klangfarben Flügel, E-Piano und Jazz-Orgel.
- Ziellinie: dünne Linie unter jeder Note, die zur Taste zeigt (an der Note kräftig, zur Taste hin auslaufend); Länge über den Mini-Regler neben der Ansicht.
- **Noten-Editor** (Stift-Knopf unten): korrigiert Noten in der Farbnoten-Ansicht. Korrekturen werden als eigene Version in der Bibliothek gespeichert, das Original bleibt unverändert.
  - Pfeiltasten bewegen die Auswahl (links/rechts zur nächsten Note, hoch/runter durch den Akkord).
  - Shift + Pfeile verschieben die Note: hoch/runter in der Tonhöhe, links/rechts um ein Sechzehntel in der Zeit.
  - Eine Note nach oben oder unten ziehen ändert die Tonhöhe, nicht die Zeit; der Notenname steht dabei über der Note.
  - Mit der rechten Maustaste nach rechts oder links ziehen, oder die Zahlen `1` `2` `4` `8` `6` (Ganze, Halbe, Viertel, Achtel, Sechzehntel), ändern die Dauer; `.` macht sie punktiert.
  - `+` und dann Buchstaben (`C D E F G A H`, `B` = B♭) fügen Noten nach der Auswahl ein, `#` erhöht, `−` fügt eine Pause ein. Die folgenden Noten derselben Hand rücken dabei nach hinten.
  - `Entf` löscht, `Strg+Z` macht rückgängig, `Esc` beendet.
- **Lehrer-Modus (Aufnahme)**: Der rote Punkt (oder R) blendet die Noten aus und zeigt ein Metronom. Tempo (auch per Tippen), Takt (2/4, 3/4, 4/4, 6/8), Einzählen (aus, 1 oder 2 Takte) und Klick (immer, nur beim Einzählen, stumm) sind einstellbar. Nach dem Einzählen läuft die Aufnahme taktgenau; Auftakte bleiben erhalten. So spielt die Lehrerin ein Stück ein, und der Schüler übt es danach mit Notenregen, Farbnoten oder Notensatz, auf Wunsch mit demselben Metronom-Klick. Zeitpunkt, Anschlagstärke und Haltepedal bleiben so erhalten, wie gespielt wurde. Aufnahmen werden im Browser gespeichert, lassen sich umbenennen, als Notenregen abspielen und als .mid-Datei mit Tempo und Taktart herunterladen.
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
