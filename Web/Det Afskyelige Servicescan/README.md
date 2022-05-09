# Det Afskyelige Servicescan
### Description
>Folk har flere gange rapporteret om en mystisk host på netværket. Konkret evidens for, hvad fænomenet drejer sig om udløser en klækkelig dusør fra os. Dog har alle tilsendte videoer indtil videre været i lav opløsning, en anelse turbulente og 100% fake. Vi køber i hvert fald ikke præmissen, at en netværkshost, som nok ikke engang er fugtsikker, kan vade rundt i de danske skovbryn iklædt gorillakostume.
>
>Vi har imidlertid selv fundet nogle enorme fodspor, som kunne være værd at følge, fra hosten med domænet `abominable.hkn`. Din opgave er at afsløre _navnet_ og _versionsnummeret_ på den sagnomspundne service, som skulle køre på hosten - måske en dinosaur eller et manglende led?
>
>Hvis servicenavnet fx er `Nessie`, og versionsnummeret er `12.34.5v67890`, så er flaget `DDC{Nessie-12.34.5v67890}`. God jagt!

## Løsning
Da vi leder efter navnet og versionsnummeret på en service tænkte jeg at `Nmap` ville være det perfekte værktøj til dette.

Vi kan starte et Nmap scan ved bare at skrive følgende kommando:
>nmap abominable.hkn

Men eftersom at vi skal bruge servicenavnet og versionsnummeret bliver vi nødt til at køre den med parameteret `-sV` .

Vi kører derfor kommandoen:
>nmap abominable.hkn -sV

Her får vi følgende output:
>Starting Nmap 7.92 ( https://nmap.org ) at 2022-05-09 03:45 EDT
Nmap scan report for abominable.hkn (34.25.49.190)
Host is up (0.023s latency).
Not shown: 999 closed tcp ports (conn-refused)
PORT      STATE SERVICE VERSION
31337/tcp open  http    Jetty 9.4.45.v20220203
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9.44 seconds

Og der har vi alt den information vi skal bruge! Jetty 9.4.45.v20220203
Det giver os flaget:
>DDC{Jetty-9.4.45.v20220203}