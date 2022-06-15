### How to compile and run it?

In Terminal

Compile:
```
>>> ant
```

Run:
```
>>> java -cp ExtractGraph.jar -Xmx1g iways.map.PreProcessingMap melb.osm
```

Clean:
```
>>> ant clean
```

### What are the meanings of each column in output files?

NOTICE: The 1., 2., 3. means the row number in the file.

In edges.txt

1.   [the number of vertices]
2.   [the number of edges]
3.   [ID of edge] [ID of start node] [ID of end node] [distance(meters)]
4.   ...

In vertex.txt

1.   [the number of vertices]
2.   [ID of vertex] [ID in OSM file] [Longitude] [Latitude]
3.   ...

In streets.txt (for some my own reason, I hope to combine 'edges.txt' and 
'vertext.txt' into one file)
    
1.   [the number of edges]
2.   [ID of edge] [ID of start node] [Longitude of start node] [Latitude of
start node] [ID of end node] [Longitude of end node] [Latitude of end node]
[distance(meters)] [type of this road] [angle]
3.   ...

Hengfeng Li

Jun 14, 2013

### Anmerkungen Luis

Der osm-parser wird genutzt, um Karten im osm-Format, in streets.txt, edges.txt und vertex.txt umzuwandeln. Diese stellen zusammen mit den GPS-Logs die Ausgangsdaten für das map-matching dar.
Theoretisch existiert ein jar, welches ausgeführt werden kann. Da ich es nicht zum Laufen bekommen habe, beinhalten PreProcessingMap, sowie PreProcessingMapMammut eine main-Methode und können so ausgeführt werden.
Die Umwandlung sehr großer Map-Ausschnitte benötigt viel Arbeitsspeicher, weshalb diese auf einem leistungsstarken Rechner durchgeführt werden sollte.

