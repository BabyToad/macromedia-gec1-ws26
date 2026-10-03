# Kursvorlage – Game Engines & Coding 1 (WiSe 2026/27)

Vorlage für das eigene Projekt im Kurs **Game Engines & Coding 1** an der Hochschule Macromedia,
Leipzig. Daraus entsteht ein eigenes Repository, in dem das Spiel gebaut wird.

**Anleitung:** <https://www.allknivesnobagel.com/teaching/gec1/guides/create-project/>

## Vorlage benutzen

1. Oben rechts auf **Use this template** > **Create a new repository** klicken.
2. Owner: der eigene GitHub-Name. Name: z. B. `gec1-nachname`. **Private** auswählen.
3. Im neuen Repository: **Code** > **Open with GitHub Desktop**, dann nach `C:\Unity\`
   (Windows) bzw. `~/Unity/` (Mac) klonen.
4. Unity Hub > **Add** > **Add project from disk** > den geklonten Ordner wählen.
5. In Unity: **Kurs > Setup prüfen**.

## Inhalt

| Datei / Ordner | Wofür |
|---|---|
| `Assets/`, `Packages/`, `ProjectSettings/` | ein leeres Unity-Projekt: Unity 6000.3.15f1, Vorlage Universal 3D (URP) |
| `.gitignore` | hält Unitys Zwischendateien (`Library/`, `Temp/` …) aus Git heraus |
| `.gitattributes` | einheitliche Zeilenenden für Windows und Mac |
| `AGENTS.md` | Regeln für den KI-Agenten (Copilot, Codex, Claude Code) |
| `CLAUDE.md` | verweist Claude Code auf `AGENTS.md` |
| `DOKUMENTATION.md`, `bilder/` | Gerüst für die Dokumentation, wächst mit dem Projekt; Screenshots mit Datum in `bilder/` |
| `KI-VERZEICHNIS.md` | das KI-Verzeichnis (Pflicht laut KI-Richtlinie der Hochschule), kommt in den Anhang der Dokumentation |
| `Packages/manifest.json` | bindet das Kurs-Paket `de.macromedia.gec1` per Git ein (Menü **Kurs > Setup prüfen**); dafür muss Git installiert sein |
| `.vscode/` | Einstellungen für VS Code und die Unity-Erweiterung |

Diese Dateien bitte nicht löschen. `AGENTS.md` darf um eigene Regeln für das Projekt ergänzt
werden.

## Jonas Zugriff geben (freiwillig)

Damit Jonas ins Projekt schauen kann: **Settings** > **Collaborators** > **Add people** >
`BabyToad`. Das ist freiwillig und keine Bedingung für den Kurs. Bei Fragen hilft es aber.
