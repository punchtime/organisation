---
layout: default
---

[back](.)

# Backend

Voor de backend is er gebruik gemaakt van Google's Firebase, een MBaaS. Deze houdt de realtime data bij en geeft meldingen wanneer er aanpassingen zijn.

Er is een aparte backendservice, geschreven in Nodejs, die luistert naar data van Firebase en via Mailgun emails stuurt voor uitnodigingen en mogelijks andere dingen in de toekomst.

# Webclient

De webclient is zonder framework geschreven. Het bestaat volledig uit een aantal statische pagina's. Er is gebruik gemaakt van de Firebasebibliotheek om data te delen met de rest van de applicatie en de Google Chartsbibliotheek om een tijdslijn te tekenen.

De site is geschreven in een combinatie van JavaScript (met browserify om packages te integreren) voor de interacties, scss voor de stijling en Pug (tot recent Jade) als markup. Deze worden door middel van Gulp als task runner via Travis als CD omgezet naar een statisch geheel en dan op een `gh-pages` branch van een project op GitHub gezet. Daardoor wordt er een GitHub Pages site gecreëerd. Voor https, caching etc. gaat al het verkeer eerst via Cloudflare als CDN.

Het totaal is zichtbaar op [punchtime.io](https://punchtime.io).

# Androidclient

De applicatie is geschreven in Java zodoende een integratie met het operatiesysteem op een optimale manier te kunnen voorzien.

Ook in de applicatie wordt er gebruik gemaakt van Firebase om de data bij te houden, hier geïmporteerd als een sdk. Er wordt ook gebruik gemaakt van een aangepaste library om speciale toggles te maken, een library om eenvoudig een kalender bij te houden, en een library om grafieken te tekenen.

Er is zo veel mogelijk gebruikt gemaakt van vectordata voor de afbeeldingen en icoontjes, wat ervoor zorgt dat deze er scherp uit zien op elke schermgrootte en dat met een kleinere bestandsgrootte.
