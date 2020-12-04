# Lösung

Zu 1.)

1. Das Verzeichnis /mnt/data MUSS leer sein. Ggf. mit ```sudo rm``` leeren.
2. Docker Hub im Browser öffnen und nach postgres suchen
3. Unter "Where to Store Data" ist zu sehen, dass das Datenverzeichnis im Container unter /var/lib/postgresql/data gespeichert ist. Hierhin ist unser Mount zu leiten.
4. Persistent Volume (10Gi, RWO) in /mnt/data erstellen
5. Claim für 3Gi, RWO erstellen
6. Pod erstellen, dabei auf die Variablen auf der odoo-Seite im Docker-Hub achten und im Container Port 5432 veröffentlichen
7. Service erstellen. Port: 5432

Zu 2.)
1. Pod erstellen
2. Container-Port ist 8069
3. Variable für den PostgreSQL-Host beachten

