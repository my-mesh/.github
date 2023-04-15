# Projektidee
Das Projekt soll die ersten Schritte der Vernetzung von Eingebetten Systemen erleichtern. Hierfür besteht das System aus einer Box welche sich um die Kommunikation, Speichern und die Darstellung der Daten kümmert.

# Projektaufteilung
- [Server](https://github.com/my-mesh/server)
- [Sensoren](https://github.com/my-mesh/sensor)
- [Poster](https://github.com/my-mesh/poster)
- [Bilder](https://github.com/my-mesh/pictures)

# Geräteliste
- Raspberry Pi
  - NRF24 Chips
  - GC9A01 Bildschirm
  - Neopixel Ring
- Arduino Nano
  - NRF24 Chips
  - Sensoren

# Raspberry Pi
Über den Raspberry Pi läuft sowohl der Webserver, Bildschirm, LED-Ring und der Mesh Master. Der Webserver und Mesh Master werden jeweils als eigenständige System Service automatisch beim hochfahren gestartet.

Bildschirm:
VCC	3.3V	1
GND	GND	6
DIN	10 (spi0 MOSI)	19
CLK	11 (spi0 SCLK)	23
CS	8 (spi0 CE0)	24
DC	25	22
RST	27	13
BL	18 (pcm clock)	12

Mesh:
VCC 3.3V 17
GND GND 39
CE CE 15
CSN CSN 11
SCK SCK 40
MOSI MOSI 38
MISO MISO 35

Neopixel:
VCC 5V 2
GND GND 14
GPIO12 32
