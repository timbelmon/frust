# frust

> „Streite niemals mit dummen Leuten. Sie werden dich auf ihr Level runterziehen und dich dort mit Erfahrung schlagen." – Mark Twain

Wer jeden Tag im echten Leben bis zum Hals in der täglichen Dosis Schwurbelei, faktenbefreiter Stammtisch-Agitation und verstrahltem Alltagsirrsinn steht, braucht ein Ventil. **frust** ist genau das: ein digitales Archiv, das politischen Realitätsabgleich mit harter Frustration verbindet – polemisch im Ton, aber faktenbasiert in der Substanz.

## Worum geht es?

Der Inhalt lebt im Obsidian-kompatiblen Ordner `content/` und deckt im Kern diese Kategorien ab:

- **AFD** – Personen (Höcke, Lüth, Weidel, Kalbitz u. a.), Perspektive & Praxis, Rechtsradikal, Schwurbeleien, Volksverräter und Politik für Reiche
- **Fake News** – Medien- und Desinformationskritik
- **Politik erklärt für Dummies** – Sachliche Erklärstücke
- **VW** – Parteien aus Sicht eines VW-Arbeiters

Das Projekt ist bewusst **Open Source**: Ich bin sicher nicht der Einzige, dem bei dem Wahnsinn das Kotzen kommt. Wer Zeug hat, das raus muss, oder den Bullshit hier mit harten Fakten, Richtigstellungen oder Extra-Quellen füttern will, ist eingeladen.

## Technik

Die Website wird mit **Quartz v5** erzeugt, einem Open-Source-Tool zum Veröffentlichen von Obsidian-Notizen bzw. eines „digital garden" als statische Website.

- Quartz-Dokumentation: https://quartz.jzhao.xyz/
- Quelle der Inhalte: [`content/`](content/)

## Quellenstandards

Das Regelwerk ist bewusst streng, denn der Ton darf polemisch sein – die Fakten müssen stimmen. Grundprinzip: **Fakten vor Meinung.**

**Grundregeln:**
- Jede Kernaussage muss auf eine Primär- oder qualifizierte Sekundärquelle zurückgehen. Was sich nicht belegen lässt, wird markiert oder weggelassen – nie erfunden.
- Bevorzugt werden **deutsche und englische** Quellen (offizielle Behörden, Gerichte, Bundestag, Verfassungsschutz sowie etablierter Qualitätsjournalismus). Nicht-deutsche/englische Quellen nur als absolute Ausnahme und nie als einzige Belegstelle.
- **Primärquellen zuerst:** Bundestag-Drucksachen, Plenarprotokolle, Gerichtsurteile und Behördenberichte schlagen jede Zeitung.

**Quellen-Kategorien:**
- **„Gut" (bevorzugt):** öffentlich-rechtliche und etablierte Medien (Tagesschau, ZDF, Deutschlandfunk, Spiegel, ZEIT, SZ, FAZ, taz, Handelsblatt, Tagesspiegel, DW, BBC, Reuters, AP, The Guardian, Politico) sowie offizielle/institutionelle Quellen (Bundestag, Gerichte, Verfassungsschutz, bpb, Correctiv).
- **„Skepsis" (nur ergänzend, nie als Kernquelle):** Quellen mit Bias-Risiko wie Welt, Focus, Berliner Zeitung, Bild, Merkur oder Euractiv. Im Zweifel werden sie durch eine „gute" Quelle ersetzt.
- **„Ausgeschlossen" (niemals):** Propaganda und tendenziöse Quellen, z. B. RT/Sputnik/TASS/Ria (russische Staatspropaganda), topwar.ru, euromaidanpress, extremistische Medien (Kompakt, NIUS, Aktuell24), Wikipedia als Zitat, Blog-/Substack-Inhalte ohne Redaktion, sowie Platzhalter-URLs und ablaufende `/live-news/`-Links.

**Quellenprüfung (vor jeder Nutzung einer neuen Quelle):**
1. Art der Quelle (Behörde/Gericht = sofort ok, Journalismus = weiter prüfen, Blog/soziales Medium = kritisch) – 2. Sprache (deutsch/englisch?) – 3. Herausgeber (wer steckt dahinter? unabhängige Redaktion oder Partei/NGO/Staat/Ideologie?) – 4. Bias-Check (framed die Quelle? wählt sie Fakten einseitig aus?) – 5. Doppel-Check (belegt ein Zweitsource aus der „gut"-Liste dieselbe Kernaussage?) – 6. Link-Status (HTTP 200? kein Platzhalter, keine `/live-news/`-URL?) – 7. Bei Unsicherheit: Quelle markieren, nachfragen oder weglassen.

## KI-Einsatz und Transparenz

Für die Erstellung und Pflege der Artikel wird **vor Ort laufende lokale KI** eingesetzt. Das hat Vorteile für ein Projekt wie dieses, ist aber mit klaren Regeln verbunden. Die KI übernimmt keine redaktionelle Verantwortung – sie ist ein Werkzeug zur Recherche und Qualitätssicherung.

**Automatisierte Web-Durchforstung (Crawling):**
- **Quellen- und Link-Validierung:** Die KI prüft jede Quellen-URL automatisiert auf Erreichbarkeit (HTTP-Status), erkennt Platzhalter-URLs (`a-0000…`), ablaufende `/live-news/`-Links und tote/404-Seiten und entfernt bzw. ersetzt sie.
- **Domain-Einordnung:** Neue Domains werden automatisch anhand des Quellenverzeichnisses einsortiert (gut / Skepsis / ausgeschlossen) – inklusive Sprachprüfung und Herausgeber-Bewertung. Etablierte Behörden/Gerichte passieren sofort, Unbekanntes landet zur manuellen Prüfung.
- **Automatische Fake-News-Erkennung:** Beim Durchforsten wird verdächtiger Inhalt gecheckt – etwa Plattitüden ohne Beleg, reißerische Sprache ohne Faktenbasis, ungeprüfte „Enthüllungen" aus Propaganda-Kanälen, sowie Indizien für Framing (einseitige Faktenauswahl, parteiische Diktion, Strohmann-Argumentation). Als Referenz dient der bekannte Muster-Nachweis (RT/Sputnik-Kopien in „Skepsis"-Medien u. ä.).
- **Multi-Source-Kreuzvalidierung:** Kernaussagen werden automatisch gegen mehrere unabhängige Quellen aus der „gut"-Liste gegeneinander abgeglichen. Nur was von mindestens einer qualifizierten Quelle unabhängig gedeckt ist, gilt als belastbar.

**Regeln dafür:**
1. **Lokal statt Cloud:** Es läuft die auf meinem Rechner installierte KI – es werden keine Inhalte an externe Dienste hochgeladen.
2. **Keine erfundenen Quellen:** Die KI darf keine URLs, Drucksachen-Nummern, Zitate oder Belege erfinden. Jede Kernaussage muss nachprüfbar sein.
3. **Mensch finalisiert:** KI durchforstet, validiert und schlägt vor. Die Freigabe und Verantwortung für veröffentlichte Artikel liegt beim Menschen.
4. **Quellenstandard gilt auch für KI:** Die KI ist an genau dieselben Quellenregeln gebunden wie ein menschlicher Autor – inklusive Verbot von Platzhalter-URLs und tendenziösen Quellen.
5. **Unsicherheit wird gemeldet:** Was die KI nicht verifizieren kann oder wo eine Quelle unsicher ist, wird markiert oder weggelassen – nie stillschweigend eingebaut.

Der Mehrwert ist Qualitätssicherung, nicht Autorität: Die KI soll Fehler finden, tote oder unseriöse Quellen aussortieren und belegbare Artikel liefern – nicht Meinung ersetzen.

## Lizenz

MIT – siehe [`LICENSE.txt`](LICENSE.txt).
