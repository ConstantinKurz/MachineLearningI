#Blatt 10
#10.1

Im allgemeinen kann man sagen, dass GD Methods, die nicht die Fähigkeit haben ihre Learning-Rate anzupassen, weitaus anfälliger sind für Verschiebungen der Anfangsposition.
Das ist eigentlich nur logisch, da eine gleichbleibende Learningrate bei unterschiedlichen Anfangsbedingungen leicht zu einem stark beeinflussten Endergebnis führt.
Während Algorithmen, die die veränderte Position mit der Learning-Rate abfangen können hier besser performen.


#10.3

Im Fall von Momentum führt gamma = 0 also keine Reibung auf Vanilla GD.

m2 = g^2
m1 = 1
beta_1 = 0
beta_2 = gamma = 0

FÜr die Anwendung dieser Methoden bedeutet dass, das man im Prinzip RMSProp und Vanilla nicht zwingen implementieren muss, sonder auf Adam/Momentum zurückgreifen kann mit den oben genannten Parametern.
Auch kann ich mir vorstellen, dass man beide Methoden kombiniert. 
Also bei nicht allzu Komplexen Fragestellungne z.b. auf Vanilla GD zurückgreift, um dann in Fällen geringer Steigung auf Momentum umzusteigen.
Bei Momentum muss zusätzlich v berechnet werden.
Ich kann mir gut vorstellen, dass das bei großen Datensätzen erhebliche Rechenleistung kostet und das oben vorgeschlagene Vorgehen so performance einspart.

