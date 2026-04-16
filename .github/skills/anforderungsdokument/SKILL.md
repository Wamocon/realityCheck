---
name: anforderungsdokument
description: >-
  WAMOCON Entwicklungsprompts: Tiefenanalyse, Marketing/UX-Rework und
  Anforderungsdokument (9 Kapitel + Quellenverzeichnis als .docx).
  Workflow: IDEA.md ausfuellen, Skill aufrufen, Dokument pruefen, Freigabe.
---

# WAMOCON Entwicklungsprompts und Anforderungsdokument

## Uebersicht

Dieser Skill stellt drei Entwicklungsprompts und eine verbindliche Dokumentstruktur
fuer WAMOCON-Anforderungsdokumente bereit. Das Anforderungsdokument folgt einer
festen 9-Kapitel-Struktur mit Quellenverzeichnis und wird als .docx generiert.

**Workflow:** IDEA.md ausfuellen -> Prompt 3 aufrufen -> Dokument pruefen -> Freigabe -> Implementierung starten.

---

## Prompt 1: Tiefenanalyse und kritische Projektbewertung

Verwende diesen Prompt nach dem Onboarding einer neuen App-Idee, um eine vollumfaengliche
Analyse auf Basis des Anforderungsdokuments durchzufuehren.

```
Pruefe bitte das aktuelle Projekt und mache dich mit allen Daten und Inhalten vertraut.

Fuehre anschliessend eine vollumfaengliche Tiefenanalyse zum Thema der App aus dem
Anforderungsdokument durch. Erstelle dafuer:
- Eine vollumfaengliche Bedarfsanalyse des geplanten Themas
- Eine Nutzwertanalyse fuer die Funktionen
- Hinweise auf moegliche Luecken im Markt, die mit der App nicht abgedeckt sind

Fasse deine Ergebnisse in einem Analysedokument zusammen und gib eine Empfehlung ab,
welche Richtung die App nehmen soll, um die groestmoegliche Nutzerplattform und den
groessten Nutzen zu erzielen.

Erstelle am Ende Entscheidungsvorlagen zur Entscheidung der naechsten Schritte fuer die
Entwicklung und Ausrichtung der Applikation.

Pruefe intern deine Ergebnisse kritisch und mehrfach, sodass die Ergebnisse brauchbar sind.
```

---

## Prompt 2: Marketing und UX/UI Rework

Verwende diesen Prompt, wenn die App eine Ueberarbeitung aus Marketing- und UX-Perspektive
benoetigt.

```
Bitte fuehre eine vollstaendige Analyse und Optimierung des Projektes durch.

Ziel ist eine umfassende Ueberarbeitung der Applikation aus Marketing- und UX/UI-Perspektive:
- Analysiere die Applikation und passende Oberflaechen, Farben, Typografie und Designsystem
- Optimiere den Workflow nach typischen UX-Prinzipien (gefuehrt, unterstuetzt, intuitiv)
- Stelle sicher, dass die Web-App auf Mobilgeraeten genauso ansprechend aussieht wie auf Desktop
- Implementiere passende Hilfestellungen fuer den User

Ueberarbeite alle Seiten vollstaendig und fuehre anschliessend alle notwendigen
Fehlerbehebungen durch.
```

---

## Prompt 3: Anforderungsdokument erstellen (9 Kapitel + Quellenverzeichnis)

Verwende diesen Prompt, um ein vollstaendiges Anforderungsdokument fuer eine App-Idee
zu erstellen. Ersetze [APP-IDEE] mit der Beschreibung aus IDEA.md. Die KI erstellt
das Skript scripts/generate-anforderungsdokument.mjs und fuehrt es aus.

```
Rolle: Du agierst als interdisziplinaeres Expertenteam: Senior Product Manager,
Market Research Analyst und Tech Lead.
Denkweise: analytisch, datengestuetzt, kritisch, loesungsorientiert.

Kontext: Wir entwickeln ein neues Webtool.
Tech-Stack: Next.js, Tailwind CSS, TypeScript, Supabase, Vercel.

[APP-IDEE aus IDEA.md einfuegen]

Aufgabe: Erstelle ein vollstaendiges WAMOCON-Anforderungsdokument nach der
verbindlichen 9-Kapitel-Struktur (siehe DOKUMENTSTRUKTUR unten). Jedes Kapitel
muss mit echten, belegten Daten und Quellen gefuellt werden. Keine Platzhalter.
Alle Quellen muessen real, oeffentlich und aktuell (nicht aelter als 1-2 Jahre) sein.

Das Dokument wird als .docx generiert:
Skript: scripts/generate-anforderungsdokument.mjs
Ausgabe: public/Anforderungsdokument_[ProjektName].docx

Regeln:
- Jede Zahl braucht eine Quellenangabe
- Anforderungstabellen mit ID-Praefix (z.B. K-, B-, R-)
- Wettbewerber mit echten Staerken UND Schwaechen
- Ehrliche Risikoanalyse, keine Schoenrede
- Tone: professionell, direkt, beratend, auf Deutsch
- Kosten realistisch: GitHub Copilot 35 EUR/Monat, Supabase 10 EUR/Monat,
  Domain 2-4 EUR/Monat, ggf. API-Kosten
- V1 muss in 5-7 Werktagen realisierbar sein
```

---

## DOKUMENTSTRUKTUR (verbindlich fuer jedes Anforderungsdokument)

### Deckblatt

Oben: dicke Trennlinie (WAMOCON-Blau).
Titel zentriert: "WAMOCON GMBH" + "Anforderungsdokument" + [Projektname].
Metadaten-Tabelle ohne Rahmen:

| Feld              | Wert                          |
|-------------------|-------------------------------|
| Welle             | [Wellennummer aus IDEA.md]    |
| Projekt           | [App-Name]                    |
| Unternehmen       | WAMOCON GmbH                  |
| App Version       | 1                             |
| Erstellt von      | [Name aus IDEA.md]            |
| Eingereicht an    | [Empfaenger aus IDEA.md]      |
| Datum             | [TT.MM.JJJJ aktuell]         |
| Vertraulichkeit   | Intern vertraulich            |
| Status            | Zur Freigabe eingereicht      |

Unten: gestrichelte Trennlinie.

---

### Kapitel 1: Zusammenfassung

- **1.1 Die Idee** -- Was macht die App? Welches Problem loest sie? Kernnutzen in 3-5 Saetzen.
- **1.2 Warum jetzt?** -- Markttiming: Warum ist das Thema genau jetzt relevant? Mit aktuellen Zahlen belegen.

---

### Kapitel 2: Marktanalyse

- **2.1 Zielgruppe in Zahlen** -- Marktgroesse, Nutzeranzahl, Wachstumsprognosen. Fokus Deutschland/DACH. Jede Zahl mit Quellenangabe.
- **2.2 Infrastruktur/Marktwachstum** -- Was waechst? Welche Trends treiben den Markt? Prognosen bis 2030.
- **2.3 Das Kernproblem** -- Faktisch belegt: Was ist das konkrete Problem, das die App loest? Warum existiert es heute noch?
- **2.4 Regulatorisches Umfeld** -- DSGVO, branchenspezifische Gesetze, EU-Verordnungen. Was staerkt den USP?

---

### Kapitel 3: Wettbewerb

- **3.1 Direkte Wettbewerber** -- Tabelle: Anbieter | Staerken | Schwaechen/Chance fuer uns | Preis.
  Echte Anbieter mit echten Daten. Staerken UND Schwaechen ehrlich benennen.
- **3.2 Indirekte Wettbewerber / Aggregate** -- Tabelle: Anbieter | Was er bietet | Was fehlt (Chance fuer uns).
- **Marktluecke** -- Zusammenfassung: Welche Kombination bietet kein Wettbewerber? Das ist unser Einstieg.

---

### Kapitel 4: Zielgruppe

- **4.1 Primaere Zielgruppe** -- Genaue Beschreibung mit Zahlen. Nutzerprofile als Fliesstext (Personas mit Name, Rolle, Verhalten).
- **4.2 Sekundaere Zielgruppe** -- Wer kommt spaeter dazu? Warum erst spaeter?
- **4.3 Nicht-Zielgruppe** -- Wen adressiert die App NICHT? Klar abgrenzen.

---

### Kapitel 5: Nutzen

- **5.1 Nutzen fuer Kunden** -- Tabelle: Problem heute | Loesung durch App | Konkreter Vorteil. Mit messbaren Zahlen.
- **5.2 Nutzen fuer WAMOCON GmbH** -- Warum lohnt sich das Projekt? Einnahmequellen, Skalierungspotenzial, strategischer Wert.

---

### Kapitel 6: Abhaengigkeiten und Machbarkeit

- **6.1 Externe Abhaengigkeiten** -- APIs, Dienste, Datenquellen. Tabelle: Quelle | Was sie liefert | Kosten | Abhaengigkeit.
- **6.2 Abrechnungs-/Integrationsoptionen** -- Falls relevant: Welche Optionen fuer Bezahlung/Integration gibt es? Pro Version.
- **6.3 Gesamtbewertung** -- Hat V1 kritische Abhaengigkeiten? Kann ein Wettbewerber den Start blockieren?

---

### Kapitel 7: Anforderungen Version 1

- **7.1 Hauptprozesse** -- Gruppiert nach Themen (z.B. "Dokumenten-Upload", "Frage-Generator").
  Jede Gruppe hat eine eigene Anforderungstabelle:

  | ID   | Anforderung                          | Prioritaet | Status |
  |------|--------------------------------------|------------|--------|
  | K-01 | [Kernfunktion]                       | Muss       | Neu    |

- **7.2 Basisfunktionalitaeten** -- Pflicht fuer jede App:

  | ID   | Anforderung                                              | Prioritaet | Status |
  |------|----------------------------------------------------------|------------|--------|
  | B-01 | Rollen- und Rechteprinzip                                | Muss       | Neu    |
  | B-02 | Anmeldung und Registrierung (E-Mail mit Bestaetigung)    | Muss       | Neu    |
  | B-03 | Passwort zuruecksetzen                                   | Muss       | Neu    |
  | B-04 | Admin-Bereich fuer Nutzerverwaltung                      | Muss       | Neu    |
  | B-05 | Profilseite                                              | Muss       | Neu    |
  | B-06 | Dashboard als Startseite                                 | Muss       | Neu    |
  | B-07 | Navigation mit Breadcrumbs                               | Muss       | Neu    |
  | B-08 | Benachrichtigungssystem (In-App und/oder E-Mail)         | Soll       | Neu    |
  | B-09 | Spracheinstellungen (Deutsch und Englisch)               | Muss       | Neu    |
  | B-10 | Dunkel/Hell-Modus                                        | Muss       | Neu    |
  | B-11 | FAQ und Hilfebereich                                     | Soll       | Neu    |
  | B-12 | AGB, Impressum, Datenschutzerklaerung                    | Muss       | Neu    |
  | B-13 | Cookie-Banner nach DSGVO                                 | Muss       | Neu    |
  | B-14 | DSGVO-Funktionen (Daten exportieren, Konto loeschen)     | Muss       | Neu    |
  | B-15 | Geschaeftsmodell (Free und Premium)                      | Muss       | Neu    |
  | B-16 | Upgrade von Free auf Premium in der App                  | Muss       | Neu    |

- **7.3 Scope** -- Tabelle: In Scope V1 | Out of Scope (V2+). Klare Abgrenzung.

---

### Kapitel 8: Chancen und Risiken

- **8.1 Chancen** -- Tabelle: Chance | Begruendung. Mit Zahlen und Quellen.
- **8.2 Risiken** -- Tabelle: Risiko | Warum es eintreten kann | Gegenmassnahme.

---

### Kapitel 9: Umsetzungsplan Version 1

- **9.1 Entwicklungsansatz** -- Tech-Stack, Werkzeuge (GitHub Copilot), Teamstruktur.
- **9.2 Umsetzungsplan** -- Tag-fuer-Tag-Tabelle ueber 5-7 Werktage:

  | Tag       | Fokus                       | Inhalt                          |
  |-----------|-----------------------------|---------------------------------|
  | Tag 1-3   | Hauptprozesse               | [Details]                       |
  | Tag 3-4   | Testing und Bugfixing       | [Details]                       |
  | Tag 4-5   | Basisfunktionalitaeten      | [Details]                       |
  | Tag 5-6   | Puffer                      | [Details]                       |

- **Hinweis** -- Realistisch: V1 ist ein lauffaehiger Prototyp, kein Endprodukt.

---

### Quellenverzeichnis

Tabelle: Quelle | Inhalt/URL. Nur reale, oeffentlich verfuegbare Quellen.
Jede Zahl im Dokument muss mindestens eine Quelle haben.

---

## FORMATREGELN

- **Sprache:** Deutsch. Echte Umlaute wo moeglich (ae/oe/ue in Code ist OK).
- **Schrift:** Arial Narrow, 11pt Fliesstext.
- **Tabellenkopf:** WAMOCON-Blau (1E3A5F) mit weissem Text, fett.
- **Tabellenzeilen:** alternierend weiss / hellgrau (F5F5F5).
- **Breiten:** WidthType.DXA (keine Prozent).
- **Shading:** ShadingType.CLEAR (kein SOLID).
- **Kein \n in TextRun** -- separate Paragraphen verwenden.
- **Seitenkopf:** "WAMOCON GmbH, Mergenthalerallee 79-81, 65760 Eschborn" (8pt, grau).
- **Seitenumbruch** zwischen den Hauptkapiteln.

---

## Workflow

```
[1] IDEA.md im Projekt-Root ausfuellen
        |
        v
[2] Prompt 3 aufrufen -> Anforderungsdokument als .docx generieren
        |
        v
[3] Dokument pruefen und zur Freigabe einreichen (Geschaeftsfuehrung)
        |
        v
[4] Nach Freigabe: Prompt 1 fuer Tiefenanalyse aufrufen
        |
        v
[5] Implementierung mit @planner -> @developer
        |
        v
[6] Nach Launch: Prompt 2 fuer UX/UI Rework
```

---

## Voraussetzungen

- Node.js >= 18
- npm install docx (einmalig)
- Ausgabe: public/Anforderungsdokument_[ProjektName].docx
- package.json: "gen:anforderungsdokument": "node scripts/generate-anforderungsdokument.mjs"