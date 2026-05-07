# PromptArchitekt Speech-2-Text

> Mobile Sprachnachrichten in pruefbaren Text verwandeln - mit Markierungen,
> Woerterbuch, Google-Drive-Ablage und einem Workflow, der vom Handy bis zum
> Rechner weitergeht.

`Next.js` `TypeScript` `OpenAI API` `Clerk` `Google Drive` `Vercel` &nbsp;·&nbsp; Status: MVP

**Live:** https://speech.promptarchitekt.de  
**Code:** privat - dieses Repository zeigt Produkt, Arbeitsweise und Ergebnis, nicht den Quellcode.

---

## Ausloeser

Sprachnachrichten sind praktisch, aber sie bleiben oft im falschen Medium
stecken: am Handy aufgenommen, in WhatsApp weitergeleitet, spaeter am Rechner
fuer Angebote, E-Mails, Dokumentation oder interne Klaerung gebraucht.

Der eigentliche Bedarf war nicht nur "Audio in Text", sondern ein kleiner
Arbeitsbereich:

- Audio direkt aus dem mobilen Teilen-Workflow annehmen
- Text erzeugen
- auffaellige Stellen sichtbar machen
- Ergebnis bewusst pruefen
- erst danach speichern oder weiterverarbeiten

## Was es tut

Speech-2-Text nimmt Audiodateien und geteilte WhatsApp-Sprachnachrichten an,
transkribiert sie und erzeugt eine pruefbare Arbeitsfassung. Das Ergebnis kann
kopiert, bearbeitet, lokal gespeichert oder in Google Drive abgelegt werden.

Die App speichert bewusst nicht automatisch nach der Transkription. Der
Speichervorgang bleibt eine Nutzerentscheidung ueber das Disketten-Symbol.

## Meine Rolle

Produktidee · Prozessdesign · Architektur · KI-Co-Build · UI-Iteration ·
OAuth-/Drive-Anbindung · Deployment · laufende Verbesserung

## Warum dieses Projekt zaehlt

Das Projekt zeigt die Entwicklung von einem Verwaltungsproblem zu einer
konkreten Web-App: nicht abstrakte KI-Beratung, sondern ein realer Workflow,
der Medienbrueche reduziert.

Der fachliche Hintergrund liegt nicht in einer klassischen Entwicklerausbildung.
Der Wert entsteht aus Verwaltungspraxis, Prozessverstaendnis und der Faehigkeit,
ein wiederkehrendes Arbeitsproblem bis zur nutzbaren Anwendung durchzudenken.

## Kernfunktionen

### Mobile Audioannahme

- Audiodateien per Dateiauswahl verarbeiten
- WhatsApp-Sprachnachrichten ueber Teilen/Weiterleiten an die App uebergeben
- geteilte Audiodaten browserseitig wieder als Datei verarbeiten
- neutrale Audioleiste auch im Leerzustand

### Transkription und Qualitaetskontrolle

- API-basierte Transkription fuer die gehostete Web-App
- optionaler Vergleichslauf fuer eine zweite Erkennung
- Chunking fuer lange Audiodateien
- getrennte Bereiche fuer Ergebnis, Original, Arbeitsfassung, Vergleich,
  Pruefhinweise und Woerterbuch

### Pruefhinweise

- markierte Stellen direkt im Ergebnistext
- klare Trennung zwischen aktuellem Text und Vorschlag
- Vorschlag uebernehmen oder Hinweis ignorieren
- Begriffe ins Woerterbuch uebernehmen, ohne den aktuellen Text automatisch zu
  veraendern
- betroffene Audiostelle optional erneut anhoeren

### Woerterbuch

- Standardbegriffe fuer wiederkehrende Fachsprache
- eigenes Browser-Woerterbuch
- Sicherung lokal als TXT oder bei aktivem Google Drive als Markdown

### Google Drive

- Anmeldung und Google-Verbindung ueber Clerk
- eingeschraenkter Google-Drive-Scope `drive.file`
- Standardordner `PromptArchitekt/Speech-2-Text`
- Speicherung des Ergebnisses, nicht des Originalaudios
- Drive-Status im Header sichtbar

## Entscheidungen

**Kein automatisches Speichern**  
Die App transkribiert, aber sie entscheidet nicht ungefragt ueber Ablage. Das
Speichern erfolgt bewusst per Klick auf das Disketten-Symbol.

**Google Drive statt Audio-Archiv**  
Gespeichert wird das Ergebnis, nicht das Originalaudio. Das reduziert
Redundanz und vermeidet unnoetige sensible Audiodaten in der Ablage.

**Pruefung vor Weitergabe**  
Speech-to-Text bleibt fehleranfaellig, besonders bei Namen, Zahlen und
Fachbegriffen. Deshalb zeigt die App Pruefhinweise als Entscheidungspunkte, nicht
als automatische Wahrheit.

**Showroom ohne Quellcode**  
Das oeffentliche Repository zeigt Produktstand, Arbeitslogik und
Entwicklungsleistung. Der produktive App-Code bleibt im privaten
Entwicklungsrepo.

## Ergebnis

- Live-App unter eigener Subdomain
- mobiler WhatsApp-Share-Workflow funktioniert ohne temporaeren Pfadbruch
- Google-Drive-Ablage fuer Ergebnisse und Woerterbuch
- Changelog und Feature-Liste als wiederverwendbare Produktdokumentation
- klare Abgrenzung: Transkriptions-QA statt Inhaltsinterpretation

## Entwicklungslinie

```text
Verwaltungspraxis
  -> Medienbruch erkannt
  -> erster Toolbau mit ChatGPT / Excel / VBA
  -> Web-App-Stack mit Next.js, TypeScript, Tailwind, shadcn
  -> Speech-2-Text als mobile, gehostete Arbeitsumgebung
```

Dieses Projekt ist ein Beispiel dafuer, wie praktische Prozessprobleme in eine
nutzbare KI-gestuetzte Anwendung uebersetzt werden koennen.

## Weitere Dokumente

- [Features](FEATURES.md)
- [Changelog](CHANGELOG.md)
