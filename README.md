M300
====

## Git

#### Befehle

| Befehl                       | Effekt                         |
| ---------------------------- |:------------------------------:|
| git add *Pfad* | Fügt die Datei dem Index hinzu |
| git add -A | Fügt alle Dateien im Verzeichnis dem Index hinzu |
| git status   | Zeigt Unterschiede zwischen dem Index und dem aktuellen HEAD commit |
| Git commit -m "comment"   | Fügt die Änderungen dem Repository hinzu |
| Git push  | Lädt die Änderungen beim Repository hoch  |
|  git pull  | Lädt das angegebene Repository herunter |


## Vagrant

#### Übersicht

Vagrant ermöglicht es, sehr schnell virtuelle Maschinen auf Basis einer Datei (vagrantfile) zu erstellen. Im vagrantfile werden die Einstellungen für die Virtuelle Maschine in maschienenlesbarem Text hinterlegt.


#### Befehle

| Befehl                       | Effekt                         |
| ---------------------------- |:------------------------------:|
| vagrant init *NAME* | Initialisiert im aktuellen Verzeichnis eine Vagrant-Umgebung und erstellt, falls nicht vorhanden, ein Vagrantfile |
| vagrant up | Erzeugt und Konfiguriert eine neue Virtuelle Maschine, basierend auf dem Vagrantfile |
| vagrant ssh | Baut eine SSH-Verbindung zur gewünschten VM auf |
| vagrant status | Zeigt den aktuellen Status der VM an |
| vagrant port | Zeigt die Weitergeleiteten Ports der VM an |
| vagrant halt | Stoppt die laufende Virtuelle Maschine |
| vagrant destroy | Stoppt die Virtuelle Maschine und zerstört sie |
| vagrant box add *NAME* | Lädt die Box herunter, welche dann mit vagrant init *NAME* und vagrant up gestartet werden kann |

#### Vagrant Cloud

| Befehl                       | Effekt                         |
| ---------------------------- |:------------------------------:|
| vagrant cloud auth login | Login in vagrant cloud |
| vagrant cloud auth whoami | Zeigt den momentan eingeloggten Account an |
| vagrant cloud search *suchbegriff* | Suche in der Vagrant Cloud |
| vagrant box add *box name* | Download Box mit diesem Box Name |


## Vagrantfile

####Festlegen der Box, welche die Maschine nutzen soll:

`config.vm.box = "ubuntu/xenial64"`

####VM Name in VirtualBox festlegen:

`config.vm.provider "virtualbox" do |v|
  v.name = "VagrantLinuxVM" #VM Name setzen
end`

####Es besteht auch die Möglichkeit, Linux-Befehle nach der Installation automatisch ausführen zulassen. Dafür wird folgende Struktur verwendet:

`config.vm.provision "shell", inline: <<-SHELL
 *Befehle Hier*
SHELL`