# rpi-bt-door
A Python Program that scans BT devices and opens a door per GPIO motor. Additionally a webinterface to view logs.

Zugangsdaten: bluedoor, bluedoor

## Übersicht der Schnittstellen:

- SQLite-Datenbank:
  Die zentrale Schnittstelle zwischen den verschiedenen Programmen. Sie dient als Speicher für Events, die sowohl von der Hardware-Steuerung (Tür-Controller) als auch von der Flask-Webapp genutzt werden.

- Bluetooth-Geräteerkennung:
  Diese Schnittstelle wird in deinem Python-Programm verwendet, um Geräte in Reichweite zu erkennen. Sie interagiert nicht direkt mit der Datenbank, sondern entscheidet über Aktionen (Tür öffnen/schließen).

- GPIO (Servo-Motor):
  Die GPIO-Schnittstelle des Raspberry Pi wird verwendet, um den Servo-Motor (und damit die Tür) zu steuern.

- HTTP/Flask-Webinterface:
  Die Flask-Webapp stellt die Events in der Datenbank grafisch dar und fungiert als Benutzeroberfläche.

  
