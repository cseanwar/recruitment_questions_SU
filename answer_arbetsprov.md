Linux
=====

GNU
---

### Vimsigt värre..

På hur många sätt är VIM överlägsen Emacs?
```
    * Vim is faster
    * Vim is pre-installed almost in every Linux distro
    * Vim is lighter than Emacs - uses less memory
    * Once a user becomes familiar with the Vim's editing modes and commands of Vim, it enables far greater productivity and efficiency.
```
### Insomnia

Hur gör du om du vill att din webbläsare ska stängas av på din
linuxdator för att du ska komma i säng klockan 03:00 varje dag?
```
    We can do it by set a cronjob. For exemple:
    crontab -e
    0 3 * * * killall <browser name>
```
### !telnet

Nämn minst ett sätt att logga in säkert på en server utan att ett
lösenord skickas över nätverk.
```
    SSH
```
kurlade åldringar
=================

Du väntar på ett paket som dina gamla morföräldrar har skickat efter, en
ruskigt fräsch Alien laptop för de tyngsta spelen. Ditt uppdrag är att
hämta paketet så fort det kommer fram till Frasses Kött och Video. Skriv
ett skript som underlättar ditt åtagande.

Misc.
=====

### Auth.allow?

Vad gör Auth till en diffus term?


### NSA

Varför börjar så många guider med ’Disable SELinux’?
```
    Because it creates permission  failure
```
### Gandalf

Du ska sätta upp tre miljöer, produktion, laboration och testing. I
varje miljö ingår det en databasserver, två webfrontar och tre vanliga
servers. Hur skulle du namnge dessa på bästa sätt? Tjänsten som dessa
servrar ska hosta heter nixnux.
```
    For Production:
    nixnux-prod-database
    nixnux-prod-web1
    nixnux-prod-web2
    nixnux-prod-srv1
    nixnux-prod-srv2
    nixnux-prod-srv3

    For Laboration:
    nixnux-lab-database
    nixnux-lab-web1
    nixnux-lab-web2
    nixnux-lab-srv1
    nixnux-lab-srv2
    nixnux-lab-srv3

    For testing:
    nixnux-test-database
    nixnux-test-web1
    nixnux-test-web2
    nixnux-test-srv1
    nixnux-test-srv2
    nixnux-test-srv3
```
BASH
====

### Tacos!

Skriv ett script som svarar på frågan “Är det fredag?”
```
    #!/bin/bash

    c="dag"
    a="Är det freadag? "
    read -p "What do want to know?" question
    echo "I want to know: " $question

    ans ()
    {
        b=$(date +%a)
        if [ $b == "fre" ]
        then
              echo "JA"
        else
              echo "Nej, det är $b$c"
        fi
    }
    ans
```
### yes no

Vad gör följande kommando:

cat food
```
    Show/view the content of the file food.
```
### Sjukt awkward!

Använd ett script- eller cli-verktyg för att ta fram en lista på
efternamn och titel.

    Edmund,Swettenham,författare
    Jane,Marple,detektiv
    Myrna,Harris,servitris
    Phillipa,Haymes,änka
    Rudi,Schertz,receptionist
```
        awk -F "," '{print $2","$3}' <filename>
```
### sortera mera!

Hur sorterar du listan ovan i bokstavsordning på efternamn.
```
    sort -t"," -k2 <filename>
```
### Me, my self and I

I vilket sammanhang kan man behöva pipe:a till nedan kommando?

    grep foo | grep -v grep ?
```
    grep -v grep | grep foo | ?
```
### Hejsan hoppsan

Hur tar du bort filen ’-hej’ ? 
```
    rm ./-hej
```
### Hoppa hage

Ge alla exempel du kan för att skriva ut nedan rad i terminalen.

    /\/\

```
    echo "/\\/\\"
```
### TNT

Beskriv vad raden nedan kan tänkas göra steg för steg. Var i strängen är
rekursionen?

    :(){ :|: & };:    

### keep going, eller?

Vilken skillnad är det mellan

    ; och &&
```
    ; is command separator. Permits putting two or more commands on the same line.
    && returns true if both exp1 and exp2 are true. "&&" is used to chain commands together, such that the next command is run if and only if the preceding command exited without errors (or, more accurately, exits with a return code of 0).
```
### Reflekterande aritmetik

Med så få tecken som möjligt, skriv ut alla tal mellan 1 och 100.
```
   #!/bin/bash
    for ((i=1;i<=100;i++));
    do
        echo $i
    done
```
### Noob Error

Varför misslyckas följande:

    while touch fil; do if [[ -f fil ]]; then rm fil done
```
a "if" statement must ends with "fi" in bash script
```
### macchine inutili

Vad gör ovanstående script?
```
    It creates a file named fil then delete it.
```
### short hand

Ge exempel på en tillämpning av bashs positionala variabler.
```
    #!/bin/bash
    echo "City: $1"
    echo "Country: $2"
```
### Retropespektiv

Vad händer om du kör raden nedan, varför?

    foo(){ foo | foo &};foo

Nät
===

Cisco
-----

### Here is Jonny!

Hur letar du enklast reda på ett anslutet NIC då du känner till MAC
adressen i en L2 enhet.
```
    show mac address-table
```
### Cake?

Hur gör du för att hitta en annan nätverksutrustning som är inkopplad i
en switch eller router?
```
    show interfaces
```
### ISO/IEC/IEEE 8802-3:2014 -\> ISO/IEC 7816

Ange vilka (fler än ett) sätt du kan ta reda på vilka interface som är
err-disablade på en cisco switch.
```
    show interfaces status
```
### Vlan

Du ska koppla upp en server i en access-switch på vlan 208, vlanet finns
inte på switchen så du lägger till det. Hur gör du detta i cisco? Tyvärr
får du ändå ingen länk trots att allt är helt. Vad är troligen orsaken
till de?
```
    vlan 208
    interface ethernet 0/1
    switchport mode access
    switchport access vlan 208

    To get a link we must configure trunk code, since it's in another switch. 
```
### Ben-Hur 3.44

Du har precis satt upp ett storagenät för högupplösta videofiler. Allt
verkar fungera men du lyckas inte få upp hastigheten. Vad kan du göra
för att få upp hastigheten i ditt L2 nät?
```
    1. we can change the interface mode from half duplex to full duplex and set the speed to 500mb/s
    2. show interface <interface name> 
    3. configure terminal 
    4. interface <interface name>
    5. speed 500
    6. duplex full
```
### Great wall of China

En lokal admin (DSA) köper in all infrastruktur centralt men får för sig
att sätta upp en egen brandvägg (cisco ASA) mellan era nät. Det stora
flertalet klienter kommer inte ut på internet, medans vissa gör det. Vad
har troligvis glömts i konfigurationen i ASA:n?

### Rete Lumbricus

En familj har satt upp en egen router med ip-utdelning. I
konfigurationsmenyn kunde man skriva in ip/ett nummer. Familjen
uppfattade numret som antalet klienter och valde således 192.168.0.0/30.
Hur kommer detta att fungera för familjen?
```
    useable host 2:
    192.168.0.1-2
    subnetmask 255.255.255.252
    broadcast address 192.168.0.3
    unusable 192.168.0.0
```
### Lockdown

Vilken RFC beskriver internal nät som inte får routas ut på internet?
```
    RFC 1918
    10.0.0.0 - 10.255.255.255 (10/8 prefix)
    172.16.0.0 - 172.31.255.255 (172.16/12 prefix)
    192.168.0.0 - 192.168.255.255 (192.168/16 prefix)
```
### Skotstek

Vad finns det för möjlighet att knyta ip med MAC-adress i en renodlad L2
switch? Har metoden begränsningar?



### Väldigt trasiga prylar

Helt plötsligt försvinner alla vlan från alla switchar samtidigt. Vad
har troligtvis hänt?
```
    All configurations has been erased.
```
### Huston, we have a problem!

Du har satt lösenord på en switch för att kunna logga in via SSH och
AUX. Du stoppar in en konsollkabel och blir inte promptad för lösenord,
varför?
```
    It's because of the "privilege level 15" within the VTY configs.
```
Misc
----

### !False

Beskriv vad nedan kod gör. Stämmer resonemanget?

    if ! (!0) != !0
 ```   
    !0 = 1 or True
    ! (!0) = 0 or False
    0 != 1  True
    Resonemanget stämmer.
```

