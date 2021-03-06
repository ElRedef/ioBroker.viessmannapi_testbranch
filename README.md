TESTBRANCH ONLY

PLEASE USE OFFICIAL REPO







![Logo](admin/viessmannapi.png)

# ioBroker.viessmannapi_testbranch

[![NPM version](https://img.shields.io/npm/v/iobroker.viessmannapi.svg)](https://www.npmjs.com/package/iobroker.viessmannapi)
[![Downloads](https://img.shields.io/npm/dm/iobroker.viessmannapi.svg)](https://www.npmjs.com/package/iobroker.viessmannapi)
![Number of Installations (latest)](https://iobroker.live/badges/viessmannapi-installed.svg)
![Number of Installations (stable)](https://iobroker.live/badges/viessmannapi-stable.svg)
[![Dependency Status](https://img.shields.io/david/TA2k/iobroker.viessmannapi.svg)](https://david-dm.org/TA2k/iobroker.viessmannapi)

[![NPM](https://nodei.co/npm/iobroker.viessmannapi.png?downloads=true)](https://nodei.co/npm/iobroker.viessmannapi/)

**Tests:** ![Test and Release](https://github.com/TA2k/ioBroker.viessmannapi/workflows/Test%20and%20Release/badge.svg)

## viessmannapi adapter for ioBroker

Adapter for Viessmannapi

Visit https://developer.viessmann.com/de/clients and create a new client.

Name: iobroker
deactivate Google reCAPTCHA
URI: http://localhost:4200/

Copy Client ID in the instance settings.

To change parameter set the state setValue
Example:

***viessmannapi.0.XXXXX.0.features.heating.dhw.temperature.main.commands.setTargetTemperature.setValue***

**Outdoor Temperature
viessmannapi.0.XXX.0.features.heating.sensors.temperature.outside.properties.value.value**

**Kompatibilitätsliste**:
**Regelungen für Wand- oder Kompaktgeräte**
Vitotronic 200, Typ HO1, HO1A, HO1B, HO1D, HO2B, HO2C
Vitotronic 200 RF, Typ HO1C, HO1E

**Regelungen für bodenstehende Heizkessel**
Vitotronic 200, Typ KO1B, KO2B, KW6, KW6A, KW6B, KW1, KW2, KW4, KW5
Vitotronic 300, Typ KW3

**Regelungen für Wärmepumpen und Hybridgeräte**
Vitotronic 200, Typ WO1A, WO1B, WO1C

**Regelungen für Festbrennstoffkessel**
Vitoligno 200-S mit Ecotronic (ab Softwarestand 2.03)
Vitoligno 250-S mit Ecotronic (ab Softwarestand 2.00)
Vitoligno 300-C mit Ecotronic (ab Softwarestand 2.12)
Vitoligno 300-P mit Vitotronic 200 FO1
Vitoligno 300-S mit Ecotronic (ab Softwarestand 2.04)

**Liste aller Datenpunkte:
https://developer.viessmann.com/de/doc/iot/data-points**

Beispiele:
```
Vorlauftemperatur: 
viessmannapi.0.XXXX.features.heating.circuits.0.sensors.temperature.supply.properties.value.value, 

Anzahl Zündungen:
viessmannapi.0.XXXXX.features.heating.burners.0.statistics.properties.starts.value

Betriebsstunden
viessmannapi.0.XXXXX.features.heating.burners.0.statistics.properties.hours.value

Kesseltemperatur
viessmannapi.0.XXXXX.features.heating.boiler.sensors.temperature.main.properties.unit.value

Kompressor aktiv:		viessmannapi.0.xxx.0.features.heating.compressors.0.properties.active.value
Heizkreispumpe aktiv:		viessmannapi.0.xxx.0.features.heating.circuits.1.circulation.pump.properties.status.value
Warmwasserbereitung:		viessmannapi.0.xxx.0.features.heating.dhw.charging.properties.active.value
Heizungsmodus:			viessmannapi.0.xxx.0.features.heating.circuits.1.operating.modes.active.properties.value.value
Heizprogramm:			viessmannapi.0.xxx.0.features.heating.circuits.1.operating.programs.active.properties.value.value
Temperatur Heizprogramm normal:	viessmannapi.0.xxx.0.features.heating.circuits.1.operating.programs.normal.properties.temperature.value
Temperatur Heizprogramm reduz.:	viessmannapi.0.xxx.0.features.heating.circuits.1.operating.programs.reduced.properties.temperature.value
Warmwasser Soll Temperatur:	viessmannapi.0.xxx.0.features.heating.dhw.temperature.properties.value.value
Warmwasser Ist Temperatur:	viessmannapi.0.xxx.0.features.heating.dhw.sensors.temperature.hotWaterStorage.properties.value.value
Temperatur Außensensor:		viessmannapi.0.xxx.0.features.heating.sensors.temperature.outside.properties.value.value
Statistik Kompressor Starts:	viessmannapi.0.xxx.0.features.heating.compressors.0.statistics.properties.starts.value
Statistik Kompressor Stunden:	viessmannapi.0.xxx.0.features.heating.compressors.0.statistics.properties.hours.value
 
 
Primärkreis Vorlauftemperatur:		viessmannapi.0.xxx.0.features.heating.primaryCircuit.sensors.temperature.supply.properties.value.value
Sekundärkreis Vorlauftemperatur:	viessmannapi.0.xxx.0.features.heating.secondaryCircuit.sensors.temperature.supply.properties.value.value
Sekundärkreis Rücklauftemperatur:	viessmannapi.0.xxx.0.features.heating.secondaryCircuit.sensors.temperature.return.properties.value.value
?					viessmannapi.0.xxx.0.features.heating.sensors.temperature.return.properties.value.value

```

## Changelog

### 2.0.0

-   (TA2k) initial release

## License

MIT License

Copyright (c) 2021 TA2k <tombox2020@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
