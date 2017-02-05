# Wie Funktioniert das Internet?

## Begriffe

| Was         | Beispiel      | Beschriebung                                                                                                                       |
|-------------|---------------|------------------------------------------------------------------------------------------------------------------------------------|
| Domain Name | `rosel.ch`      | Unter diesem Namen ist die Webseite verfügbar im Internet                                                                          |
| IP Adresse  | 80.74.152.191 | "Hausnummer" des Servers, auf dem die Webseite läuft. Ein Domain Name "zeigt" auf eine IP Adresse, also: `rosel.ch -> 80.74.152.191` |
| DNS Server  | Quickline     | "Adressbuch", ein bei dem beispielsweise der Internet Browser abfragen kann, unter welcher IP Adresse eine Webseite verfügbar ist. |
| Registrar   | switch.ch     | Hier "kauft" man Domain Namen wie `rosel.ch`.                                                                                   |
| Web Hoster  | Kreativ Media | Stellt einen Server zur Verfügung, wo man die Dateien einer Webseite hochladen kann.                                               |
## Webseiten aufschalten

Damit eine Webseite im Internet verfügbar ist müssen einige Voraussetzungen erfüllt seit:

* Es muss einen Domain Namen wie `rosel.ch` bei einem Registrar gekauft bzw gemietet haben.
* Die Webseite muss auf einen Webserver, der öffentlich zugänglich ist publiziert sein. Den Server kann ich selber installieren oder viel bequemer bei einem Webhoster mieten. Der Webserver hat eine Adresse in Form einer Nummer, die IP Adresse.
* Bei einem DNS Server muss ich eintragen lassen, dass die mein Domain Name auf die IP Adresse meines Webservers zeigt, ähnlich einem Eintrag ins Telefonbuch.

Ist all das erfüllt ist die Webseite im Internet erreichbar.

## Webseite aufrufen - wie passiert das?

```
+-----------+                       +------------+
| Röselchen |  -- sitzt am ... -->  | Computerli |
+-----------+                       +------------+
                                     |  ^   |  ^
                .--------------------`  |   |  |
                |                       |   |  |
                |    .------------------`   |  |
                |    |                      |  `---(4)-----.
               (1)   |                     (3)             |
                |    |                      |              |
                |   (2)                     |              |
                v    |                      v              |
          +------------+               +-----------------------+
          | DNS Server |               | Webserver beim Hoster |
          +------------+               |   IP: 80.74.152.191   |
                                       +-----------------------+
```

0. Rosel sitzt am Computer und gibt `rosel.ch` im Browser ein.
1. Der Browser erkundigt sich beim DNS Server, welche IP Adresse der Server wohl hat, auf welchem die Webseite `rosel.ch` läuft.
2. Der DNS Server läst verlauten, dass die Webseite `rosel.ch` auf dem Webserver mit der IP Adresse `80.74.152.191` zu finden ist.
3. Der Browser wendet sich nun an entsprechenden Webserver und fragt nach der Webseite.
4. Der Webserver schickt die HTML Dateien (sowie die Bilder, CSS Dateien usw.) an den Browser, welche dieser dann anzeigt.
