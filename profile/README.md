# Projektidee
Das Projekt soll die ersten Schritte der Vernetzung von Eingebetten Systemen erleichtern. Hierfür besteht das System aus einer Box welche sich um die Kommunikation, Speichern und die Darstellung der Daten kümmert.

# Projektaufteilung
- [Server](https://github.com/my-mesh/server)
- [Mesh](https://github.com/my-mesh/mesh)
- [Sensoren](https://github.com/my-mesh/sensor)
- [Poster](https://github.com/my-mesh/poster)
- [Bilder](https://github.com/my-mesh/pictures)

# Geräteliste
- [Raspberry Pi](#raspberry-pi)
  - [NRF24 Chip](#nrf24-chip)
  - [GC9A01 Bildschirm](#gc9a01-bildschirm)
  - [Neopixel Ring](#neopixel-ring)
- Arduino Nano
  - NRF24 Chips
  - Sensoren

# Raspberry Pi
Über den Raspberry Pi läuft sowohl der Webserver, Bildschirm, LED-Ring und der Mesh Master. Der Webserver und Mesh Master werden jeweils als eigenständige System Service hochgefahren.

## NRF24 Chip
Der NRF24 Chip ermöglicht die Kommunikation des Mesh Masters mit anderen Nodes im System.

<table>
    <tbody>
        <tr>
            <td>VCC</td><td>3.3V</td><td>17</td>
        </tr>
        <tr>
            <td>GND</td><td>GND</td><td>39</td>
        </tr>
        <tr>
            <td>CE</td><td>CE</td><td>15</td>
        </tr>
        <tr>
            <td>CSN</td><td>CSN</td><td>11</td>
        </tr>
        <tr>
            <td>SCK</td><td></td><td>40</td>
        </tr>
        <tr>
            <td>MOSI</td><td>25</td><td>38</td>
        </tr>
        <tr>
            <td>MISO</td><td>27</td><td>35</td>
        </tr>
    </tbody>
</table>

## GC9A01 Bildschirm
Der Bildschirm ist über SPI an den Raspberry Pi angeschlossen und spiegelt mithilfe des [Raspberry Pi Framebuffer Copy](https://github.com/tasanakorn/rpi-fbcp) den HDMI Output vom Raspberry Pi auf den Bildschirm. Dadurch kann das Interface als Unterseite auf dem Webserver gehostet werden und ermöglicht ein einfachs anpassen und austauschen der Dargestellten Seite.

<table>
    <tbody>
        <tr>
            <td>VCC</td><td>3.3V</td><td>1</td>
        </tr>
        <tr>
            <td>GND</td><td>GND</td><td>6</td>
        </tr>
        <tr>
            <td>DIN</td><td>10 (spi0 MOSI)</td><td>19</td>
        </tr>
        <tr>
            <td>CLK</td><td>11 (spi0 SCLK)</td><td>23</td>
        </tr>
        <tr>
            <td>CS</td><td>8 (spi0 CE0)</td><td>24</td>
        </tr>
        <tr>
            <td>DC</td><td>25</td><td>22</td>
        </tr>
        <tr>
            <td>RST</td><td>27</td><td>13</td>
        </tr>
        <tr>
            <td>BL</td><td>18 (pcm clock)</td><td>12</td>
        </tr>
    </tbody>
</table>

## Neopixel Ring
Der Neopixel Ring wird auch über den WebServer gesteuert

<table>
    <tbody>
        <tr>
            <td>VCC</td><td>5V</td><td>2</td>
        </tr>
        <tr>
            <td>GND</td><td>GND</td><td>14</td>
        </tr>
        <tr>
            <td>GPIO</td><td>GPIO</td><td>32</td>
        </tr>
    </tbody>
</table>
