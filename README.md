# Audi ABH 4.2 V8 – ECUMaster EMU Black First-Start Mapping

Basis-Mapping (First Start) für den **Audi 4.2L V8 (Motorcode ABH)** auf einer **ECUMaster EMU Black**. Das Projekt enthält die Grundkonfiguration für Trigger, Zündung und Einspritzung, mit der der Motor erstmalig gestartet und im Leerlauf betrieben werden kann. Es ist **kein** fertig abgestimmtes Mapping für Last- oder Fahrbetrieb.

## Dateien

| Datei | Beschreibung |
|---|---|
| `V2_Audi_ABH_42_V8_FirstStart.emub` | EMU Black Projektdatei (erstellt mit EMU Black Software, Projektversion 2.175) |

Die Datei wird mit dem **EMU Black Client** von ECUMaster geöffnet (Datei → Projekt öffnen) und kann von dort auf das Steuergerät geladen werden.

## Motor

| Parameter | Wert |
|---|---|
| Motor | Audi ABH, 4.2L V8 (32V) |
| Hubraum | 4172 cm³ |
| Zylinder | 8 |
| Aufladung | Saugmotor (Boost Control deaktiviert) |

## Grundkonfiguration (Auszug)

| Bereich | Einstellung |
|---|---|
| Primärtrigger | 60 Zähne Kurbelwelle, VR-Sensor, Triggerwinkel 45° |
| Sekundärtrigger | Nockenwellensignal (Cam Sync) für sequentielle Einspritzung |
| Drehzahlbegrenzer | 6500 U/min |
| Startdrehzahl-Schwelle | 400 U/min |
| Zündwinkel beim Start | 20° v. OT |
| MAP-Sensor | interner Sensor der EMU Black |
| Injektoren | 8× einzeln angesteuert (sequentiell), Öffnungszeit- und Dwell-Tabellen hinterlegt |

## Status

-  Erststart-Konfiguration (Trigger-Setup verifiziert, Motor startet)
-  Leerlauf, Gemisch und Zündkennfeld nur grob bedatet
-  Kein Last-/Teillast-Tuning, keine Klopfregelung abgestimmt

## Verwendung

1. EMU Black Client installieren (Download bei [ECUMaster](https://www.ecumaster.com)).
2. Projektdatei öffnen und **alle Einstellungen mit der eigenen Hardware abgleichen** (Sensoren, Injektoren, Zündspulen, Verkabelung).
3. Vor dem ersten Start: Triggerlog prüfen, Drosselklappe kalibrieren (TPS Min/Max), Sensorwerte plausibilisieren.
4. Erststart nur mit Breitband-Lambda-Überwachung durchführen.

## Haftungsausschluss

Dieses Mapping wird ohne jede Gewährleistung bereitgestellt. Die Verwendung erfolgt auf eigene Gefahr. Falsche Einstellungen können zu Motorschäden führen. Der Betrieb eines frei programmierbaren Steuergeräts ist auf öffentlichen Straßen in Deutschland in der Regel nicht zulässig – Nutzung nur für Motorsport bzw. auf abgesperrtem Gelände.
