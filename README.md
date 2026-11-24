# GPR-Zitierstil für Zotero

CSL-Zitierstil für die Zeitschrift *GPR – Zeitschrift für das Privatrecht der Europäischen Union*.

*Der Zitierstil wurde unter Zuhilfenahme von KI erstellt.*

## Verschiedene Versionen

| Datei | Ausgabe für denselben Aufsatz (Stürner, GPR 2013, 305, zitiert S. 306) |
|---|---|
| `zeitschrift-gpr.csl` | `Stürner, GPR 2013, 305, 306.` |
| `zeitschrift-gpr-vollzitat.csl` | `Stürner, Gerichtsstands- und Erfüllungsortvereinbarungen im europäischen Zivilprozessrecht, GPR 2013, 305, 306.` |

Zulässig sind beide Formen; der Unterschied ist allein der Aufsatztitel, der Verfasser steht in beiden kursiv.

In beiden Stilen enthält jede Fußnote das vollständige Zitat – kein „a.a.O.“, „ders.“, „siehe Fn. 1“. Eine Literaturliste wird nicht erzeugt.

## Lizenz

Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) – siehe [LICENSE](LICENSE). Weitergabe und Bearbeitung sind erlaubt, solange die Namensnennung erhalten bleibt und Bearbeitungen unter derselben Lizenz stehen.

## Installation

In Zotero: *Einstellungen → Zitieren → Stile → „+“* und die `.csl`-Datei wählen. Alternativ die Datei in den Ordner `Zotero/styles` kopieren und Zotero neu starten.

## Feldbelegung

### Rechtsprechung (Typ „Gerichtsentscheidung“ / Case)

| Ausgabe | Zotero-Feld |
|---|---|
| `BGH` | Gericht |
| `29.3.1996` | Datum der Entscheidung (ohne führende Nullen, automatisch formatiert) |
| `II ZR 124/95` | Aktenzeichen |
| `ECLI:EU:C:2012:440` | Rechte (nur EU-Gerichte; alternativ Reihentitel) |
| `VALE Építési kft` | Titel (Parteiname, erscheint direkt vor der ersten Fundstelle) |
| `GmbHR` | Reporter (Kürzel) |
| `1996` bzw. `79` | Band/Jahrgang: Jahrgang oder Band der Fundstelle |
| `437` | Erste Seite |
| `438` / `Rz. 18` | Seite (Zitatstelle, im Zitatdialog als „Seite“ eintragen) |
| `Müller` | Autor (Verfasser einer Anmerkung → erscheint als `m. Anm. Müller`) |

Das Feld **Autor** ist bei Entscheidungen für den Verfasser einer Anmerkung reserviert; das Gericht gehört ausschließlich in „Gericht“.

Band/Jahrgang hat Vorrang. Ist das Feld leer, setzt der Stil automatisch das Entscheidungsjahr ein (`GmbHR 1996`); weicht das Veröffentlichungsjahr ab (`Beschluss 2015, MDR 2016, 10`), das Jahr deshalb in „Band/Jahrgang“ eintragen. Bei Juris-Fundstellen bleibt das Feld leer → `juris Rz. 18`.

Ohne Zeitschriftenfundstelle wird die amtliche Veröffentlichung zitiert; sie wird nicht angegeben. Reporter, Band und Seite bleiben dann leer, und das Zitat endet nach dem Aktenzeichen (`BGH v. 1.6.2022 – VIII ZR 278/20.`). URLs werden bei Entscheidungen bewusst nicht ausgegeben.

### Kommentare, Sammel- und Tagungsbände, Festschriften (Typ „Buchabschnitt“ / Book Section)

| Ausgabe | Zotero-Feld |
|---|---|
| `Wilhemi` | Autor (kursiv, nur Nachname) |
| `in Erman` | Buch-/Kommentartitel (`Erman`, `MünchKomm/BGB`, `Festschrift von Hoffmann`) |
| `Geimer/Schütze` | Herausgeber (nur bei Sammelbänden; entfällt bei Kommentaren) |
| `Das Prorogationsstatut …` | Titel des Beitrags (bei Kommentaren leer lassen, bei Festschriften/Aufsätzen in Sammelbänden eintragen) |
| `17` | Auflage (nur die Zahl, der Stil ergänzt „17. Aufl.“) |
| `2023` | Datum (Jahr) |
| `577` | Seitenzahl (Startseite des Beitrags, wird als „S. 577“ ausgegeben) |
| `§ 823 Rz. 24` | Seite (Zitatstelle: `§ 823 Rz. 24`, `Art. 23 EuGVVO Rz. 94`, `579 f.`) |

### Zeitschriftenaufsätze (Typ „Zeitschriftenartikel“)

`Kürzel` (Zeitschrift), `Band` (nur bei Archivzeitschriften wie AcP → `AcP 200 (2000)`), `Datum` (Jahr), `Seiten` (Startseite), Seite/Zitatstelle als Locator (`306`).

Ausgegeben wird nur das Kürzel, aus dem Feld **Zeitschriften-Abkürzung**. Der volle Zeitschriftentitel (Feld „Publikation“) erscheint nicht und darf fehlen; ist die Abkürzung leer, greift der Stil ersatzweise auf „Publikation“ zurück.

### Monografien (Typ „Buch“)

Autor, Titel, Auflage (Zahl), Datum (Jahr); die Fundstelle wird als Locator eingetragen und dort ausgeschrieben: `Rz. 147` oder `S. 144`.

### Online-Quellen (Typ „Webseite“, „Forumspost“, „Dokument“)

`Autor, Titel, Website, URL, zul. abger. 12.3.2026` – „zul. abger.“ mit dem Abrufdatum; ohne Abrufdatum die Angabe aus „Datum“ (`9.1.2025`). Bei „Dokument“ tritt an die Stelle der Website das Feld „Standort im Archiv“ (z. B. `KOM(2025) 1 endg.`).

### Normen (Typ „Gesetz“, „Verordnung“, „Vertrag“)

`Titel v. Datum, Amtsblatt Band, Seite` – z. B. `Richtlinie 93/13/EWG v. 5.4.1993, ABl. L 95, 29.` Der Zweig hält Normen im gleichen Muster wie die übrigen Quellen.

## Hinweise

- **Seitenbereiche sind erlaubt:** `213–216` in „Seiten“ ist unschädlich, ausgegeben wird nur die Startseite (`213`).
- **ECLI** steht im Feld *Rechte* (Zotero exportiert „Rechte“ als CSL-Variable `license`, die der Stil an dieser Stelle ausgibt). Ein bereits gefüllter *Reihentitel* funktioniert weiterhin, „Rechte“ hat Vorrang.
- **Zitatstelle ohne automatische Beschriftung:** CSL kann „S.“, „Rz.“, „§“ nicht aus dem Inhalt ableiten. Die Zitatstelle deshalb so eintragen, wie sie erscheinen soll: `438`, `S. 144`, `Rz. 147`, `§ 823 Rz. 24`.
- **Anmerkungen** (`m. Anm. Müller`) werden aus dem Feld „Autor“ der Entscheidung gebildet und ohne Komma angeschlossen.
- **Gericht bei Folgezitaten** wird automatisch wiederholt, da jeder Beleg vollständig ausgegeben wird.
- Der Stil formatiert den Autor/das Gericht nach den Vorgaben: Verfasser kursiv, Gericht aufrecht, Datum ohne führende Nullen, Halbgeviertstrich zwischen Datum und Aktenzeichen.
