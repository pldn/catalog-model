# Inleiding

De PLDN Werkgroep ‘Nederlands profiel voor stelselcatalogi’ heeft als ambitie een basisprofiel voor stlelselcatalogi te beschrijven. De eerste stap daarin is een basisprofiel voor begrippencatalogi, waarmee verschillende begrippencatalogi interoperabel ingericht kunnen worden. Het doel is een samenhangend stelsel van begrippencatogi, waarbij elke begrippencatalogus een samenhangend domein representeert. Voorbeelden zijn de begrippencatalogus van de basisregistraties, de begrippencatalogus voor het DSO en de begrippencatalogus voor het Zorgeloos Vastgoed afsprakenstelsel. Daartoe willen we het uiteindelijke profiel als aanbevolen standaard of als pas-toe-leg-uit standaard aanbieden aan het Forum Standaardisatie.

Een begrippencatalogus bestaat uit één of meerdere begrippenkaders. Elk begrippenkader is de beschrijving van de begrippen die als samenhangend geheel wordt beheerd. Een begrippencatalogus heeft raakvlakken met andere soorten catalogi:
- De catalogus met een overzicht van waardelijsten met referentiegegevens of classificaties.
- De catalogus met een beschrijving van de gegevens en hun structuur in de vorm van een informatiemodel. Hiervoor bestaat al het  MIM (Metamodel voor InformatieModellelering).
- De catalogus met een beschrijving van de uitwisselingsstandaard. Ook hiervoor kunnen bestaande standaarden als XML, OAS3 en NL api strategie worden gebruikt.

Een stelsel catalogus is een catalogus die bestaat uit een begrippencatalogus, waardelijstencatalogus, informatiemodellen en uitwisselingsstandaarden, inclusief de samenhang tussen deze deelcatalogi. De meeste stelselcatalogi bevatten nog niet al deze elementen, maar een begrippencatalogus is wel altijd een onderdeel. Een randvoorwaarde is dat de begrippenkaders die in een begrippencatalogus worden opgenomen op een interoperabele manier zijn beschreven.

De voorliggende standaard richt zich op het beschrijven van een begrippenkader met begrippen en collecties van begrippen. Waar in het Nederlands vaak de term "begrip" wordt gebruikt, is hiervoor in het Engels de term "concept" gebruikelijk. Soms wordt ook in het Nederlandsde term "concept" gebruikt. In dit document zullen we de Nederlandse term "begrip" gebruiken, tenzij we expliciet willen verwijzen naar de Engelse term (bijvoorbeeld bij de aansluiting op internationale standaarden).

Met de beschrijving van een begrip proberen we de betekenis van dit begrip te "vangen" zoals deze in het betreffende domein wordt beoogd. Hiervoor hebben we enkele middelen:
- De basis voor een begrip is de voorkeursterm waarmee we dit begrip duiden. Mogelijk is het begrip ook bekend onder andere alternatieve termen, die kunnen we daarbij vermelden;
- Daarnaast kunnen we een verwoording geven van de betekenis van het begrip in natuurlijke taal. Dit kan een (formele) definitie zijn, maar ook een uitleg in klare taal ([taalniveau B1](https://www.communicatierijk.nl/vakkennis/rijkswebsites/aanbevolen-richtlijnen/taalniveau-b1)) behoort tot de mogelijkheden;
- We kunnen begrippen onderling aan elkaar relateren, zodat duidelijk is hoe de begrippen zich tot elkaar verhouden;
- We kunnen verwijzen naar een bron waar de betekenis van het begrip staat beschreven, zoals in wet- en regelgeving, standaarden, werkinstructies en afspraken;
- Door voorbeelden van een begrip te benoemen.

Deze middelen vullen elkaar aan: het is niet zo dat het ene middel "beter" is dan het ander, juist door in de beschrijving meerdere middelen te gebruiken die elkaar aanvullen (en elkaar niet tegenspreken!) ontstaat een beschrijving die de betekenis van een begrip optimaal "vangt".

Daarbij besteden we aandacht aan de verschillende niveaus van detaillering voor het beschrijven van begrippen. Dit begint met de minimale beschrijving van de voorkeursterm en een verwoording van de betekenis (de "definitie"), waarbij we naast een definitie ook een publieksvriendelijke variant op taalniveau B2 willen hebben: de "uitleg". Door hiërarchische relaties toe te voegen ontstaat een taxonomie en door nog meer verbanden tussen begrippen toe te voegen ontstaat een (ISO25964 compatible) thesaurus. We onderkennen daarbij ook het belang in specifieke domeinen om meer semantiek toevoegen: dit zien wij als uitbreidingen op het basisprofiel.

De elementen in deze standaard, begrippenkader, begrip en collectie, worden in 3 stappen beschreven:
- Bij ieder begrip in deze standaard starten we met techniekonafhankelijke principes voor het beschrijven van een begrippenkader, de overeengekomen richtlijnen.
- Iedere eigenschap van een begrip beschrijven we inhoudelijk met een definitie, uitleg, toelichting, één of meerdere redactionele notities en eventueel een voorbeeld.
- Daarnaast beschrijven we per eigenschap van een begrip of deze verplicht/aanbevolen/optioneel is en hoe kan worden gevalideerd dat deze beschrijving aan de standaard voldoet. Hiermee bedoelen we:
  - Verplicht: je voldoet (alleen) aan het profiel als voldaan is aan de voorwaarden voor het gebruik van deze eigenschap;
  - Aanbevolen: je voldoet aan het profiel, zelfs als je geen gebruik maakt van deze eigenschap. Wel wordt het gebruik aanbevolen en zul je moet uitleggen waarom je geen gebruik maakt van deze eigenschap;
  - Optioneel: je voldoet aan het profiel, ook als je geen gebruik maakt van deze eigenschap.

Uitbreidingen van het basisprofiel zijn altijd optioneel.

Voor het beschrijven van het profiel maken we gebruik van bestaande W3C standaarden. Dit leidt tot een abstracte syntax van het profiel uitgedrukt in de SHACL standaard. Daarnaast geven we een taalbinding van deze abstracte syntax naar andere bestaande W3C standaarden, zoals SKOS en DublinCore. Voor de abstracte syntax gebruiken we URI's die uitgedrukt worden in de Engelse taal, om zo direct een internationale aansluiting te houden. De abstracte syntax zal daarnaast Nederlandse labels kennen die in de deze lopende (Nederlandstalige) tekst zal worden gebruikt. De meerwaarde van het gebruik van SHACL is dat deze praktische handvatten biedt bij het toepassen van deze bestaande standaarden, inclusief een validatiemogelijkheid. Door het geven van de taalbinding naar de andere W3C standaarden bieden we een profiel dat direct kan worden begrepen door de internationale (internet) gemeenschap. Specifiek voor de Nederlandse (overheids)situatie geldt dat we hierbij aansluiten op de standaarden zoals opgenomen op de [Pas-Toe-Of-Leg-Uit lijst](https://www.forumstandaardisatie.nl/open-standaarden/verplicht) van het Forum Standaardisatie.
