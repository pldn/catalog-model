# Toepassingsprofiel in RDF
Dit hoofdstuk beschrijft de set aan afspraken voor het toepassen van de kenmerken zoals beschreven in hoofdstuk 2 op basis van bestaande semantische standaarden. Deze afspraken zijn vastgelegd in een RDF model.
Een RDF model bestaat uit twee delen; 1) een RDF vocabulaire en 2) een RDF Shapesgraph. Als RDF vocabulaire hanteren we bestaande W3C standaarden. Welke dit zijn en hoe deze zich verhouden tot het conceptueel model wordt beschreven in sectie [Uitwerking](#uitwerking). Hoe deze vocabulaires toegepast moeten worden, conform het conceptuele model, is beschreven in sectie [Specificatie](#specificatie).
Dit hoofdstuk is normatief wanneer begrippen via het web worden ontsloten.

## Overzicht

Het onderstaande diagram geeft een overzicht van de taalbinding in RDF die bij het conceptuele model gedefinieerd is.

![](/respec/media/skos-ap-nl.png "Diagram: Toepassingsprofiel skos")

## Uitwerking
Voor het representeren van de conceptuele elementen in RDF maken we gebruik van de volgende vocabulaires 1) RDF(s), 2) SKOS, 3) DCTERMS, 4) FOAF en 5) ISOTHES. We geven de taalbinding voor types en kenmerken apart in [types](#types) en [eigenschappen](#eigenschappen)


### Types

| Conceptueel element | Taalbinding in RDF                                                      |
| ------------------- | ----------------------------------------------------------------------- |
| [=begrip=]          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=begrippenkader=]  | [skos:ConceptScheme](http://www.w3.org/2004/02/skos/core#ConceptScheme) |
| [=brondocument=]    | [rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource)          |
| [=collectie=]       | [skos:Collection](http://www.w3.org/2004/02/skos/core#Collection)       |

<div class="note">
Een brondocument heeft niet één definitieve taalbinding. Dit komt omdat er veel verschillende toepasbare standaarden zijn op dit gebied waar de één niet per definitie beter is dan een andere. In dit profiel is wordt aangeraden om een brondocument te zien als als een `foaf:Document`. Andere toepasbare standaarden (niet limitatief) zijn bijvoorbeeld:
<ul>
<li>DublinCore (<a href="http://purl.org/dc/terms/BibliographicResource">BibliographicResource</a>) of </li>
<li>FRBR (<a href="http://purl.org/vocab/frbr/core#term-Work">Work</a>, <a href="http://purl.org/vocab/frbr/core#term-Expression">Expression</a>, <a href="http://purl.org/vocab/frbr/core#term-Manifestation">Manifestation</a> of <a href="http://purl.org/vocab/frbr/core#term-Item">Item</a>)</li>
</ul>
</div>

### Eigenschappen

| Conceptueel element                   | Taalbinding in RDF                                                                  |
| ------------------------------------- | ----------------------------------------------------------------------------------- |
| [=naam=]                              | [rdfs:label](http://www.w3.org/2000/01/rdf-schema#label)                            |
| [=heeft topbegrip=]                   | [skos:hasTopConcept](http://www.w3.org/2004/02/skos/core#hasTopConcept)             |
| [=voorkeursterm=]                     | [skos:prefLabel](http://www.w3.org/2004/02/skos/core#prefLabel)                     |
| [=alternatieve term=]                 | [skos:altLabel](http://www.w3.org/2004/02/skos/core#altLabel)                       |
| [=zoekterm=]                          | [skos:hiddenLabel](http://www.w3.org/2004/02/skos/core#hiddenLabel)                 |
| [=code=]                              | [skos:notation](http://www.w3.org/2004/02/skos/core#notation)                       |
| [=in kader=]                          | [skos:inScheme](http://www.w3.org/2004/02/skos/core#inScheme)                       |
| [=is topbegrip van=]                  | [skos:topConceptOf](http://www.w3.org/2004/02/skos/core#topConceptOf)               |
| [=uitleg=]                            | [rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)                        |
| [=definitie=]                         | [skos:definition](http://www.w3.org/2004/02/skos/core#definition)                   |
| [=heeft bron=]                        | [dct:source](http://purl.org/dc/terms/source)                                       |
| [=heeft bovenliggend begrip=]         | [skos:broader](http://www.w3.org/2004/02/skos/core#broader)                         |
| [=heeft onderliggend begrip=]         | [skos:narrower](http://www.w3.org/2004/02/skos/core#narrower)                       |
| [=is gerelateerd aan=]                | [skos:related](http://www.w3.org/2004/02/skos/core#related)                         |
| [=wijzigingsnotitie=]                 | [skos:changeNote](http://www.w3.org/2004/02/skos/core#changeNote)                   |
| [=redactionele notitie=]              | [skos:editorialNote](http://www.w3.org/2004/02/skos/core#editorialNote)             |
| [=historie notitie=]                  | [skos:historyNote](http://www.w3.org/2004/02/skos/core#historyNote)                 |
| [=toelichting=]                       | [skos:scopeNote](http://www.w3.org/2004/02/skos/core#scopeNote)                     |
| [=voorbeeld=]                         | [skos:example](http://www.w3.org/2004/02/skos/core#example)                         |
| [=heeft overeenkomstig bovenliggend=] | [skos:broadMatch](http://www.w3.org/2004/02/skos/core#broadMatch)                   |
| [=heeft overeenkomstig onderliggend=] | [skos:narrowMatch](http://www.w3.org/2004/02/skos/core#narrowMatch)                 |
| [=is vrijwel overeenkomstig=]         | [skos:closeMatch](http://www.w3.org/2004/02/skos/core#closeMatch)                   |
| [=is exact overeenkomstig=]           | [skos:exactMatch](http://www.w3.org/2004/02/skos/core#exactMatch)                   |
| [=is overeenkomstig verwant=]         | [skos:relatedMatch](http://www.w3.org/2004/02/skos/core#relatedMatch)               |
| [=is specialisatie van=]              | [isothes:broaderGeneric](http://purl.org/iso25964/skos-thes#broaderGeneric)         |
| [=is generalisatie van=]              | [isothes:narrowerGeneric](http://purl.org/iso25964/skos-thes#narrowerGeneric)       |
| [=is onderdeel van=]                  | [isothes:broaderPartitive](http://purl.org/iso25964/skos-thes#broaderPartitive)     |
| [=omvat=]                             | [isothes:narrowerPartitive](http://purl.org/iso25964/skos-thes#narrowerPartitive)   |
| [=is exemplaar van=]                  | [isothes:broaderInstantial](http://purl.org/iso25964/skos-thes#broaderInstantial)   |
| [=is categorie van=]                  | [isothes:narrowerInstantial](http://purl.org/iso25964/skos-thes#narrowerInstantial) |
| [=bronverwijzing=]                    | [dct:bibliographicCitation](http://purl.org/dc/terms/bibliographicCitation)         |
| [=url=]                               | [foaf:page](http://xmlns.com/foaf/0.1/page)                                         |
| [=bevat=]                             | [skos:member](http://www.w3.org/2004/02/skos/core#member)                           |

# Specificatie

Met het conceptueel model en de taalbinding die daar aan toegevoegd is kunnen we een dataspecificatie opstellen. Deze wordt in dit hoofdstuk besproken. De specificatie is ook in SHACL beschreven en is [hier](https://raw.githubusercontent.com/pldn/nederlands-profiel-voor-stelselcatalogi/main/profiles/skos-ap-nl.ttl) beschikbaar. 

## Specificatie Begrippenkader

Een begrippenkader wordt gerepresenteerd als een `skos:ConceptScheme`. Deze typering is verplicht.

<!-- Voor het beschrijven van de metadata van een begrippenkader sluiten we aan op metadatastandaarden zoals Dublin Core (dcterms), de Provenance Ontologie (Prov-O) en ADMS/DCAT. We zien een begrippenkader als een "semantic asset". Dit komt overeen met een adms:Asset. Aangezien adms:Asset een specialisatie is van een dcat:Dataset kunnen we op deze wijze goed aansluiten op catalogi die DCAT als uitgangspunt nemen, zoals [data.overheid.nl](data.overheid.nl) -->

<!-- > In ons profiel gebruiken we term "begrippenkader" met de taalbinding naar zowel skos:ConceptScheme als adms:Asset. We stellen daarmee dat een begrippenkader daadwerkelijk een beheerde asset is, maar ook gezien kan worden als een skos:ConceptScheme. De term "begrippenstelsel" hanteren we alleen in de betekenis van een "stelsel van begrippen", ongeacht of de beschrijvingen van deze begrippen als één geheel worden beheerd. Zo kun je dus spreken over het "stelsel van alle begrippen van alle (10) basisregistraties", die beheerd worden in (10) afzonderlijke begrippenkaders. -->

| Conceptueel element | Eigenschap                                                              | Kardinaliteit | Type                                                                    |
| ------------------- | ----------------------------------------------------------------------- | ------------- | ----------------------------------------------------------------------- |
| [=naam=]            | [dct:title](http://purl.org/dc/terms/title)                             | 1..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=uitleg=]          | [rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)            | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=heeft topbegrip=] | [skos:hasTopConcept](http://www.w3.org/2004/02/skos/core#hasTopConcept) | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |

## Specificatie Begrip

Een begrip wordt gerepresenteerd als een `skos:Concept`. Deze typering is verplicht.

| Conceptueel element                   | Eigenschap                                                                          | Kardinaliteit | Type                                                                    |
| ------------------------------------- | ----------------------------------------------------------------------------------- | ------------- | ----------------------------------------------------------------------- |
| [=voorkeursterm=]                     | [skos:prefLabel](http://www.w3.org/2004/02/skos/core#prefLabel)                     | 1..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=alternatieve term=]                 | [skos:altLabel](http://www.w3.org/2004/02/skos/core#altLabel)                       | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=zoekterm=]                          | [skos:hiddenLabel](http://www.w3.org/2004/02/skos/core#hiddenLabel)                 | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=code=]                              | [skos:notation](http://www.w3.org/2004/02/skos/core#notation)                       | 0..*          | [sh:Literal](http://www.w3.org/ns/shacl#Literal)                        |
| [=in kader=]                          | [skos:inScheme](http://www.w3.org/2004/02/skos/core#inScheme)                       | 1..*          | [skos:ConceptScheme](http://www.w3.org/2004/02/skos/core#ConceptScheme) |
| [=is topbegrip van=]                  | [skos:topConceptOf](http://www.w3.org/2004/02/skos/core#topConceptOf)               | 0..*          | [skos:ConceptScheme](http://www.w3.org/2004/02/skos/core#ConceptScheme) |
| [=uitleg=]                            | [rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)                        | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=definitie=]                         | [skos:definition](http://www.w3.org/2004/02/skos/core#definition)                   | 1..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=heeft bron=]                        | [dct:source](http://purl.org/dc/terms/source)                                       | 0..*          | [foaf:Document](http://xmlns.com/foaf/0.1/Document)                     |
| [=heeft bovenliggend begrip=]         | [skos:broader](http://www.w3.org/2004/02/skos/core#broader)                         | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=heeft onderliggend begrip=]         | [skos:narrower](http://www.w3.org/2004/02/skos/core#narrower)                       | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is gerelateerd aan=]                | [skos:related](http://www.w3.org/2004/02/skos/core#related)                         | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=wijzigingsnotitie=]                 | [skos:changeNote](http://www.w3.org/2004/02/skos/core#changeNote)                   | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=redactionele notitie=]              | [skos:editorialNote](http://www.w3.org/2004/02/skos/core#editorialNote)             | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=historie notitie=]                  | [skos:historyNote](http://www.w3.org/2004/02/skos/core#historyNote)                 | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=toelichting=]                       | [skos:scopeNote](http://www.w3.org/2004/02/skos/core#scopeNote)                     | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=voorbeeld=]                         | [skos:example](http://www.w3.org/2004/02/skos/core#example)                         | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=heeft overeenkomstig bovenliggend=] | [skos:broadMatch](http://www.w3.org/2004/02/skos/core#broadMatch)                   | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=heeft overeenkomstig onderliggend=] | [skos:narrowMatch](http://www.w3.org/2004/02/skos/core#narrowMatch)                 | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is vrijwel overeenkomstig=]         | [skos:closeMatch](http://www.w3.org/2004/02/skos/core#closeMatch)                   | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is exact overeenkomstig=]           | [skos:exactMatch](http://www.w3.org/2004/02/skos/core#exactMatch)                   | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is overeenkomstig verwant=]         | [skos:relatedMatch](http://www.w3.org/2004/02/skos/core#relatedMatch)               | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is specialisatie van=]              | [isothes:broaderGeneric](http://purl.org/iso25964/skos-thes#broaderGeneric)         | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is generalisatie van=]              | [isothes:narrowerGeneric](http://purl.org/iso25964/skos-thes#narrowerGeneric)       | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is onderdeel van=]                  | [isothes:broaderPartitive](http://purl.org/iso25964/skos-thes#broaderPartitive)     | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=omvat=]                             | [isothes:narrowerPartitive](http://purl.org/iso25964/skos-thes#narrowerPartitive)   | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is exemplaar van=]                  | [isothes:broaderInstantial](http://purl.org/iso25964/skos-thes#broaderInstantial)   | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=is categorie van=]                  | [isothes:narrowerInstantial](http://purl.org/iso25964/skos-thes#narrowerInstantial) | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)             |
| [=naam=]                              | [rdfs:label](http://www.w3.org/2000/01/rdf-schema#label)                            | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |

## Specificatie Brondocument

Een Brondocument wordt gerepresenteerd als een `foaf:Document`. Deze typering wordt aangeraden.

| Conceptueel element | Eigenschap                                                                  | Kardinaliteit | Type                                                                    |
| ------------------- | --------------------------------------------------------------------------- | ------------- | ----------------------------------------------------------------------- |
| [=naam=]            | [dct:title](http://purl.org/dc/terms/title)                                 | 1..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=uitleg=]          | [rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)                | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) |
| [=url=]             | [foaf:page](http://xmlns.com/foaf/0.1/page)                                 | 0..*          | [sh:IRI](http://www.w3.org/ns/shacl#IRI)                                |
| [=bronverwijzing=]  | [dct:bibliographicCitation](http://purl.org/dc/terms/bibliographicCitation) | 0..*          | [xsd:string](http://www.w3.org/2001/XMLSchema#string)                   |

## Specificatie Collectie

Een collectie wordt gerepresenteerd als een `skos:Collection`. Deze typering is verplicht.

| Conceptueel element | Eigenschap                                                      | Kardinaliteit | Type                                                                                                                             |
| ------------------- | --------------------------------------------------------------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| [=naam=]            | [skos:prefLabel](http://www.w3.org/2004/02/skos/core#prefLabel) | 1..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString)                                                          |
| [=uitleg=]          | [rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)    | 0..*          | [rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString)                                                          |
| [=bevat=]           | [skos:member](http://www.w3.org/2004/02/skos/core#member)       | 0..*          | [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept) OR [skos:Collection](http://www.w3.org/2004/02/skos/core#Collection) |
 
