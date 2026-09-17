# PROJEKT.md — Nexora (eigene Agentur, Arbeitsname)

> Hier steht nur Projektspezifisches. Allgemeine Vorgaben stehen global in `CLAUDE.md`
> und `~/.claude/rules/` und müssen hier nicht wiederholt werden.

Angelegt: 2026-09-16 · Zuletzt aktualisiert: 2026-09-17

---

## 1. Brief

- **Kunde:** Eigene Agentur (kein Kundenprojekt), Arbeitsname "Nexora" — Firmenname noch nicht final
- **Was macht sie konkret:** Digitalagentur für Websites & Sichtbarkeit (Automatisierung als optionale Erweiterung)
- **Zielgruppe:** Branchenoffen — Kaltakquise-Leads (SHK, Kanzleien, Physiopraxen) und persönliche Kontakte/Empfehlungen
- **Der eine Job der Seite:** Anfrage/Erstgespräch auslösen
- **Erfolg heißt für sie:** Eingehende Anfragen über Formular/WhatsApp
- **Tonalität:** Sie-Form, Unternehmen ("wir"), keine Personenmarke, nicht buzzwordig (kein "maßgeschneidert")
- **Was sie unterscheidet:** Direkter, durchgehender Ansprechpartner statt Wechsel/Warteschlange, Website + Sichtbarkeit aus einer Hand
- **Was sie auf keinen Fall will:** Buzzwordige Sprache ("maßgeschneidert" o. ä.), generischer Baukasten-Look

## 2. Referenzen

- **Positiv:**
  - dhigital-lab.de — Karten-Animationen (Referenz für Referenzen-Sektion, Kachel-Highlight-Rahmen)
  - flow8.de/prozess — Button- und Kachel-Hover-Effekte
  - drautomation.de — Kontakt-Layout (Formular + Direkt-Kontakt-Card)
- **Negativ:**
  - flowwise-digital.com — zu generisch/basic
  - drautomation.de (Sprache) — zu buzzwordig, "maßgeschneidert" o. ä. vermeiden
- Corporate Design vorhanden? Nein — Design-Token wurden aus der Hero-Video-Produktion abgeleitet (siehe Punkt 3)
- Kollision mit einem Hard Ban? Keine

## 3. Design-Token *(final)*

| Rolle | Hex | Einsatz |
|---|---|---|
| Basis (`--color-background`) | `#FFFFFF` (war `#F1EDEB`, siehe Entscheidung 2026-09-16) | Seitenhintergrund im Hero — exakt per Farbpipette aus letztem Frame des aktuellen Hero-Videos, 1:1 als `background-color` für nahtlosen Übergang |
| Basis warm (`--color-background-warm`) | `#F4F0EA` | Seitenhintergrund ab der Angebot-Sektion abwärts — per sanftem Gradient aus der Basis übergeleitet (siehe Entscheidung 2026-09-17), gilt für alle künftigen Sektionen unterhalb des Heros |
| Fläche (`--color-surface`) | `#FFFFFF` | Karten-Hintergrund (seit Entscheidung 2026-09-17) — Kontrast zur warmen Creme-Basis kommt jetzt über Weiß-auf-Creme statt Creme-auf-Creme |
| Fläche warm (`--color-surface-alt`) | `#F8F5F2` | Zweite, wärmere Fläche für Detail-Elemente (Chrome-Leisten, Wireframe-Tiles) — nicht mehr der Karten-Hintergrund selbst |
| Text | `#1E1D1B` | Fließtext, Headlines (Anthrazit statt Schwarz) |
| Text sekundär | `#6B6862` | Sublines, Meta-Text |
| Akzent | `#F58B2E` (Hover `#D9781F`) | Buttons, Links, Highlights, Icons, Ränder — sparsam, keine große Fläche. Verlauf: `#E08A3C`→`#F5943C`→`#F58B2E` final (2026-09-17, nach Live-Vergleich dreier Varianten gewählt), überall ersetzt |
| Akzent hell | `#F6E4CC` | Badges/Fills |
| Rahmen | `#E4DFD5` | Linien, Trenner |

Kontrast AA geprüft: Hero-Texte und CTA-Button geprüft (≥4,5:1, CTA nutzt dunklen Text `#1E1D1B` statt Weiß auf Akzent) — restliche Sektionen bei ihrem Bau prüfen

- Display-Font: Clash Display (Fontshare, self-hosted) — Hero-Headline, alle Zwischenüberschriften, große Nummern (01/02/03); bei kleineren Labels ggf. auf General Sans Bold ausweichen (beim Bauen prüfen)
- Body-Font: General Sans (Fontshare, self-hosted) — Navigation, Fließtext, Buttons, Labels, FAQ, Footer
- Beide Fonts self-hosted, `font-display: swap`, keine externen Font-CDN-URLs
- Layoutkonzept: Single-Page-Scroller, editorialer Rhythmus, Hero als Video-zu-HTML-Übergang
- Signature: Hero-Video (Laptop öffnet sich, Kamera zoomt rein, Zoom-Transition direkt in den echten HTML-Content) — passt zur Agentur, weil es die eigene Handwerksfähigkeit (Motion/Technik) direkt im ersten Moment zeigt. Exakte Animation-Specs: siehe `content.md` Abschnitt 1.

## 4. Seitenstruktur

Single-Page-Scroller (spätere Unterseiten pro Leistung optional). Reihenfolge zuletzt geändert
(2026-09-17): "Problem" wurde in "Angebot" aufgelöst (Intro-Text übernimmt die Schmerzpunkt-Ansprache),
Referenzen ist vor Ablauf gerückt.

| Sektion | Job | Status |
|---|---|---|
| Hero | Aufmerksamkeit, Positionierung, erster CTA | Gebaut |
| Angebot | Website / Sichtbarkeit / Automatisierung (optional), inkl. Intro zum Schmerzpunkt | Gebaut |
| Referenzen | 3 echte Case Studies mit Testimonial | Text + Screenshots final |
| Ablauf | 4 Schritte bis zur Lösung | Text final |
| Vergleichstabelle | Baukasten / Große Agentur / Nexora | Text final |
| FAQ | Einwände abbauen | Text final |
| Kontakt-CTA | Formular + Direkt-Kontakt-Card | Text final |
| Footer | Kontakt, Rechtliches | Text final |

Navigation: Floating Glass-Pill (`SiteNav.astro`), global in `Layout.astro`, erscheint erst beim
Scrollen über den Hero hinaus (siehe Entscheidung 2026-09-17). Nav-Links zeigen bereits auf
Anker, die noch nicht alle existieren (`#referenzen`, `#ablauf`, `#faq`) — wird beim Bau der
jeweiligen Sektion automatisch funktionsfähig, kein Fix nötig.

Alle Detailtexte, Struktur je Sektion und Animation-Specs: siehe `content.md` im Projektroot (Primärquelle, siehe Punkt 5).

## 5. Inhalte & Assets

- Texte: final, Primärquelle ist das Google Doc "website-content-final" (Drive-Ordner "Eigene Website") sowie die lokale `content.md` im Projektroot — nicht neu texten, nur strukturell umsetzen
- 3 echte Testimonials: Kanzlei Paetsch, Vita Passo, Kara Verpackung — Screenshots im Drive-Ordner "Eigene Website"
- Bilder: Referenz-Screenshots vorhanden (Drive-Ordner); für Mockups vorerst Platzhalterbilder erlaubt, klar markiert
- Hero-Video: liegt vor (Datei "Hero Video" im Drive-Ordner), inkl. Referenzbild "Hero Inspo.PNG" für Text-Overlay-Positionierung
- Logo: OFFEN — noch kein finales Logo (Firmenname selbst noch offen)
- Kontaktdaten: E-Mail julianhelms.digital@gmail.com (vorläufig), WhatsApp +49 152 24310832, Hamburg

## 6. Technik

- Stack: Astro
- Hosting: Netlify
- Formular-Anbindung: Astro + Resend (E-Mail-Versand, Free-Tier)
- WhatsApp-Link: wa.me, kein Kalender-Tool im Start-Setup
- Repository: https://github.com/JulianHelmsRepo/eigene-agentur-website

## 7. Rechtliches

- Impressum: OFFEN — noch zu erstellen
- Datenschutzerklärung: OFFEN — noch zu erstellen
- Externe Dienste: Fonts self-hosted (Clash Display, General Sans — keine Fremdserver), Video lokal gehostet
- Cookie-Banner nötig: Voraussichtlich nein — keine einwilligungspflichtigen Dienste geplant (final vor Livegang prüfen)
- Vor Livegang geprüft: OFFEN

## 8. CMS & Übergabe

- Kein CMS geplant — Eigenprojekt, Pflege durch mich selbst im Code

## 9. Rahmen

- Livegang: OFFEN
- Umfang: Single-Page-Scroller wie unter Punkt 4, Automatisierung ist eigenes Leistungsangebot der Seite, nicht Teil dieser Website selbst

## 10. Entscheidungen (chronologisch)

- 2026-09-16 — PROJEKT.md angelegt, Brief/Referenzen/Design-Token final aus vorliegendem Content-Dokument übernommen
- 2026-09-16 — Hero wird zuerst gebaut (Video-Hero mit `10k-websites`-Skill, Scroll-Übergänge mit `astro-motion-design`)
- 2026-09-16 — Astro-Projekt gescaffoldet (minimal template), Clash Display + General Sans self-hosted von Fontshare bezogen, `hero video.mp4` verarbeitet (mp4+webm, Poster- und Endframe extrahiert) und als autoplay Hero-Video eingebaut
- 2026-09-16 — Kicker-Darstellung nach `impeccable detect`-Fund entschärft: kein All-Caps/Tracking mehr (war als "Eyebrow-Chip über Headline"-Anti-Pattern erkannt), Text bleibt inhaltlich gleich
- 2026-09-16 — `impeccable detect` Fund "cream-palette" bewusst nicht umgesetzt: Hintergrundfarbe `#F1EDEB` ist exakt aus dem Hero-Video-Frame gepixelt (nahtloser Übergang Video→Website ist harte technische Anforderung), kein reflexhafter Default
- 2026-09-16 — `impeccable detect` Fund "content-hidden-at-rest" bewusst nicht vollständig umgesetzt: Der Text soll laut Brief erst erscheinen, wenn der Laptop im Video vollständig geöffnet ist (Kern der Choreografie) — als Absicherung wurde ein Hard-Fallback ergänzt, der den Text spätestens nach 3 Sekunden garantiert einblendet, falls Video/JS aus irgendeinem Grund nicht wie erwartet läuft
- 2026-09-16 — Hero-Video ausgetauscht ("neues hero video.mp4", 1926×1076 statt vorher 1280×720, in Originalauflösung ohne Downscaling verarbeitet, verlustarm mit CRF 16/24). Bildschirm endet jetzt komplett vollflächig in Weiß (`#FFFFFF`, an allen vier Ecken per Pixelprobe verifiziert), kein Laptop-Rand mehr sichtbar → CSS-Crop-Workaround (`transform: scale(1.15)`) aus Hero.astro entfernt, da nicht mehr nötig. Basis-Farbe von `#F1EDEB` auf `#FFFFFF` angepasst (neu aus Endframe gepixelt), da der neue Bildschirm spürbar heller ist. Fläche/Oberfläche dadurch auf `#F8F5F2` vereinheitlicht, damit Karten sich noch von der Basis abheben. `impeccable detect` danach erneut gelaufen: cream-palette-Fund ist entfallen (Basis ist jetzt Weiß statt Creme), content-hidden-at-rest-Fund bleibt wie oben begründet bestehen
- 2026-09-16 — Reveal-Timing an neues Video angepasst: `OPEN_THRESHOLD` von 1,4s auf 2,6s erhöht, weil das neue Video den Bildschirm langsamer öffnet als das alte (per Frame-Analyse: aufrecht/nicht mehr gekippt erst ab ca. 2,3–2,6s statt vorher ~1,5s). Bei 1,4s kollidierte der noch schräg geöffnete Bildschirmrand sichtbar mit dem Fließtext. Mit 2,6s erscheint der Text erst, wenn der Screen vollständig aufrecht steht — Überlappung mit dem Text während der anschließenden Zoom-Phase ist laut Vorgabe gewollt und kein Fehler
- 2026-09-16 — Hero-Video erneut ausgetauscht ("neustes hero video final.mp4", gleiche Auflösung 1926×1076, gleiche Verarbeitung mp4+webm verlustarm CRF 16/24). Endframe wieder komplett vollflächig Weiß an allen vier Ecken per Pixelprobe verifiziert — kein Crop-Workaround nötig, Basis-Farbe `#FFFFFF` passt unverändert. Öffnungsbewegung im neuen Video per Frame-für-Frame-Analyse (10fps-Extraktion) genau untersucht: Bildschirm öffnet sich UND zoomt gleichzeitig, wird erst ab ca. 3,1–3,4s wirklich aufrecht/ungekippt — zu diesem Zeitpunkt überlappt der Screen aber bereits sichtbar mit der oberen Headline-Zeile, weil Öffnen und Zoomen bei diesem Video nicht nacheinander, sondern gleichzeitig ablaufen. Eine Trigger-Zeit mit gleichzeitig null Überlappung UND vollständig aufrechtem Screen existiert bei diesem Video schlicht nicht. Priorität nach Kundenvorgabe: kein sichtbar schräger/kippender Rand beim ersten Kontakt mit dem Text (das sah wie ein Fehler aus), Überlappung an sich in der Zoom-Phase ist ausdrücklich in Ordnung. `OPEN_THRESHOLD` daher auf 3,2s gesetzt (Bildschirm dort nachweislich gerade/nicht mehr gekippt, sauberer horizontaler Schnitt durch den Text statt schräger Kante). Getestet: Live-Screenshots von laufendem Video in Headless-Chromium sind unzuverlässig (zeigen teils das statische Fallback-Bild statt den echten Videoframe) — verlässliche Verifikation lief über pausiertes Video bei exaktem `currentTime`
- 2026-09-16 — Bug behoben: Der 3-Sekunden-Notfall-Fallback in Hero.astro lief in Echtzeit (`setTimeout(..., 3000)`), während `OPEN_THRESHOLD` auf 3,2s **Videozeit** stand — bei 1:1-Echtzeitwiedergabe hat der Fallback fast immer VOR dem eigentlichen Trigger gefeuert und dabei per `is-static`-Klasse das komplette `<video>`-Element ausgeblendet (auf das statische Endframe-Bild umgeschaltet), noch bevor das Video zu Ende war. Ursache: Text-Reveal und Video-Sichtbarkeit waren im selben Fallback-Pfad verdrahtet. Fix: beide entkoppelt — der Notfall-Fallback (jetzt 10s, deutlich über Videodauer + Threshold) blendet nur noch den Text ein und rührt das Video nicht mehr an; `is-static` wird nur noch bei echtem Video-Fehler oder `prefers-reduced-motion` gesetzt. Mit einem 200ms-Zustandsmonitor über die komplette Wiedergabedauer verifiziert: Video läuft ohne Unterbrechung von 0 bis 6,04s durch (`paused` bleibt `false`), Text erscheint bei ~3,3–3,5s zusätzlich obendrüber, `is-static` wird zu keinem Zeitpunkt gesetzt
- 2026-09-17 — Farbschema erneut angepasst (Video-Screen ist jetzt Weiß): CSS-Variable `--color-base` in `--color-background` umbenannt (Wert unverändert `#FFFFFF`), Kartenfläche bleibt `--color-surface-alt` = `#F8F5F2`. content.md aktualisiert: Sektion "Problem" wurde in "Angebot" aufgelöst (Intro-Absatz übernimmt die Schmerzpunkt-Ansprache), Referenzen vor Ablauf verschoben — Seitenstruktur in Punkt 4 entsprechend angepasst
- 2026-09-17 — Angebot-Sektion gebaut (`src/components/Angebot.astro`): Intro + 3 Karten (Website/Sichtbarkeit/Automatisierung) mit Outline-Icons in Akzent-Farbe auf hellem Akzent-Tile, dünner oberer Akzent-Rahmen, gestaffelter Scroll-Reveal via GSAP ScrollTrigger (Inhalte per Default sichtbar, JS blendet nur progressiv ein — kein "content-hidden-at-rest"). `impeccable detect` Fund "border-accent-on-rounded" technisch behoben (Akzent-Rahmen jetzt als `::before` mit `overflow:hidden`-Clipping statt hartem `border-top`, dadurch sauber gerundet). Zwei Funde bewusst nicht umgesetzt, weil sie exakt der expliziten Vorgabe aus dem Auftrag widersprechen: "icon-tile-stack" (rundes Icon-Tile über der Headline) und "side-tab" (farbiger oberer Kartenrahmen) — beide waren wortwörtlich so vom Kunden spezifiziert, daher zur Entscheidung vorgelegt statt eigenmächtig geändert
- 2026-09-17 — Design-Constraint "Kein Glassmorphism als Standard" aus content.md entfernt (Kunde erlaubt es jetzt gezielt). Angebot-Sektion umgebaut auf asymmetrisches Layout: Website-Karte (~60%) als Hauptkarte mit Browser-Fenster-Mockup (Traffic-Light-Punkte, Adresszeile, abstraktes Wireframe aus reinem CSS statt Screenshot) plus bewusstem Glassmorphism-Akzent (`rgba(248,245,242,.75)`, `backdrop-filter: blur(14px)`, heller Rand) — nur auf dieser einen Karte, kein Standard. Sichtbarkeit/Automatisierung (~40%, gestapelt) bekommen stattdessen macOS-Squircle-Icons mit Verlauf/Tiefe statt flachem Icon-Badge. Seiten-Hintergrund ab dieser Sektion per `linear-gradient(180deg, --color-background 0px, --color-background-warm 480px)` von Hero-Weiß zu warmem Creme (`#F4F0EA`, neues Token `--color-background-warm`) übergeleitet, ohne den nahtlosen Video-Übergang im Hero zu berühren
- 2026-09-17 — Floating Glass-Pill-Navigation gebaut (`src/components/SiteNav.astro`, global in `Layout.astro` eingebunden): unsichtbar solange der Hero im Viewport ist, blendet erst per `IntersectionObserver` auf dem Hero-Element ein/aus, sobald darüber hinausgescrollt wird. Logo links, Nav-Links (Angebot/Referenzen/Ablauf/FAQ) mittig, CTA "Erstgespräch" rechts als einziges farbiges Element. Auf Mobile (≤720px) werden die Nav-Links ausgeblendet, nur Logo+CTA bleiben — bewusste Vereinfachung, volles Mobilmenü folgt, sobald alle Sektionen stehen
- 2026-09-17 — `impeccable detect` Fund "low-contrast" auf der Website-Hauptkarte (Glassmorphism) geprüft und als Fehlalarm verifiziert: Werte schwankten zwischen zwei Läufen (1.1–1.2:1 / 2.1–10.8:1), das ist ein Hinweis auf einen Mess-Artefakt statt eines echten, reproduzierbaren Zustands. Per Hand nachgerechnet (WCAG-Formel): Text `#6B6862` auf der Glas-Karte ergibt selbst im ungünstigsten Fall (Karte über reinem Weiß geblendet) 5,22:1, über der Creme-Basis 5,06:1 — beides über der 4,5:1-Grenze. Direkter Pixel-Crop im echten Browser (nach Abschluss der Reveal-Animation, `opacity:1` verifiziert) zeigt klar lesbaren Text. Vermutliche Ursache: `backdrop-filter` wird im Headless-Chromium des Prüf-Tools nicht immer korrekt gerendert. `ignore-value`-Unterdrückung mit `--file`-Scope hat keine Wirkung gezeigt (Fund ist offenbar nicht datei-attribuierbar) und wurde wieder zurückgesetzt (`impeccable hooks reset`) statt eine wirkungslose Konfiguration stehen zu lassen — Fund bleibt als dokumentierter, mathematisch widerlegter Fehlalarm bestehen
- 2026-09-17 — Zweite Review-Runde: Akzentfarbe auf `#F5943C` (Hover `#E0822E`) geändert, überall ersetzt (Token, hartkodierter CTA-Glow in Hero.astro). Angebot-Karten komplett neu gebaut (`src/components/Angebot.astro`): Karte selbst ist jetzt das Browser-Fenster (Chrome-Leiste mit Traffic-Light-Punkten + Adresszeile direkt in jeder Karte, kein verschachteltes Mockup mehr), kein Icon-Tile und kein separater Akzent-Rahmen mehr — dadurch lösen sich die offenen `impeccable`-Funde "icon-tile-stack" und "side-tab" von selbst auf (nach Umbau erneut geprüft: beide Funde tatsächlich verschwunden). Layout jetzt eine Reihe mit gestaffelter Breite; Verhältnis 5fr/3fr/2fr (≈50/30/20) wirkte bei der Automatisierung-Karte zu gequetscht (Text riss nach 2–3 Wörtern um) → auf `4.5fr/3fr/2.5fr` (≈45/30/25) angepasst, seitdem gut lesbar. Karten-Hintergrund auf `#FFFFFF` (`--color-surface`) geändert, `--color-surface-alt` (`#F8F5F2`) bleibt als zweite Fläche für Detail-Elemente. Glassmorphism bleibt exklusiv auf der Website-Karte. Pill-Nav transparenter gemacht (Opacity 0.7→0.52, Blur 14px→20px, Schatten reduziert, dafür 1px Akzent-Rand `rgba(245,148,60,0.4)`). Beim Testen der Nav-Sichtbarkeit fiel ein Mess-Artefakt auf: bei ungewöhnlich hohem Test-Viewport (1000px) reichte die inzwischen kürzere Angebot-Sektion nicht aus, um den Hero beim Scrollen vollständig aus dem Viewport zu schieben (Seite nur 1926px hoch) — mit realistischer Viewport-Höhe (800px) funktioniert die Nav-Einblendung einwandfrei; kein Code-Fehler, nur ein zu großzügig gewählter Test-Viewport
- 2026-09-17 — Dritte Review-Runde (Feedback zum letzten Build): Nav-Kollision mit Angebot-Headline behoben — zwei Maßnahmen kombiniert: (a) Trigger-Zeitpunkt der Nav-Einblendung von "sofort bei Hero-Ende" auf "Hero-Ende + 65% einer weiteren Hero-Höhe" verzögert (adaptiv gedeckelt auf das tatsächlich verfügbare Scroll-Polster, damit die Nav auf der noch kurzen Seite mit nur 2 Sektionen nicht unerreichbar wird — sobald mehr Sektionen unten dazukommen, nähert sich der Trigger von selbst den vollen 65%; **To-Do:** einmal gegenprüfen, wenn die ganze Seite steht), (b) zusätzliche 90px `padding-top` auf die Angebot-Sektion als Sicherheitsabstand. Pill-Nav auf `width: min(94%, 72rem)` (Referenz flow8.de) verbreitert, `justify-content: space-between` statt schmalem Content-Fit. Angebot-Intro-Container von `42rem` auf `52rem` verbreitert, Intro-Text-Max-Width von `58ch` auf `68ch` — Headline passt jetzt auf 2 Zeilen, Intro-Text auf 3 Zeilen (beide bleiben linksbündig, wie gewünscht). Intro-Text 1:1 wie vorgegeben gekürzt (", bevor es losging" gestrichen), auch in `content.md` nachgezogen. Glassmorphism auf der Website-Karte komplett entfernt, alle drei Karten jetzt identisch: Titelleiste + Kartenrahmen in Anthrazit `#2A2825` (dunkles Browser-Fenster), Traffic-Light-Punkte bleiben in ihren echten Farben (Rot/Gelb/Grün — realistischer als monochrom, auch im echten Dark Mode üblich), nur die Adresszeile wurde auf hellen/weißen Text mit dunkel-transparentem Pill-Hintergrund umgestellt, da Weiß-auf-Weiß sonst unlesbar gewesen wäre. `impeccable detect` läuft danach komplett sauber durch (0 Funde) — der bisherige low-contrast-Fehlalarm ist mit dem Glassmorphism-Entfernen von selbst verschwunden
- 2026-09-17 — Vierte Review-Runde: Kunde meldete, die Karten-Reveal-Animation zeige "keinerlei Effekt". Mechanik selbst war korrekt (per Frame-Trace verifiziert: sauberer gestaffelter Fade+Slide), wahrscheinliche Ursache ein klassischer GSAP/Webfont-Bug — `ScrollTrigger` berechnet Trigger-Positionen beim Setup, aber self-hosted Fonts laden asynchron nach und verschieben das Layout (Reflow), wodurch die gecachten Trigger-Positionen im echten Betrieb (mit realistischem Font-Ladezeitpunkt) nicht mehr stimmen können, in einem schnellen lokalen Test mit bereits gecachten Fonts aber unauffällig bleiben. Fix: `document.fonts.ready.then(() => ScrollTrigger.refresh())` sowie ein zusätzlicher Refresh auf `window.load` ergänzt. Trigger-Punkt von "top 85%" auf "top 88%" verfeinert. Nav-Breite auf `width: min(90%, 63rem)` reduziert (vorher `min(94%, 72rem)` deckte sich fast mit der Content-Breite und wirkte blockig) — jetzt sichtbarer Rand links/rechts zum Content. Temporäre Vergleichsseite `src/pages/akzent-vergleich.astro` angelegt (nicht Teil der echten Seite, `noindex`), zeigt 3 Akzentfarb-Varianten (`#F5943C` aktuell / `#F58B2E` / `#F97316`) nebeneinander im Kontext von Nav-CTA, Hero-CTA, Angebot-Karten-Wireframe und Headline-Hervorhebung
- 2026-09-17 — Fünfte Review-Runde: Variante (b) `#F58B2E` (Hover `#D9781F`) final gewählt, überall ersetzt (Token, hartkodierte rgba-Werte in Hero.astro und SiteNav.astro, `content.md`). Vergleichsseite `akzent-vergleich.astro` wieder entfernt. Karten-Reveal-Animation überarbeitet: Bewegungsmuster von reinem Slide-in (`translateY(24px)`) auf ein "aufklappendes Fenster" geändert — Start bei `scale(0.95)` + Opacity 0, Ziel `scale(1)` + Opacity 1, `ease: power2.out`, Dauer von 0.7s auf 0.55s reduziert (Zielkorridor 500–600ms), gestaffelter 100ms-Versatz unverändert. Per Frame-Trace verifiziert: sauberer, klar sichtbarer Verlauf über die volle Dauer

## 11. Gelernt in diesem Projekt

- `impeccable detect` läuft nur gegen eine laufende URL zuverlässig (Astro-Dateien direkt scannen liefert keine Treffer) — vor dem Prüfen `astro dev --background` starten und gegen `http://localhost:4321/` prüfen
- Fontshare stellt unter `https://api.fontshare.com/v2/fonts/download/<family-slug>` direkte ZIP-Downloads für Self-Hosting bereit (kein manuelles Herunterladen über die Website nötig)
- Bei Tests für "Element erscheint erst nach Scroll über Section X hinaus": Test-Viewport realistisch wählen (~800px Höhe). Ein zu hoher Test-Viewport (z. B. 1000px) kann bei noch kurzen Seiten dazu führen, dass selbst ein Scroll bis ganz nach unten die erste Section nicht vollständig aus dem sichtbaren Bereich schiebt — sieht wie ein Bug aus, ist aber nur zu wenig Seiteninhalt relativ zum Viewport
- GSAP `ScrollTrigger` + self-hosted Fonts: immer `document.fonts.ready.then(() => ScrollTrigger.refresh())` ergänzen. Self-hosted Fonts laden asynchron nach und verschieben per Reflow die Layout-Positionen, auf denen ScrollTrigger seine Trigger-Punkte beim Setup berechnet hat — ohne Refresh können Scroll-Reveals im echten Betrieb "gar nicht" oder am falschen Punkt feuern, obwohl sie in einem schnellen lokalen Test (Fonts schon gecacht) unauffällig wirken. Für jedes künftige Projekt mit GSAP + self-hosted Fonts von Anfang an einbauen, nicht erst wenn es auffällt

## 12. Offene Punkte

- [ ] Firmenname final festlegen (Nexora = Arbeitsplatzhalter)
- [ ] E-Mail auf Firmen-Domain umziehen
- [ ] Impressum & Datenschutz erstellen
- [ ] Kontrast AA-Prüfung vor Livegang
- [ ] Cookie-Banner-Entscheidung final vor Livegang bestätigen
