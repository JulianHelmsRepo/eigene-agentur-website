Website-Content – Nexora (Arbeitsplatzhalter, Name wird noch final festgelegt)

Seitentyp: One-Pager (Single-Page-Scroller), spätere Unterseiten pro Leistung optional
Ansprache: Sie-Form, Unternehmen ("Wir"), keine Personenmarke
Zielgruppe: Branchenoffen, kein Nischen-Branding auf der Website
Design-Inspiration: Sehr gute Seite ist https://dhigital-lab.de, solche oder ähnliche Animationen nutzen, gerade die Karten-Animationen sind sehr stark. Button- und Kachel-Hover-Effekte ähnlich flow8.de/prozess; Kontakt-Layout (Formular + Direkt-Kontakt-Card) wie drautomation.de
Negativ-Referenz: flowwise-digital.com (zu generisch/basic), drautomation.de Sprache (zu buzzwordig, "maßgeschneidert" o.ä. vermeiden)
Bildmaterial: Für den Mockup können vorerst Fake-/Platzhalterbilder verwendet werden, Screenshots liefere ich wenn vorhanden. Screenshots sind im Drive Ordner.
Ziel: moderne Premium-Website für meine Digitalagentur für Websites & Sichtbarkeit (Automatisierung als optionale Erweiterung).

Design-Constraints (verbindlich, aus eigenen Design-Regeln):
Kein Lila/Violett/Indigo als Hauptfarbe, keine Lila→Blau/Pink-Verläufe, keine verlaufsgefüllten Wörter in Überschriften
Keine erfundenen Zahlenblöcke ("25% · 95%") – Zahlen nur, wenn echt und belegt
Keine Emojis in Überschriften, keine Badge-Reihen unter dem Hero
Nicht alles zentriert in einer Spalte von oben bis unten
Inter/Roboto/System-Font nicht als komplettes Typo-System ohne Display-Font
Keine externen Fonts/Scripts/Bilder von Drittserver-URLs (DSGVO)
Keine generischen "Zweite-Ordnung"-KI-Looks: Fast-Schwarz+Neonakzent, Zeitungslook mit Radius 0
Qualitätsboden: semantisches HTML, sichtbare Fokuszustände, Alt-Texte, beschriftete Formularfelder, prefers-reduced-motion respektieren
Kernprinzip: Eigenständigkeit muss aus dem Thema kommen (Sprache, Zielgruppe), kein austauschbares Gerüst in anderen Farben


Farbschema (final, bestätigt aus Hero-Video-Produktion)
Helles Theme, off-white + warmer Amber-Akzent. Entstanden aus dem AI-generierten Hero-Video (Laptop öffnet sich, Kamera zoomt in den Screen, Übergang in die echte Website).
Hintergrund (Basis): #FFFFFF -- exakt per Farbpipette aus dem letzten Video-Frame bestätigt, muss 1:1 als background-color der Seite übernommen werden für nahtlosen Übergang
Oberfläche/Karten: #F8F5F2
Text primär: #1E1D1B (Anthrazit statt Schwarz)
Text sekundär: #6B6862
Akzent (Haupt): #F58B2E -- Buttons, Links, Highlights; nicht als große Fläche verwenden
Akzent Hover: #D9781F
Akzent hell (Badges/Fills): #F6E4CC
Rahmen/Linien: #E4DFD5
Typografie (final)
Display/Headline: Clash Display -- für Hero-Headline UND alle Zwischenüberschriften der Sektionen sowie die großen Nummern (01, 02, 03); gleiche Foundry-Familie wie General Sans (Fontshare, kostenlos, self-hosted), einheitlicher roter Faden beim Scrollen durch die Seite
Basis-Schrift (Navigation, Fließtext/Beschreibungen, Buttons, Labels, FAQ, Footer): General Sans, Regular/Medium -- deckt alles außer den Überschriften ab
Bei kleineren Zwischenüberschriften/Labels erst beim echten Bauen prüfen, ob Clash Display in kleinerer Schriftgröße noch gut aussieht -- Display-Fonts sind oft auf große Schriftgrade optimiert; im Zweifel dort auf General Sans Bold ausweichen
Beide Fonts self-hosted einbinden (keine externen Font-CDN-URLs, siehe DSGVO-Constraint oben)


1. Hero
Kicker (klein, über der Headline): DIGITALAGENTUR FÜR WEBSITES & SICHTBARKEIT
Headline: Gefunden werden. Verstanden werden. Beauftragt werden.
(Hinweis: nur das Wort "Beauftragt" in Akzentfarbe #F58B2E, Rest bleibt Anthrazit #1E1D1B — kein Gradient/Verlauf, einfarbige Hervorhebung, siehe Design-Constraint zu verlaufsgefüllten Wörtern)
Subline: Conversion-starke Websites und Sichtbarkeit in Google & KI-Suchen – für Dienstleister und Online-Shops.
CTA: Kostenloses Erstgespräch

Animation/Interaktion (final):
Hero-Video (final) -- siehe Datei "Hero Video" im Drive-Ordner
Einmaliges AI-generiertes Video (kein Loop): Laptop öffnet sich, Kamera zoomt langsam rein
Sobald der Laptop vollständig geöffnet ist (während das Video noch läuft): Hero-Content (Kicker, Headline, Subline, CTA) blendet als HTML-Overlay ein – bereits in seiner finalen Zielgröße/-position (wie später auf der echten Website), dadurch anfangs größer/breiter als der noch kleine Laptop-Bildschirm, ragt bewusst über den Bildschirmrand und an den Seiten hinaus (Referenz: "Hero Inspo.PNG" im selben Drive-Ordner)
WICHTIG: Der Text-Overlay bleibt ab diesem Moment die ganze Zeit unverändert in Größe und Position stehen – KEIN eigenes Zoomen/Skalieren des Textes. Nur das Video-Bild darunter zoomt weiter rein, wodurch der (feststehende) Laptop-Bildschirm optisch immer größer wird und sich zunehmend an die Textgröße annähert
Am Ende des Video-Zooms deckt sich der jetzt volle Screen exakt mit der Text-Position/-Größe – Video endet, Übergang zur echten HTML-Website, Text hat sich die ganze Zeit über nicht bewegt oder verändert
Rest-Rand vom Laptop-Bezel im letzten Video-Frame ggf. per CSS-Crop mitkaschieren, falls beim Testen noch Rand sichtbar bleibt
Da der Text-Overlay während des Videos über dem (noch teils dunklen/schwarzen) Laptop-Rand liegt: dezenter heller text-shadow/Glow hinter dem Hero-Text als Kontrast-Absicherung, unabhängig von der Bezel-Farbe
Video-Element: autoplay, muted, playsinline, KEIN loop-Attribut
prefers-reduced-motion: statisches letztes Frame direkt mit final positioniertem Hero-Content zeigen, kein Video/keine Zoom-Animation abspielen
Generell: professionelle Hover-Effekte auf Buttons und Kacheln (Inspiration: flow8.de/prozess), bewusst dosiert statt überladen – Ziel ist "zeigt Können", nicht "zu viel Bewegung"


2. Angebot
Zwischenüberschrift:
Eine Website, die für Sie arbeitet – nicht nur schön aussieht
Intro:
Die meisten Kunden entscheiden schon vor dem Anruf, wen sie beauftragen, und zwar anhand der Website. Ist sie veraltet oder taucht bei Google nicht auf, sind Sie raus. Kommt die Anfrage doch an, darf sie nicht im Postfach untergehen.

01 – Website Klar aufgebaut, schnell, auf jedem Gerät nutzbar – mit den Inhalten, die Ihre Kunden wirklich überzeugen. Auch als Online-Shop möglich.

02 – Sichtbarkeit Lokale Suche und KI-gestützte Suchassistenten wie ChatGPT oder Google AI Overviews finden Sie nur, wenn Ihre Seite dafür aufgebaut ist. Wir sorgen dafür, dass Sie dort auftauchen, wo gesucht wird.

03 – Automatisierung (optional) Anfragen automatisch erfassen, Termine vorschlagen, ins CRM übertragen – bis hin zu individuellen Lösungen wie einem KI-Telefonbot, je nach Bedarf.


3. Referenzen
Zwischenüberschrift:
Was wir für andere gebaut haben.
Layout: Drei Karten/Kacheln, welche mit einer Scroll-Animation nacheinander angezeigt werden, es wird immer nur eine gleichzeitig angezeigt. Mobile horizontal swipe (bestätigt als bevorzugtes Muster, auch für später bei 5+ Referenzen). Pro Kachel: angeschnittener Website-Screenshot oben (kein vollständiger Screenshot – wirkt wie Portfolio-Bild statt Beweisfoto), dann zwei-drei kurze Stichworte zur Beschreibung was für ein Produkt erstellt wurde (diese speziell hervorheben, z.B. mit Rahmen, siehe dhigital-lab.de), Testimonial darunter, Name/Unternehmen klar zugeordnet unter dem Zitat.
Kanzlei Paetsch · (Website) (CMS) [(Google Auftritt) erst wenn Google-Profil live] (SEO/GEO). Screenshot: https://drive.google.com/file/d/1mW75hvQbU6YSF2Hhxy1JNYlb9dBScnXh/view
„Bevor wir zu (Firmenname) kamen, hatten wir keinen Online-Auftritt. Sie haben uns gut beraten und genau das umgesetzt, was uns wichtig war: Vertrauen aufbauen, seriös wirken, aber trotzdem modern. Dabei wurde nachgefragt und mitgedacht, bis die Lösung wirklich passte. Das Ergebnis: eine Website, mit der wir uns jetzt präsentieren können.“ — Frederik Voltman, Kanzlei Paetsch [Website ansehen →]
Vita Passo · (Landing Page) (Google Auftritt) (Bewertungsmanagement). Screenshot: https://drive.google.com/file/d/1m0QevICVNwVneo1COge3UEMgBqMJWWzn/view
„Für uns als Praxis für Physio- und Ergotherapie mit zwei Standorten hat online eine klare und zugängliche Struktur gefehlt. Hier hat (Firmenname) für uns Landingpage, Google-Auftritt und Bewertungsmanagement sauber aufgesetzt und jeder Standort hat nun seinen eigenes Profil. Die Zusammenarbeit war professionell, stets verlässlich und Anliegen wurden zeitnah geklärt. (Firmenname) hat uns dabei unterstützt, genau dort sichtbar zu sein, wo unsere (zukünftigen) Patient:innen/Patientinnen und Patienten uns suchen.“ — Nico Scholz, Vita Passo
Kara Verpackung · (Online Shop) (Produktkatalog). Screenshot: https://drive.google.com/file/d/1qZ25IRZv4_H49x5PT3OTYG0S87dbSyBb/view
„Der Wunsch nach einem eigenen Onlineshop bestand schon länger. Jetzt steht ein vollständiger B2B-Shop mit unserem gesamten Katalog, sauber nach Kategorien geordnet und mit allen rechtlichen Vorgaben abgedeckt. Die Umsetzung war strukturiert, auch bei mehreren hundert Produkten wurde alles im Blick behalten.“ — Serkan Kara, Kara Verpackung
Struktur bleibt erweiterbar – weitere Referenzen können ohne Anpassung der Überschrift ergänzt werden.

4. Ablauf
Zwischenüberschrift:
Vier Schritte bis zur fertigen Lösung.
01 – Erstgespräch Ein kurzes, unverbindliches Gespräch. Sie schildern, was Sie brauchen und wo es aktuell hakt – wir hören zu und stellen die richtigen Fragen.
02 – Konzept & Demo Auf Basis Ihrer Angaben entsteht ein erster Entwurf. Keine Skizze auf Papier, sondern eine Vorschau, die Sie sich direkt ansehen können.
03 – Anpassung Gemeinsam gehen wir durch, was passt und was noch nicht. Änderungen fließen direkt ein, bis alles zu Ihnen und Ihrem Auftritt passt.
04 – Umsetzung & Go-Live Technik, Design und Anbindung an Ihre Systeme übernehmen wir. Danach bleiben wir erreichbar, falls etwas angepasst werden soll.


5. Baukasten, Agentur oder Nexora?


Baukasten (z. B. Wix)
Große Agentur
Nexora
Umsetzung
Selbst zusammenbauen
Meist Wochen bis Monate
Direkt mit einem Ansprechpartner
Ansprechpartner
Keiner
Wechselnd, oft Projektmanager
Immer derselbe
Nach Go-Live
Auf sich allein gestellt
Oft neues Projekt, neue Warteschlange
Weiterhin erreichbar
Sichtbarkeit (SEO & KI-Suche)
Nicht vorgesehen
Oft Extra-Dienstleister
Aus einer Hand


Kurzblock (Erfahrung):
Die Erfahrung dahinter kommt aus der IT- und Prozessberatung – dort, wo Systeme und Abläufe jeden Tag den Unterschied machen. Diese Herangehensweise übertragen wir auf Websites und Sichtbarkeit für Unternehmen: strukturiert, direkt, ohne Umwege über große Teams oder lange Abstimmungswege.


6. FAQ
Zwischenüberschrift:
Häufige Fragen.
Wie läuft der Einstieg ab? Nach einem ersten Gespräch bekommen Sie ein konkretes Angebot mit Umfang und Preis. Bei größeren Projekten oder offenen Punkten auf Ihrer Seite klären wir Details in einem kurzen Folgetermin.
Wer liefert die Inhalte für die Website? Texte, Bilder und Angaben zu Ihrem Unternehmen kommen von Ihnen. Aufbau, Design, technische Umsetzung sowie Hosting übernehmen wir – Sie müssen sich um nichts Technisches kümmern.
Wie lange dauert die Umsetzung? Kommt auf den Umfang an. Nach dem Erstgespräch nennen wir Ihnen einen realistischen Zeitrahmen.
Ich habe schon eine Website, die veraltet ist. Geht das auch? Ja. Wir übernehmen bestehende Inhalte und bauen darauf eine neue, moderne Seite.
Was passiert, nachdem die Website online ist? Sie sind nicht allein damit. Kleinere Anpassungen und Rückfragen sind auch nach dem Launch möglich.


7. Finale CTA / Kontakt
Headline:
Kontaktieren Sie uns ganz einfach.
Subline:
Ein paar Zeilen genügen. Wir melden uns in der Regel innerhalb von 24 Stunden mit einer ehrlichen ersten Einschätzung – unverbindlich.
Formular (linke Spalte):
Name
E-Mail
Telefon (optional)
Nachricht – Platzhaltertext: „Wo klemmt es bei Ihnen? Was möchten Sie erreichen?“
Checkbox Datenschutz
Button: „Nachricht senden“
Direkt erreichen – Card (rechte Spalte):
E-Mail: julianhelms.digital@gmail.com (vorläufig – auf finale Firmen-Domain umziehen, sobald verfügbar)
WhatsApp: +49 152 24310832 – „Für schnelle Fragen zwischendurch“
Antwortzeit: „innerhalb von 24 Stunden, werktags meist schneller“
Technik: Kontaktformular via Astro + Resend (E-Mail-Versand, kostenloser Free-Tier), WhatsApp-Link (wa.me), kein Kalender-Tool im Start-Setup.


8. Footer
Spalte 1 – Unternehmen Nexora. Websites und Sichtbarkeit für Unternehmen – Automatisierung auf Wunsch.
Spalte 2 – Leistungen Website · Sichtbarkeit · Automatisierung (optional)
Spalte 3 – Kontakt julianhelms.digital@gmail.com · +49 152 24310832 · Hamburg
Unterzeile: © 2026 Nexora · Alle Rechte vorbehalten · [Impressum] · [Datenschutz]


Offene To-Dos (unabhängig vom Design)
[x] Bilder/Screenshots der 3 Referenzprojekte besorgt (liegen im Drive-Ordner "Eigene Website")
[x] Testimonials eingeholt (Freddi/Kanzlei Paetsch, Vita Passo, Kara Verpackung)
[ ] Firmenname final festlegen (Nexora ist Arbeitsplatzhalter)
[ ] E-Mail-Adresse ggf. auf finale Firmen-Domain umziehen
[X] Impressum & Datenschutz-Text erstellen (rechtlich nötig vor Live-Schaltung) Impressum und datenschutz sind im lokalen ordner oder im drive ordnern
