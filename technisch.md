---
layout: default
---

[back](.)

# Backend

De backend maakt gebruik van Google's Firebase, een MBaaS. Deze houdt de data bij en stuurt in realtime meldingen naar alle frontends wanneer er aanpassingen gebeurd zijn. Zo is de data in alle frontends steeds up to date zonder dat er een actie van de gebruiker vereist is.

Er is een tweede backend voor het uitnodigingssysteem, met dit systeem kunnen werkgevers hun werknemers uitnodigingen sturen om lid te worden van hun bedrijf. Deze backend werd geschreven in Node.js en luistert naar datawijzigingen in de Firebase. Via Mailgun worden emails verstuurd met daarin een unieke code. Bij het ingeven van deze code in de Androidapplicatie wordt de werknemer in de backend toegevoegd aan het bedrijf.

# Webclient

De webclient is zonder framework geschreven. Het bestaat volledig uit statische pagina's. Er is gebruik gemaakt van de Firebasebibliotheek om data te delen met de rest van de applicatie en de Google Chartsbibliotheek om een tijdslijn te tekenen.

De site is geschreven in een combinatie van JavaScript (met browserify om packages te integreren) voor de interacties, Sass voor de stijl en Pug als templating engine. De site wordt door Gulp gebuild en met behulp van Travis CI omgezet naar een statisch site en vervolgens gedeployed op de `gh-pages` branch van het project op GitHub. Daardoor wordt er een GitHub Pages site gecreëerd. Voor https, caching enzovoort gaat al het verkeer eerst via Cloudflare als CDN.

Het eindresultaat is zichtbaar op [punchtime.io](https://punchtime.io).

# Androidclient

De Androidapplicatie is geschreven in Java om optimaal gebruik te kunnen maken van de API's van het besturingssysteem.

Ook in de Androidapplicatie wordt er gebruik gemaakt van Firebase om de data bij te houden, hier geïmporteerd als een SDK. Er wordt ook gebruik gemaakt van een aangepaste library om speciale toggles te maken, een library om eenvoudig een kalender weer te geven en een library om grafieken te tekenen.

Er is zo veel mogelijk gebruikt gemaakt van vectordata voor de afbeeldingen en icoontjes, wat ervoor zorgt dat deze er scherp uit zien op elke schermgrootte en dat met een kleinere bestandsgrootte.
