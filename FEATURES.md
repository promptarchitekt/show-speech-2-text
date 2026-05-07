# Features

## Audioeingabe

- Audiodatei auswaehlen
- WhatsApp-Sprachnachricht ueber Teilen/Weiterleiten annehmen
- Mikrofonaufnahme starten
- Audioleiste bleibt auch im Leerzustand sichtbar

## Verarbeitung

- API-basierte Transkription
- optionaler Vergleichslauf
- robuste Verarbeitung langer Audiodateien ueber Chunking
- getrennte Ergebnisbereiche fuer Pruefung und Weiterarbeit

## Ergebnisbereiche

- Ergebnis: bereinigte Arbeitsfassung
- Original: unveraendertes Transkript
- Arbeitsfassung: optional abgeleitete Fassung
- Vergleich: Abweichungen zwischen zwei Erkennungen
- Pruefhinweise: auffaellige Stellen mit Entscheidung
- Woerterbuch: eigene und standardisierte Begriffe

## Pruefung

- Markierungen direkt im Text
- Erklaerung, warum eine Stelle geprueft werden sollte
- Vorschlag uebernehmen
- Hinweis ignorieren
- Begriff ins Woerterbuch uebernehmen
- Audiostelle erneut anhoeren

## Speichern

- manuelles Speichern ueber Disketten-Symbol
- lokaler Export
- Google-Drive-Export bei aktiver Verbindung
- Woerterbuch-Sicherung lokal oder in Google Drive
- keine automatische Speicherung direkt nach Transkription
- keine Speicherung des Originalaudios

## Google Drive

- Clerk/Google OAuth
- eingeschraenkter Scope `drive.file`
- Standardordner `PromptArchitekt/Speech-2-Text`
- Drive-Status im Header
- Reconnect-Pfad bei fehlendem Scope oder abgelaufener Verbindung

## Mobile Nutzung

- kompakter Header
- Dropdown fuer Ergebnisbereiche
- Hilfe direkt erreichbar
- App bleibt auf Handy und Desktop verwendbar

## Nicht-Ziele

- keine automatische Inhaltsinterpretation
- keine vollautomatische Korrektur ohne Nutzerentscheidung
- keine freie Drive-Ordnerauswahl im MVP
- kein Audioarchiv
