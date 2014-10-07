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
* Hier nur **Daten** die mit anderen Daten zusammenhängen
* Linked Open Data

# Daten die mit anderen Daten zusammenhängen

* Verschiedene Daten beschreiben die gleiche Dinge

* Zum Beispiele die gleiche Person
    * Person als Autor in Katalogdatenbank
    * Museumsobjekte der Person im Bestandsverzeichnis
    * Wikipedia-Artikel über die Person
    * ...

# Old School Linked Data

* Normdaten
* Kontrollierete Vokabulare
* Identifier (z.B. RVK-Notation, Hausnummer, 

*Grundidee: Eindeutige Referenzierbarkeit*

"things, not strings"

# Beispiel

1. "Autor: Karl Marx"

2. "Autor:" <http://d-nb.info/gnd/118578545>

3. <http://purl.org/dc/terms/creator> ":"
   <http://d-nb.info/gnd/118578545>

# Links zwischen Daten

* Verschiedene Datensätze in verschiedenen Datenbanken\
  (z.B. Autor in Katalogdatenbank und in Wikipedia)
* Verschiedene Datensätze in einer Datenank\
  (z.B. Normdatensatz und Katalogisat)
* Verschiedene Teile eines Datensatzes\
  (z.B. Vorname und Nachname einer Person)

* In RDF kein wesentlicher Unterschied: 
  weil Tripel als kleinste Dateneinheit

* Sinn von *L*OD *Daten zusammenführen*

# Warum sind Links sinnvoll?

* Verbindung herstellen
* Findbarkeit

# Linked Open Data

Wie lassen sich solche Verknüpfungen durch Linked Open Data ausdrücken? 

* RDF, eine einheitliche Sprache für Links
    * URI
    * Triples (Ursprung, Linktyp, Ziel)
        * Achtung: Linktyp != Verbindung
        * Achtung: Ursprung kann auch identisch mit Ziel sein

* Linked Open Data
    * Massenweise Links in RDF
        * Bereitstellung von URIs (zum/vom Verknüpfen)
        * Bereitstellung von Verknüpfungen
    * Achtung: nicht alles was LOD ist, sind auch nützliche Links!
        Manchmal reicht auch eine einfache Liste (CSV-Datei, BEACON...)


# Linking Open Data cloud diagram

![](lod-cloud.png)

<!-- Welche Schwierigkeiten und Alternativen existieren? -->

<!-- Was können wir tun, um verknüpfte Daten sinnvoll zu nutzen und nutzbar zu
machen? -->

<!-- Potential für Bibliotheken/Archive/Museen -->

# Katalogisierung mit LOD

<!-- Wie wird sich katalogisierung in Zukunft mit Hilfe von LOD verändern? -->

Erstellung von Daten:

* Namen und andere Digitalisate
* Verknüpfungen

# Namen und andere Digitalisate

..hier Bild von Inschrift und Unicode-Transkription...

*Oft unnötige Arbeit, da schon vorhanden!*

# Verknüpfungen

...

# Vorteile

* Flexibler Zusammenführen
    Beispiel für Mehrwert durch Zusammenarbeit

# Zusammenfassung

* ...

# Quellen und Lizenz

* Linking Open Data cloud diagram 2014, by Max Schmachtenberg, Christian Bizer,
  Anja Jentzsch and Richard Cyganiak. http://lod-cloud.net/ 

![](cc-by-sa.png)

