---
title: Linked Open Data in Bibliotheken, Archiven & Museen
author: Jakob Voß
date: 2014-10-10
place: Infocamp, Chur
institute: Verbunzentrale des GBV (VZG)
...

---

# Im Wald

![](lod-cloud.png)

# Häh?

* Alles hängt irgendwie mit allem zusammen
* Hier: **Daten** die mit anderen Daten zusammenhängen
* Linked Open Data

# Daten die mit anderen Daten zusammenhängen

* Verschiedene Daten beschreiben die gleiche Dinge

* Zum Beispiele **die gleiche Person**
    * Person als Autor in Katalogdatenbank
    * Museumsobjekte der Person im Bestandsverzeichnis
    * Wikipedia-Artikel über die Person
    * ...

# Old School Linked Data: authority files

Normdaten
  : Personenverzeichnis, Klassifikation, Thesaurus...
Kontrollierte Vokabulare
  : statt Hymonyme und Synonyme
Identifier
  : Notation, ID-Nummer...

**Grundidee:** Eindeutige Referenzierbarkeit

> "things, not strings"

# *things, not strings* -- ein Beispiel

1. "Autor: Karl Marx"\
   "Autor: Karl Marx (Künstler)"

2. "Autor:" <http://d-nb.info/gnd/118578545>

3. Eigenschaft: <http://purl.org/dc/terms/creator>\
   Gegenstand: <http://d-nb.info/gnd/118578545>

$\Rightarrow$ Linked Open Data

# Linked Open Data

1. **Data**

    Daten in RDF
    
    HTTP-URIs als Identifier

2. **Open**

    abrufbar per HTTP-URIs

2. **Linked**

    mit Links zu anderen HTTP-URIs

# Beispiel: <http://d-nb.info/gnd/118578545>

![](gnd-beispiel.png)

# Beispiel: <http://d-nb.info/gnd/118578545>

```
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix gnd: <http://d-nb.info/standards/elementset/gnd#> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .

<http://d-nb.info/gnd/118578545>
  gnd:preferredNameForThePerson "Marx, Karl" ;
  gnd:professionOrOccupation
    <http://d-nb.info/gnd/4033423-5> ;
  foaf:page 
    <http://de.wikipedia.org/wiki/Karl_Marx_%28Maler%29> ;
  owl:sameAs <http://viaf.org/viaf/96119561> .

<http://d-nb.info/gnd/4033423-5>
  gnd:preferredNameForTheSubjectHeading "Künstler" .
```

# RDF in a Nutshell

* Alle Dinge werden mit einer URI identifiziert\
  (z.B. <http://d-nb.info/gnd/11857854>)
* Alle Daten bestehen aus einzelnen Aussagen (Triples)
    * Subjekt (immer eine URI)^[abgesehen von blank nodes]
    * Property (Eigenschaft identifiert durch eine URI)
    * Objekt (Zeichenkette oder URI)$^1$


# Ontologien

* Definition von Eigenschaften

* **Einheitliche** Eigenschaften

    * `gnd:preferredNameForThePerson`
    * `foaf:name` (<http://xmlns.com/foaf/0.1/name>)
    * `schema:name` (<http://schema.org/name>)
    * ...

* Katalogisierung mit RDA basiert auf einer RDF-Ontologie,
  andere Datenmodelle lassen sich auf Ontologien abbilden

* Ontologien sind mischbar


# Vorteile

* Einheitliches Datenformat
* Verfügbarkeit der Daten
* Flexibleres Zusammenführen und Ausschnitte bilden

$\Rightarrow$ Mehrwert durch *Zusammenarbeit*

# LOD macht keinen Sinn wenn...

* Niemand anderes die eigenen Daten nutzen soll
* Alle Daten selber erfasst und genutzt werden
* Anwendungsmöglichkeiten begrenzt sind 
* Alle unter sich bleiben wollen

$\Rightarrow$ Zusammenarbeit nicht gewünscht ist


# Linked Open Data in der Praxis

* Massenweise Links als RDF-Daten
    * Bereitstellung von URIs zum Verknüpfen
    * Bereitstellung von Verknüpfungen
        * Eigene URIs
        * Mit URIs anderer Datenbanken
        * In RDF das Gleiche
    * zum direkten Abruf und als Dumps
* Ggf. reichen auch andere Formate\
  (CSV-Datei, BEACON...)


# Linking Open Data cloud diagram

![](lod-cloud.png)


# Einige Beispiele

<!-- TODO: Potential für Bibliotheken/Archive/Museen -->

* Deutsche Nationalbibliothek
* Universität Münster
* Oslo Public Library
* ...


# Katalogisierung mit LOD

<!-- Wie wird sich katalogisierung in Zukunft mit Hilfe von LOD verändern? -->

Erstellung von Daten:

* Zeichenketten oder andere Digitalisate
* Verknüpfungen

# Zeichenketten oder andere Digitalisate

![](minnesang.png)

*Nur genau einmal notwendig, danach Verknüpfungen*

# Verknüpfungen

* Auswahl aus bereits vorhandenen URIs
* Mit geeigneten Hilsfmitteln 

![](suggest_wikipedia_en.png)

# Zusammenfassung

* Alles lässt sich mit allem verknüpfen, wenn URIs da sind
* Tripel als kleinste Dateneinheit, leichte Nachnutzung und Zusammenführung
* Bitte URIs und Ontologien weiterverwenden!

# Quellen, Hilsfmittel und Lizenz

* Linking Open Data cloud diagram 2014, by Max Schmachtenberg, Christian Bizer,
  Anja Jentzsch and Richard Cyganiak. http://lod-cloud.net/ 

* RDF per HTTP-URI abrufen
      * <http://www.easyrdf.org/converter>
      * `catmandu convert RDF --url http://d-nb.info/gnd/118578545 to YAML`

![](cc-by-sa.png)

