
# AskSin Analyzer XS Board

- Ein Board für Christophs [AskSin Analyzer XS](https://homematic-forum.de/forum/viewtopic.php?f=76&t=56395), die Minimalversion des "großen" [AskSinAnalyzer](https://homematic-forum.de/forum/viewtopic.php?f=76&t=51161) - ohne ESP32 und ohne großes Display - zum Betrieb über den USB Port eines Computers.

- Außerdem lässt sich damit die Idee der [868 MHz Wünschelrute](https://homematic-forum.de/forum/viewtopic.php?f=76&t=56881) zur Suche nach einem [Babbling Idiot](https://github.com/TomMajor/SmartHome/tree/master/Info/Babbling%20Idiot%20Protection) (BI) Dauersender realisieren.<br>
Dabei wird das Gerät von einer USB-Powerbank versorgt und man kann sich damit auf Wanderung im Haus oder Garten begeben um durch die Anzeige der Signalstärke auf einem kleinen OLED-Display das fehlerhaft sendende Gerät - den BI - zu identifizieren.

- Das OLED und die Wünschelruten Funktion sind optional in der Bestückung.<br>
Außerdem ist für diesen Anwendungsfall eine kleine und individuell konfigurierbare Lastschaltung bestückbar, so dass die Powerbank nicht abschaltet.

- ich habe versucht durch Nutzung von fertig bestückte Boards wie dem Arduino Nano und dem Levelshifter-Board den nötigen Lötaufwand gering zu halten, bei gleichzeitig möglichst sauberen Schaltungsdesign mit 5V/3,3V Levelshiftern.

- Der Arduino Nano sitzt mit ein paar Pins einer Stiftleiste über dem CC1101 und dem Levelshifter-Board, ähnlich wie bei der [tmStamp](https://github.com/TomMajor/SmartHome/tree/master/PCB/tmStamp).


## Bilder

![pic](Images/AnalyzerXS_pcb1.png)

![pic](Images/AnalyzerXS_pcb2.png)

![pic](Images/AnalyzerXS_pcb3.png)

![pic](Images/BI-Wuenschelrute.jpg)

![pic](Images/oled-module.jpg)


## Schaltplan

[:arrow_right: AskSin Analyzer XS 1.01](https://github.com/TomMajor/SmartHome/tree/master/PCB/AskSin-Analyzer-XS/Files/Analyzer_XS_101.pdf)


## Platine

[:arrow_right: PCB Gerber](Gerber)

**WIP**


## Aufbau / Stückliste

| Anzahl    | Name      | Wert              | Gehäuse       | Bemerkungen |
|---|---|---|---|---|
| - | R1                | (10k)             | (0805)        | nicht bestücken, das Levelshifter-Board hat bereits pull-ups an jedem Kanal |
| 1 | R2                | 1k                | 0805          | |
| 2 | R3,R4             | 3,3k              | 0805          | |
| 4 | R5-R8             | 10k               | 0805          | |
| 1 | IC4               | 4-fach I2C Levelshifter | 2x6     | [Beispiel bei ebay](https://www.ebay.de/itm/162352091615) |
| 2 | R9,R10            | tbd               | 0805          | Optional: Lastschaltung für USB-Powerbank |
| 1 | R11               | 4,7k              | 0805          | Optional: Lastschaltung für USB-Powerbank |

**WIP**


## Links

[HomeMatic Forum: AskSin Analyzer XS - Der Analyzer als Desktop-App ohne ESP](https://homematic-forum.de/forum/viewtopic.php?f=76&t=56395)

[HomeMatic Forum: AskSinAnalyzer-Sniffer mit Display (BI-Wünschelrute)](https://homematic-forum.de/forum/viewtopic.php?f=76&t=56881)


## Lizenz

**Creative Commons BY-NC-SA**<br>
Give Credit, NonCommercial, ShareAlike

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
