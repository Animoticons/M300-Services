M300
====

## Git

#### Befehle

| Befehl                       | Effekt                         |
| ---------------------------- |:------------------------------:|
| git add *Pfad* |: Fügt die Datei dem Index hinzu |
| git add -A | Fügt alle Dateien im Verzeichnis dem Index hinzu |
| git status   | Zeigt Unterschiede zwischen dem Index und dem aktuellen HEAD commit |
| Git commit -m "comment"   |: Fügt die Änderungen dem Repository hinzu |
| Git push  | Lädt die Änderungen beim Repository hoch  |
|  git pull  | Lädt das angegebene Repository herunter |
|    | |
|    | |
|    | |


## Vagrant

#### Übersicht

Vagrant ermöglicht es, sehr schnell virtuelle Maschinen auf Basis einer Datei (vagrantfile) zu erstellen. Im vagrantfile werden die Einstellungen für die Virtuelle Maschine in maschienenlesbarem Text hinterlegt.


#### Befehle

| Befehl                       | Effekt                         |
| ---------------------------- |:------------------------------:|
| vagrant init | Initialisiert im aktuellen Verzeichnis eine Vagrant-Umgebung und erstellt, falls nicht vorhanden, ein Vagrantfile |
| vagrant up | Erzeugt und Konfiguriert eine neue Virtuelle Maschine, basierend auf dem Vagrantfile |
| vagrant ssh | Baut eine SSH-Verbindung zur gewünschten VM auf |
| vagrant status | Zeigt den aktuellen Status der VM an |
| vagrant port | Zeigt die Weitergeleiteten Ports der VM an |
| vagrant halt | Stoppt die laufende Virtuelle Maschine |
| vagrant destroy | Stoppt die Virtuelle Maschine und zerstört sie. |
| vagrant box add *NAME* | Lädt die Box herunter, welche dann mit vagrant init *NAME* und vagrant up gestartet werden kann. |
|  |  |
|  |  |