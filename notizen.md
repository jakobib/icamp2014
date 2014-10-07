Impulsreferat: Linked Open Data in Bibliotheken, Archiven und Museen 

*Was bedeutet “linked”? Warum sollten Daten möglichst viele explizite Verknüpfungen enthalten? Wie lassen sich solche Verknüpfungen durch Linked Open Data ausdrücken? Welche Schwierigkeiten und Alternativen existieren? Was können wir tun, um verknüpfte Daten sinnvoll zu nutzen und nutzbar zu machen?*

09:45-10:15 (danach zweites Impulsreferat)

Mögliche Fragen:

* Linked vs. nicht linked data
* Potential für Bibliotheken/Archive/Museen
* Wie wird sich katalogisierung in Zukunft mit Hilfe von LOD verändern?

----
TODO: für jeden Punkt ein Beispiel!

## Warum Links?

* Was ist ein Link?
    * Beispiele von (impliziten) Links
        * Bild mit Allegorie/Anspielung/verstecktem Zitat
        * Verwandtschaftsbeziehung
        * Verschlagwortung
        * Zitat
        * Zitation (in verschiedenen Formen): konkreter Link,
          allerdings schwierig maschinell zu verarbeiten
            * Siehe TBL 1992: directly follow hyperlinks
            * Zitation mit Identifier

* Warum sind Links sinnvoll?
    * Verbindung herstellen
    * Findbarkeit
    * Ein Link ist immer mehr **Information** als kein Link

## Was sind Links?

* Links anbringen
    * von X nach Y
    * Weitere Eigenschaften
        * Typ (RDF: Property)
        * Herkunft, Alter, Gültigkeit... (Provenienz)
        * Links mit mehr als zwei Enden

* Woraus besteht ein Link?
    * Ursprung, Ziel, Verbindung
        * Drei *unterschiedliche* Entitäten:
            1. es gibt etwas ("Ursprung")
            2. es gibt ein zweites ("Ziel")
            3. es gibt etwas drittes ("Verbindung") das mit 
               beiden zusammen hängt
    * Maschinell verarbeitbar und eindeutig mittels Identifiern
    * Verbindung kann wieder ein etwas sein (endlose treppe!)
    * Achtung: Verbindung ist nicht RDF-Property!

## Linked Open Data

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


