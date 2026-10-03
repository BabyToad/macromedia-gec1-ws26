# AGENTS.md – Regeln für KI-Agenten in diesem Projekt

Gilt für jeden Agenten: GitHub Copilot und Codex lesen diese Datei direkt, Claude Code über
`CLAUDE.md`. Regeln hier ändern, nicht in `CLAUDE.md`.

Dieses Projekt ist ein Studienprojekt im Kurs **Game Engines & Coding 1** (Macromedia
Leipzig). Die Person, die daran arbeitet, lernt gerade Unity und C#. Viele haben noch nie
programmiert. Ziel ist, dass sie versteht und steuert, was passiert – nicht nur, dass es läuft.

## Projekt

- Unity **6000.3.15f1** (Unity 6.3 LTS), Universal Render Pipeline (URP), 3D.
- Eingabe über das Paket **Input System**.
- Git über GitHub Desktop. Das Repository beginnt in diesem Ordner.
- Das Kurs-Paket `de.macromedia.gec1` kommt per Git-URL (`Packages/manifest.json`). Seine Version
  nur ändern, wenn die Person darum bittet (siehe Anleitung „Kurs-Paket aktualisieren“).

## Arbeitsweise

- Auf Deutsch antworten, in einfachen Worten. Fachbegriffe beim ersten Auftreten erklären.
- In kleinen Schritten arbeiten: eine Änderung, die sich im Spiel ausprobieren lässt. Dann
  aufhören und sagen, wie man sie testet (welche Szene, welche Taste, was passieren soll).
- Am Ende jeder Änderung nennen, **welche Dateien** angelegt oder geändert wurden und warum.
- Ist die Beschreibung unklar: nachfragen, bevor etwas gebaut wird. Vorschlagen, wie sich die
  Mechanik genauer beschreiben lässt.
- Keine Unity-APIs erfinden. Ist unklar, ob es etwas in Unity 6.3 gibt, das offen sagen.

## Code

- C#-Skripte liegen unter `Assets/Scripts/`. Ein Skript pro Komponente, Dateiname = Klassenname.
- Kurze Komponenten (unter ca. 80 Zeilen). Lieber zwei kleine als eine große.
- Jede Klasse bekommt oben einen Kommentar: was sie tut und wie man sie benutzt.
- Das **Warum** kommentieren, nicht jede Zeile. Der Code soll auch für Anfänger lesbar sein.
- Einstellbare Werte als `[SerializeField] private` Felder mit sinnvollen Standardwerten,
  damit sie sich im Inspector ändern lassen.
- Bewegung pro Frame immer mit `Time.deltaTime`; Physik in `FixedUpdate` bzw. über `Rigidbody`.

## KI-Verzeichnis

Die Hochschule verlangt ein vollständiges KI-Verzeichnis (KI-Richtlinie der Hochschule Macromedia,
28.04.2025). Es liegt in `KI-VERZEICHNIS.md`.

- Regel: Eine Zeile bekommt jede Aufgabe, bei der eine KI im Projekt etwas geändert oder erzeugt hat. Reine Fragen ohne Änderung am Projekt brauchen keine Zeile – außer die Antwort geht in die Arbeit ein.
  Beispiel: „Erkläre mir dieses Skript Zeile für Zeile“ braucht keine Zeile; übernimmt man die Erklärung in die Dokumentation, schon.
- Für jede solche Aufgabe eine Zeile an die Tabelle anhängen und der Person sagen, dass das
  passiert ist. Bestehende Zeilen nicht ändern.
- Spalten: Datum | Werkzeug | Modell/Version | Anbieter | Zweck | Dateien/System | Anmerkung.
  Beispiel: `2026-10-23 | Claude Code | <Modell> | Anthropic | Tür öffnet sich per Trigger |
  Assets/Scripts/DoorTrigger.cs | von der Person getestet`.
- Das eigene Modell so genau eintragen wie bekannt. GitHub Copilot Free/Student: „Copilot (Auto)“,
  dazu das angezeigte Modell, wenn es sichtbar ist.
- Generierte Inhalte, die ins Spiel kommen (Bilder, Audio, Texte im Spiel), bekommen eine eigene
  Zeile. Dazu einen Hinweis im Spiel oder im Abspann vorschlagen (Credit).

## Git

- Nur committen, wenn die Person darum bittet. Vorher mit `git status` und `git diff --stat`
  zeigen, was im Commit landet, und es in einem Satz erklären.
- Nur committen, was zur besprochenen Änderung gehört. `.meta`-Dateien gehören immer dazu.
- Commit-Nachrichten kurz und auf Deutsch, etwa „Tür öffnet sich beim Betreten“.
- Nur pushen, wenn die Person ausdrücklich darum bittet. Die Bitte gilt für diesen einen Push,
  nicht automatisch für den nächsten.
- Rückgängig machen mit `git revert`, nicht mit `reset`.
- Tauchen `Library/` oder `Temp/` in `git status` auf: nichts committen, die `.gitignore` ist
  kaputt. Das sagen und auf **Kurs > Setup prüfen** in Unity verweisen.

### Warum nur auf ausdrückliche Bitte

Ein Mensch bleibt in der Schleife, bis er versteht, wann es klug ist, einem Agenten das Steuer
zu überlassen. Zustimmen und aushandeln kann man nur eine Zusammenarbeit, die man versteht.
Wer gerade lernt, was ein Commit und ein Push sind, entscheidet beides noch selbst. Deshalb
erst erklären, was geplant ist, und auf ein Ja warten.

## Nicht tun

- Keine Dateien in `Library/`, `Temp/`, `Logs/`, `UserSettings/` anfassen.
- Keine `.meta`-Dateien von Hand schreiben oder löschen. Unity erzeugt sie.
- Keine Szenen (`.unity`) oder Prefabs (`.prefab`) als Text umschreiben, außer die Person bittet
  ausdrücklich darum. Stattdessen sagen, was im Editor zu klicken ist.
- Keine Pakete installieren und keine Projekteinstellungen ändern, ohne vorher zu fragen.
- Keine Git-Befehle, die Verlauf oder Dateien löschen oder überschreiben (`reset --hard`,
  `push --force`, `clean`, `checkout -- .`, `rebase`).
- Keine kostenpflichtigen Assets, nichts aus unbekannten Quellen herunterladen.
