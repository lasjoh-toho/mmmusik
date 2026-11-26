# mmmusik

Eine Web-App zum Klavierlernen: Songs laden, die Noten fallen als farbige Balken auf eine Klaviatur zu, und du spielst sie auf deinem MIDI-Keyboard mit.

**Direkt im Browser öffnen:** `index.html` (eine einzige Datei, keine Installation; für die Notenansicht wird VexFlow vom CDN geladen). Für die Verbindung zum Keyboard Chrome, Edge oder Opera verwenden.

## Funktionen

- **Notenregen**: farbige Balken über einer Klaviatur, Farben als Regenbogen pro Oktave (C rot bis H violett, Halbtöne dunkler) oder nach Hand.
- **Regen / Straße**: ein Knopf für beides. Fährst du darüber, öffnet sich ein Schieberegler: ganz oben fallen die Noten als Regen von oben, je weiter du ihn nach unten ziehst, desto flacher kommen sie wie auf einer Straße aus der Tiefe auf dich zu. Der Knopf heißt dann „Straße“, ganz oben „Regen“. Der Knopf „Tasten“ darunter wählt, ob die Klaviatur die Perspektive fortsetzt oder senkrecht bleibt.
- **Farbnoten**: Klaviersystem mit kräftig-dunklen farbigen Notenköpfen und Längen-Schweifen. Eine kommende Note kündigt sich wie eine brennende Lunte an: ab Höhe der schwarzen Tasten wandert ihre Farbe die Taste hinauf und wird dabei kräftiger; den Vorlauf stellt in den Notenansichten derselbe Mini-Knopf ein, der im Notenregen die Ziellinie regelt.
- **Leuchtstreifen**: Ist die Note fällig, kommt die Farbe oben an und bleibt als kräftiger Streifen mit Leuchten nach oben stehen, solange die Taste gehalten werden soll; triffst du sie richtig, blitzt das Leuchten auf.
- **Blatt**: derselbe Notensatz wie auf einem Notenblatt, Zeile für Zeile über die ganze Breite; die Zeilen wandern beim Spielen langsam nach oben, sodass die nächste Zeile schon zu sehen ist.
- **Gleichmäßige Marke in Noten und Blatt**: Die Noten stehen dort, wo ihre Zeit ist (jedes Viertel gleich breit), daher läuft die Marke ohne Haken mit immer gleichem Tempo, auch über Taktstriche.
- **Noten**: echter Notensatz (VexFlow) mit Notenwerten, Balken, Pausen, Vorzeichen und farbigen Notenköpfen; Swing-Achtel werden wie in Jazz-Noten gerade notiert.
- **MIDI-Keyboard** per Web MIDI, mit Geräte- und Kanalwahl, Transponierung und Haltepedal. „Keyboard suchen“ hört auf allen Geräten und Kanälen und stellt das Keyboard ein, auf dem du die erste Taste drückst. Verweigert der Browser den Zugriff, steht direkt dort, wie man ihn erlaubt, mit einem Knopf, um die App als ZIP herunterzuladen. Ziellinie und Vorlauf sitzen als kleiner Knopf in der unteren Leiste. Ohne Keyboard gehen die Bildschirmtasten und die Computertastatur (`A W S E D F T G Z H U J K`, `Y`/`X` für die Oktave).
- **Drei Modi**
  - *Zuhören*: die App spielt alles vor.
  - *Üben* (Auswahl): *Warten* hält den Song an, bis alle Töne des Moments gedrückt sind; die nächsten Tasten leuchten. *50 %*, *75 %*, *90 %* und *100 %* lassen den Song im gewählten Tempo laufen, gezählt werden Treffer und verpasste Töne, ohne Punkte.
  - *Highscore*: Echtzeit mit Punkten, Genauigkeit (Perfekt / Gut / Okay), Kombo-Faktor bis ×4, Note S bis D und Bestenliste pro Song (im Browser gespeichert).
- **Hände**: zwei Hand-Symbole (von oben gesehen). Voll heißt: du spielst diese Hand, Umriss heißt: die App spielt sie. Klick schaltet um.
- **Vollbild**: Knopf oben rechts.
- **Kopfleiste**: Tempo als Schieberegler (25–110 %) mit − und + an den Enden und drei Drehregler für die Lautstärke: *Vorlage* (wie es klingen soll), *Du* (dein Spiel) und *Begleitung*. Sie zeigen den Wert in Prozent und werden beim Darüberfahren zum senkrechten Schieberegler.
- **Übersichtsleiste** oben über den Noten, schmal und halb durchsichtig; beim Darüberfahren wird sie groß: das ganze Lied als kleine Notenrolle, der gerade sichtbare Ausschnitt ist hervorgehoben. Ausschnitt ziehen verschiebt die Stelle; ein Klick springt dorthin und zeigt die Noten, bis du weiterspielst.
- **Zoom auf Tastaturbereiche**: Ausschnitt verschieben und vergrößern (Buttons, Mausrad, Shift+Mausrad, Zwei-Finger-Geste), „Auto“ passt den Ausschnitt an den Song an. War zu stark gezoomt, wächst der Bereich beim Start automatisch auf den Umfang des Liedes.
- **Songs**
  - Suche nach frei lizenzierten MIDI-Dateien auf Wikimedia Commons direkt in der App.
  - Eigene `.mid`-Dateien per Drag & Drop, Dateiauswahl oder URL.
  - **Mein Ordner**: Mit „Ordner öffnen“ zeigt die App alle MIDI-Dateien eines Ordners (auch Unterordner). Chrome und Edge merken sich den Ordner, beim nächsten Start reicht ein Klick. Läuft die App auf GitHub Pages oder einem anderen Webserver, findet sie MIDI-Dateien im Ordner `songs/` neben `index.html` von selbst.
  - Eingebaute Lieder: sechs gemeinfreie Klassiker und Kinderlieder plus Jazz & Ragtime (Swing-Blues mit Walking Bass, When the Saints Go Marching In, The Entertainer).
  - Pro Stimme wählbar: rechte Hand, linke Hand, Begleitung oder stumm.
- **Alles bleibt im Browser**: Aufnahmen, bearbeitete Versionen, zuletzt geöffnete Dateien, Bestenlisten und Einstellungen. Jeder Song lässt sich einzeln löschen oder als .mid herunterladen; unter Einstellungen → „Gespeichert in diesem Browser“ gibt es „Alles exportieren“ (Sicherung als .json), „Sicherung laden“ und „Alles löschen“.
- **Instrumente**: Der Knopf vor dem Tempo zeigt das aktuelle Instrument als Icon und öffnet in der Mitte des Fensters eine nach Gruppen sortierte Auswahl mit allen Instrumenten und Schlagzeug-Stilen (auch unter Einstellungen → Klang).
  - Klavier: Konzertflügel aus echten Aufnahmen, Flügel (synthetisch), Cembalo.
  - Elektrisch: E-Piano im Rhodes- und im Wurlitzer-Stil, Clavinet, Jazz-Orgel.
  - Synthesizer: Analog-Lead und Analog-Bass im Moog-Stil (verstimmte Sägezähne, Sub-Oszillator, resonantes Tiefpassfilter mit Hüllkurve), Synth-Brass, Flächenklang, Theremin (fast reiner Ton, gleitet immer vom letzten Ton zum nächsten, mit wachsendem Vibrato; spielt einstimmig).
  - Streicher (echte Aufnahmen): Streichorchester (Violinen, Celli und Kontrabass je nach Lage, leicht verstimmt gedoppelt), Violine, Cello, Kontrabass.
  - Bläser (echte Aufnahmen): Blechbläser-Satz (Trompete, Horn, Posaune, Tuba je nach Lage), Trompete, Posaune, Waldhorn, Tuba, Querflöte, Klarinette, Saxophon.
  - Gitarre (echte Aufnahmen): Konzertgitarre.
  - Glissando: Bei Streichern und Posaune gleitet ein Ton, der gedrückt wird, während der vorige noch gehalten ist, von dort hinüber (gleichzeitig gedrückte Akkorde nicht). Das Pitch-Bend-Rad eines MIDI-Keyboards biegt die Orchester-Instrumente um bis zu zwei Halbtöne.
  - Die Orchester-Aufnahmen liegen in `samples/orchester` (Lizenz CC BY 3.0, Quelle in `samples/orchester/LIZENZ.md`) und werden beim ersten Ton geladen; lange Töne werden per Schleife gehalten. Bis sie geladen sind, klingt ein synthetischer Ersatz.
  - Weitere: Vibraphon, Marimba, Harfe, Spieluhr.
  - Aus aller Welt: Kalimba, Koto, Sitar, Steeldrum, Gamelan-Glocken, Panflöte.
  - Der Konzertflügel spielt echte Klavieraufnahmen (*Salamander Grand Piano* von Alexander Holm, Lizenz CC BY 3.0). Sie liegen im Ordner `samples/salamander` neben der App. Läuft die App ohne Webserver direkt aus einem Ordner, holt sie die Aufnahmen aus dem Programmordner (nach „Ordner öffnen“) oder aus dem Internet; „Flügel-Aufnahmen im Programmordner speichern“ legt sie dann dort ab.
- **Schlagzeug zur Begleitung**: Pop, Rock, Swing (Besen-Ride), Shuffle/Blues, Bossa Nova, Walzer oder Percussion (Conga, Shaker, Cowbell). Das Schlagzeug folgt Takt und Tempo des Liedes und läuft über den Regler „Begleitung“. Schlagzeugspuren aus MIDI-Dateien klingen jetzt als Schlagzeug mit; „Aus“ schaltet alles ab.
  - **Eigene Pattern**: „＋ Eigenes Pattern“ in der Instrument-Auswahl öffnet ein Raster mit Sechzehnteln für Crash, Ride, Hi-Hat, Toms, Snare, Rimshot, Klatschen, Bass, Shaker und Kuhglocke, in 3/4 oder 4/4 und über einen oder zwei Takte. Ein Klick setzt einen Schlag, weitere Klicks machen ihn betont, leise und wieder leer. Probehören mit eigenem Tempo; das Pattern wird sofort gespeichert und erscheint als eigener Schlagzeug-Stil. Nochmal auf ein ausgewähltes eigenes Pattern klicken öffnet es wieder zum Bearbeiten. Der Editor füllt das Fenster; über „＋ Sound als Spur hinzufügen“ kommen weitere Klänge dazu (Toms, Becken, Bongos, Congas, Timbales, Agogo, Claves, Holzblock, Tamburin und mehr), ✕ am Namen entfernt eine Spur. Ein Swing-Regler verschiebt jedes zweite Sechzehntel bis hin zum Triolen-Gefühl. Ein Klick auf einen gesetzten Schlag öffnet ihn groß im Effekt-Editor: Lautstärke, Timing (früher/später), Tonhöhe, Ausklang, Equalizer (Bässe, Mitten, Höhen), Echo mit Abstand 1/4, 1/8, 1/8-Triole oder 1/16, Rauschen (dunkel, mittel oder hell) und Wirbel (2–4 Schläge). „Kopieren“ (oder Strg/⌘+C) merkt sich einen Schlag samt allen Effekten; Shift+Klick auf ein beliebiges Feld, „Einsetzen“ oder Strg/⌘+V setzt ihn dort ein.
- Ziellinie: dünne Linie unter jeder Note, die zur Taste zeigt (an der Note kräftig, zur Taste hin auslaufend); Länge über den Mini-Regler neben der Ansicht.
- Alle Noten sind so breit wie eine schwarze Taste und gleiten auf eigenen, dunkleren Spuren heran.
- Auf der Straße sind die Noten kleine erhabene Blöcke mit Schatten. Klingende Noten stehen vorn ein wenig über die Kante der Tasten. Das Leuchten über einer fälligen Taste ist rund und in der Mitte am hellsten; ist die Note vorbei, blendet es langsam aus.
- **Noten-Editor** (Feder unten oder die Feder „Bearbeiten“ rechts unten über den Noten): korrigiert Noten in den Ansichten Farbnoten, Noten und Blatt (aus Regen und Straße wechselt er zu Farbnoten). Eine Note anklicken wählt sie aus. Korrekturen werden als eigene Version in der Bibliothek gespeichert, das Original bleibt unverändert.
  - Pfeiltasten bewegen die Auswahl (links/rechts zur nächsten Note, hoch/runter durch den Akkord).
  - Shift + Pfeile verschieben die Note: hoch/runter in der Tonhöhe, links/rechts um ein Sechzehntel in der Zeit.
  - Eine Note nach oben oder unten ziehen ändert die Tonhöhe, nicht die Zeit; der Notenname steht dabei über der Note.
  - Mit der rechten Maustaste nach rechts oder links ziehen, oder die Zahlen `1` `2` `4` `8` `6` (Ganze, Halbe, Viertel, Achtel, Sechzehntel), ändern die Dauer; `.` macht sie punktiert.
  - `+` und dann Buchstaben (`C D E F G A H`, `B` = B♭) fügen Noten nach der Auswahl ein, `#` erhöht, `−` fügt eine Pause ein. Die folgenden Noten derselben Hand rücken dabei nach hinten.
  - `S` teilt eine gebundene (übergebundene) Note an der Taktlinie oder am Schlag in zwei Noten, `V` verbindet sie mit der nächsten gleichen Note.
  - `Alt` + links/rechts verschiebt die gewählte Note und alles danach (in allen Stimmen) um ein Sechzehntel; mit `Shift` dazu um einen ganzen Takt. So entsteht Platz, um ein Stück einzufügen. Zurück geht es nur, wenn davor Platz frei ist.
  - `Entf` löscht, `Strg+Z` macht rückgängig, `Esc` beendet.
- **Spuren** (Ebenen-Knopf unten oder das Tonband vor „mmmusik“): Rechts neben dem Menü zeigt ein Sequenzer jede Spur als Band über die ganze Breite, mit Taktstrichen und Abspielmarke; ein Klick springt dorthin. Beim Aufnehmen erscheint die neue Spur live. Der Notenknopf an einer Spur zeigt nur diese Spur als Notenblatt (und druckt sie so als PDF). „Neues Stück aufnehmen“ (auch „Neuen Song einspielen“ oben in der Songliste) beginnt ein leeres Stück im Tempo und Takt des Metronoms. Ein Menü links, das die Tasten frei lässt, zeigt alle Spuren des Lieds mit Name und Rolle. „Neue Spur aufnehmen“ zählt einen Takt ein und spielt das Lied ab, während du eine weitere Spur dazu spielst. So entstehen Stücke aus mehreren Spuren, gespeichert unter „Meine Aufnahmen“.
- **Noten als PDF**: Der Knopf oben im Seitenmenü druckt das ganze Lied als Notenblatt; im Druckdialog „Als PDF speichern“ wählen.
- **Einspielen (Aufnahme)**: Der rote Punkt (oder R) blendet die Noten aus und zeigt ein Metronom. Tempo (Drehknopf auf dem Fuß des Metronoms, auch per Tippen), Takt (2/4, 3/4, 4/4, 6/8), Einzählen (aus, 1 oder 2 Takte), Klick (immer, nur beim Einzählen, stumm) und die Lautstärke des Klicks sind einstellbar. Ist ein Lied geladen, wählst du unter „Dazu“ zwischen Metronom und Spuren: Mit „Spuren“ spielt das Lied mit, und du nimmst eine neue Spur dazu auf. Nach dem Einzählen läuft die Aufnahme taktgenau; Auftakte bleiben erhalten. So spielt die Lehrerin ein Stück ein, und der Schüler übt es danach mit Notenregen, Farbnoten oder Notensatz, auf Wunsch mit demselben Metronom-Klick. Zeitpunkt, Anschlagstärke und Haltepedal bleiben so erhalten, wie gespielt wurde. Aufnahmen werden im Browser gespeichert, lassen sich umbenennen, als Notenregen abspielen und als .mid-Datei mit Tempo und Taktart herunterladen.
- Springen, Notennamen (deutsch mit H oder englisch).

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

## Lizenz

mmmusik steht unter einer Bildungslizenz (siehe [LICENSE.md](LICENSE.md)):
- Schulen und Bildungseinrichtungen dürfen die App kostenlos auf ihrer eigenen Hardware installieren und im Unterricht nutzen.
- Privatpersonen dürfen sie zum eigenen Üben nutzen.
- Kommerzielle Anbieter brauchen eine ausdrückliche schriftliche Genehmigung.

Die Klavier- und Orchester-Aufnahmen stehen unter CC BY 3.0, VexFlow unter der MIT-Lizenz.
