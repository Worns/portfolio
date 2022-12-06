---
Title: Load
Description: Loading time
Template: analys
---

# Prestanda

Analys av tre webbplatsers laddningstid och användbarhet.

## Urval

Jag har valt tre hemsidor från tre olika kommuner och jag valde ut [Kiruna](https://www.kiruna.se/) kommun, min hemkommun [Karlskoga](https://www.karlskoga.se/) och Sveriges största kommun [Stockholm](https://start.stockholm/).

## Metod

Jag har använt mig av:

- [Google Developers Pagespeed Insight](https://pagespeed.web.dev/) (analysera prestandan)
- Mozilla Firefox DevTools (mäta laddningstiden samt filstorlekar på hemsidorna)
- [Google Kalkylark](https://www.google.se/intl/sv/sheets/about/) (redovisa mätresultat)

Jag mäter laddningstiden genom att köra en hard reload (CTRL + SHIFT + R) för det blir andra mätvärden annars med tanke på vad som sparats i cache. För att få större precision på medelvärdena så valde jag att göra varje mätning 5 ggr.

## Resultat

### Mätresultat

<iframe class="google-sheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSPMApPj4I1DygcKXNTsti9JeGuxcr1vqKaSNZab47TjMQE0xaZw06ixp0FjxgNbcggAIS8qLQMVA5J/pubhtml?widget=true&amp;headers=false"></iframe>

### Karlskoga kommun

<img src="%assets_url%/img/karlskoga-startpage.webp" alt="IMDB" width="100%"/>

Laddningstiden för Karlskogas indexsida var 2.24 sekunder vilket får anses som en godkänd laddningstid.
Pagespeed Insight ger en prestandapoäng på 39 för den mobila versionen samt 75 för desktop versionen av indexsidan.
Karlskogas indexsida har en storlek på 5,65 MB och där är 3,11 MB bilder.
För att få ner laddningstiden så bör deras huvudfokus vara att optimera bilderna mer och de bör förslagsvis använda webp för att göra det. Deras mobila sida kräver en rejäl optimering av bilderna och fördröjning bilder som inte visas direkt på skärmen. Bör även ta bort JavaScript som inte används av sidan och fördröja inläsningen av övriga skript tills de används.

### Kiruna kommun

<img src="%assets_url%/img/kiruna-startpage.webp" alt="IMDB" width="100%"/>

Laddningstiden för Kirunas indexsida var hela 4.91 sekunder vilket får anses som långsamt.
Pagespeed Insight ger en prestandapoäng på 35 för den mobila versionen samt 48 för desktop versionen av indexsidan.
Kiruna har mycket bilder som tar utrymme och sidan läser in alla bilderna direkt.
Hemsidans indexsida har en storlek på 16.24 MB och där är 12.71 MB bilder så de bör optimera bilderna för att få ner laddningstiden rejält, flera av bilderna har en filstorlek över 1 MB och där finns det mycket förbättringsutrymme. Skulle rekommendera att de konverterar bilderna till webp så hade de fått ner bildstorlekarna rejält men ändå bibehålla bra bildkvalite.
De kan även fördröja inläsningen av bilder som inte visas direkt på skärmen för att få en ännu bättre laddningstid och i detta fallet är det huvudskälet till varför sidan laddar så långsamt med tanke på att bilderna inte är optimerade heller.
Den mobila versionen kräver också samma åtgärder som desktop versionen samt även fördröja JavaScript som laddas in som är av mindre nytta.

### Stockholm kommun

<img src="%assets_url%/img/stockholm-startpage.webp" alt="IMDB" width="100%"/>

Laddningstiden för Stockholms indexsida var 1.41 sekunder vilket får anses som en snabb laddningstid.
Pagespeed Insight ger en prestandapoäng på 68 för den mobila versionen samt 79 för desktop versionen av indexsidan.
Stockholms indexsida har en storlek på 1,81 MB där 0,81 MB är bilder.
De har så pass lite innehåll i bilder eller annat som tar någon större plats så det finns inte så mycket laddningstid att spara in på desktop versionen åtminstone. Den mobila versionen däremot kan de optimera sina bilder för och även fördröja JavaScript som inte behöver laddas in direkt.

## Analys

Jag har fokuserat på indexsidan i de enskilda rapporterna eftersom jag anser att den är viktigast men här i analysen kommer jag även ta hänsyn till de andra undersidorna när jag ska rangordna sidorna.
I mitt tycke bör en hemsida ha en laddningstid som är runt 2-3 sekunder max.
Den gemensamma nämnaren för alla hemsidorna har varit att bilderna behöver optimeras i olika mån för desktop och mobil. På den mobila sidan så bör alla sidorna fördröja scripten som inte behöver aktiveras direkt när man laddar in sidan.

Min ranking för de olika sidorna baserat på enbart prestanda är följande:

1. Stockholm
   <p>Är den klara vinnaren om man ser till prestandan även om de har byggt en hemsida som laddar in mycket mindre resurser jämfört med Karlskoga och Kiruna. Har en väldigt snabb laddningstid. Både desktop och den mobila versionen är en vinnare på prestandapoängen.</p>
2. Karlskoga
   <p>Ligger i stort sett mittimellan Stockholm och Kiruna på storlek och prestanda där de har en godkänd desktop version men det finns mer att önska från den mobila versionen. Godkänd laddningstid.</p>
3. Kiruna
   <p>Har använt väldigt mycket mer utrymme än både Karlskogas och Stockholms hemsida och deras prestanda är den sämsta sammanfattat. Både desktop och den mobila versionen är prestandamässigt väldigt dålig med överlägset sämsta laddningstiden också.</p>
