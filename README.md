# Eco-GenX monitoring atlas — GitHub Pages demo

Interactieve, statische website in Eco-GenX-stijl. Leaflet-kaart, projectpictogrammen, klikbare infopanelen en Chart.js-grafieken.

## Snel publiceren

1. Maak op GitHub een repository, bijvoorbeeld `eco-genx-monitoring`.
2. Upload **alle bestanden én submappen** uit deze map naar de hoofdmap van de repository (niet de bovenliggende map).
3. Ga naar **Settings → Pages → Build and deployment** en kies **Deploy from a branch**, branch **main**, map **/(root)**. Klik **Save**.
4. Je publieke adres wordt `https://GEBRUIKERSNAAM.github.io/eco-genx-monitoring/`.

**Lokaal testen:** start in deze map `python -m http.server 8000` en open `http://localhost:8000`. Alleen dubbelklikken op index.html kan verhinderen dat CSV-bestanden worden ingelezen door browserbeveiliging.

## Inhoud

- `index.html`, `style.css`, `app.js`: complete website.
- `assets/`: twee door de gebruiker aangeleverde foto's van het drijvende wetland.
- `data/`: drie originele CSV-bestanden voor PO17 (bodemtemperatuur, bodemwaterspanning, batterijspanning).
- PO17 is voorlopig gekoppeld aan het Alken-vlot als demonstratie. **Deze koppeling is niet geverifieerd.** Pas dit aan zodra de werkelijke meetlocatie bekend is.
- Andere natte-wetlandgrafieken en de Melsbroek-jaarreeksen zijn gesimuleerd en expliciet gemarkeerd.
- De projectcoördinaten zijn **indicatieve kaartposities** en geen vastgestelde meetlocaties.

## Aanpassen

- Locaties, coördinaten, projecttypes en omschrijvingen: array `points` bovenaan `app.js`.
- Jaarlijkse chemische voorbeeldmetingen: `mock` in `app.js`.
- Vervang voor productie de simulaties door gecontroleerde meettabellen. Gebruik voor boomcores en grondwater de correcte analytische eenheden, rapportagegrenzen en meetpunt-ID's.
- Kaartlagen, grafieken en fonts laden via CDN. Internetverbinding is vereist.
- De site heeft geen server, login of automatische dataverbinding; CSV-updates verlopen via GitHub-commits.
- Publiceer geen vertrouwelijke projectcoördinaten of klantgegevens op een openbare GitHub Pages-site.
