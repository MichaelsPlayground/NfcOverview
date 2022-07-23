# NFC Generelle Übersicht

Near Field Communication (NFC)

Die "Near Field Communication" (NFC) (oder Nah-Distanz Kommunikation)
ist neben dem Telefonnetz, dem Internetzugang via WLAN/Wifi oder der
Bluetooth-Technik ein weiterer Datenübertragungskanal, der eine
Funkübertragung nutzt. Im Gegensatz zu den vorgenannten Techniken ist
die Übertragungs-Entfernung aber auf wenige Zentimeter beschränkt.

Die für NFC notwendige Antenne (Sender und Empfänger) ist je nach
Smartphone an unterschiedlichen Stellen, aber meistens auf der Rückseite
des Handy, angebracht. Hier hilft ein Blick in die Bedienungsanleitung
oder ein ausprobieren.

Zur erfolgreichen Nutzung von NFC ist es zwingend notwendig, diese
Übertragung im Smartphone auch zu aktivieren (mehr dazu später).

Neben den hier vorgestellten eigenen Apps empfehle ich Euch dringend,
die 3 nachstehenden Apps aus dem Playstore zu laden, denn sie können
Euch begleitend viele Informationen über einen sogenannten "NFC-Tag"
(oder kurz "Tag" gennt) geben:

- TagInfo (ich nutze Version 4.25.4):
- NFC TagInfo (Version ):
- NFC Tools (Version 8.6.1):

Als Letztes benötigt Ihr noch frei beschreibbare Tags - ich nutze für
meine Apps den Typ NXP NTag216 - ein Tag kostet im Zehnerpack rund 1
Euro pro Stück und bietet einen Speicher von rund 800 Bytes.

Die App "NFC EMV-Karten" ### ist in der Lage, Kredit- und Girokarten
auszulesen, hierfür benötigt Ihr entsprechende Karten mit NFC-Funktion
(erkennbar am Funkzeichen auf der Karte).

Die "NFC Passport Reader" App ist in der Lage, die auf dem NFC-Chip
eines deutschen Passes gespeicherten Daten wie Vor- und Nachname,
Geburts- und Ablaufdatum,  Geschlecht und das biometrische Passbild
auszulesen. Dieses funktioniert aber nur mit einem Reisepass und nicht
mit dem Personlausweis.

Der Zugriff auf den NFC-Tag geschieht über 4 verschiedene Technologien:

- 1) IsoDeep: Der Zugriff erfolgt über teilweise sehr komplexe
     Kommandos, welche individuell für jede Karte sein können (Beispiel:
     auslesen der Daten aus einer Kreditkarte). Das IsoDeep Protokoll ist
     mittels Android-API verfügbar.

- 2) NfcA: Der Lese- und Schreibzugriff erfolgt über sogenannte Seiten
     ("Pages"). Tag-Typ individuell können bestimmte Seiten des Tags z.B. für
     den Passwortschutz oder einen Zugriffszähler reserviert sein. Das NfcA
     Protokoll ist mittels Android-API verfügbar.

- 3) NfcB: Da mir keine NFC-Tags vorliegen, welche das NfcB Protokoll
     unterstützen, kann ich keine weiteren Informationen dazu geben. Das NfcB
     Protokoll ist mittels Android-API verfügbar.

- 4) NDEF: Das NDEF-Protokoll speichert Daten in sogenannten
     NDEF-Nachrichten, welche in einer speziellen Struktur auf dem Tag
     gespeichert werden. Es handelt sich dabei um die "Tag-Length-Value"
     ("TLV") Struktur. Da einige "Tag"-Werte genormt sind, kann ein NFC-Leser
     die Daten interpretieren. Beispielsweise kann in der TLV-Struktur eine
     Internetseite ("URL" gespeichert sein und das Android Smartphone öffnet
     zuerst den Standard-Browser und ruft dann die URL auf. Das NDEF
     Protokoll ist mittels Android- und iPhone-API verfügbar.