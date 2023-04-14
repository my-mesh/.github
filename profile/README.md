# Projektidee
Das Projekt soll die ersten Schritte der Vernetzung von Eingebetten Systemen erleichtern. Hierfür besteht das System aus einer Box welche sich um die Kommunikation, Speichern und die Darstellung der Daten kümmert.

# Projektaufbau
### Funk System
Das Funk System ermöglicht die Kommunikation zwischen Sensoren und dem Raspberry Pi. Hierbei benutzen wir ein NRF24 Funksystem mit einem Mesh Layer. Jede Node im System erhält hierbei eine eindeutige NodeID zugewiesen mit welcher die Kommunikation zwischen den Nodes ermöglicht wird.

### Ardunio
Der Ardunio stellt zusammen mit einem oder mehreren angeschlossenen Sensoren eine Node im Mesh System dar. Die Daten der Sensoren werden im Arduino verarbeitet und über das Funk System an den Raspberry Pi gesendet.

### Raspberry Pi
Der Raspberry Pi fungiert als Mesh Master welcher die gesamte Funkkommunikation des Mesh Systems orchestriert und stellt die Sicherung und Darstellung der Empfangenen Daten bereit.

# Projektaufteilung
- [Server](https://github.com/my-mesh/server)
- [Sensoren](https://github.com/my-mesh/sensor)
- [Poster](https://github.com/my-mesh/poster)
- [Bilder](https://github.com/my-mesh/pictures)
