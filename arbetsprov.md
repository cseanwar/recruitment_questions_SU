Förutsättningar och tillvägagångssätt
=====================================

Introduktion
------------

Detta test syftar till att vi på Stockholms Universitet ska få en
tydligare bild av din tekniska kompetens. Noteras bör att detta inte är
någon korkad skoluppgift utan syftar till att ett antal problem ska
lösas. Om du löser problemet helt själv, googlar eller tar hjälp av en
kompis är oss likgiltigt så länge du har förstått och lärt dig. Dessa
frågor är primärt avsedda för en praktikant som inte ännu gått klart
någon linux utbildning. Faller du inte inom den kategorin kommer
större vikt att läggas på det du programmerat/scriptat tidigare.

Bedöming & tidsram
------------------

Bedömningen kommer i första hand att ta hänsyn till hur frågorna är
lösta och i andra hand att rätt svar har presenterats. Vilket gör att en
diskussion runt en fråga är bättre än att helt utelämna den. Maila dina
svar tillsammans med källa till jesper.udd@su.se inom den tid ni har
kommit fram till. Om du har något git\*-konto kollar vi gärna igenom
dina repon.

Fel
---

Om något skulle vara otydligt eller felaktigt är du välkommen att maila.
Så, sätt dig tillrätta och ta fram din favoriteditor...

Linux
=====

GNU
---

### Vimsigt värre..

På hur många sätt är VIM överlägsen Emacs?

### Insomnia

Hur gör du om du vill att din webbläsare ska stängas av på din
linuxdator för att du ska komma i säng klockan 03:00 varje dag?

### !telnet

Nämn minst ett sätt att logga in säkert på en server utan att ett
lösenord skickas över nätverk.

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

### Gandalf

Du ska sätta upp tre miljöer, produktion, laboration och testing. I
varje miljö ingår det en databasserver, två webfrontar och tre vanliga
servers. Hur skulle du namnge dessa på bästa sätt? Tjänsten som dessa
servrar ska hosta heter nixnux.

BASH
====

### Tacos!

Skriv ett script som svarar på frågan “Är det fredag?”

### yes no

Vad gör följande kommando:

    cat food

### Sjukt awkward!

Använd ett script- eller cli-verktyg för att ta fram en lista på
efternamn och titel.

    Edmund,Swettenham,författare
    Jane,Marple,detektiv
    Myrna,Harris,servitris
    Phillipa,Haymes,änka
    Rudi,Schertz,receptionist

### sortera mera!

Hur sorterar du listan ovan i bokstavsordning på efternamn.

### Me, my self and I

I vilket sammanhang kan man behöva pipe:a till nedan kommando?

    grep foo | grep -v grep ?

### Hejsan hoppsan

Hur tar du bort filen ’-hej’ ?

### Hoppa hage

Ge alla exempel du kan för att skriva ut nedan rad i terminalen.

    /\/\

### TNT

Beskriv vad raden nedan kan tänkas göra steg för steg. Var i strängen är
rekursionen?

    :(){ :|: & };:

### keep going, eller?

Vilken skillnad är det mellan

    ; och &&

### Reflekterande aritmetik

Med så få tecken som möjligt, skriv ut alla tal mellan 1 och 100.

### Noob Error

Varför misslyckas följande:

    while touch fil; do if [[ -f fil ]]; then rm fil done

### macchine inutili

Vad gör ovanstående script?

### short hand

Ge exempel på en tillämpning av bashs positionala variabler.

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

### Cake?

Hur gör du för att hitta en annan nätverksutrustning som är inkopplad i
en switch eller router?

### ISO/IEC/IEEE 8802-3:2014 -\> ISO/IEC 7816

Ange vilka (fler än ett) sätt du kan ta reda på vilka interface som är
err-disablade på en cisco switch.

### Vlan

Du ska koppla upp en server i en access-switch på vlan 208, vlanet finns
inte på switchen så du lägger till det. Hur gör du detta i cisco? Tyvärr
får du ändå ingen länk trots att allt är helt. Vad är troligen orsaken
till de?

### Ben-Hur 3.44

Du har precis satt upp ett storagenät för högupplösta videofiler. Allt
verkar fungera men du lyckas inte få upp hastigheten. Vad kan du göra
för att få upp hastigheten i ditt L2 nät?

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

### Lockdown

Vilken RFC beskriver interna nät som inte får routas ut på internet?

### Skotstek

Vad finns det för möjlighet att knyta ip med MAC-adress i en renodlad L2
switch? Har metoden begränsningar?

### Väldigt trasiga prylar

Helt plötsligt försvinner alla vlan från alla switchar samtidigt. Vad
har troligtvis hänt?

### Huston, we have a problem!

Du har satt lösenord på en switch för att kunna logga in via SSH och
AUX. Du stoppar in en konsollkabel och blir inte promptad för lösenord,
varför?

Misc
----

### !False

Beskriv vad nedan kod gör. Stämmer resonemanget?

    if ! (!0) != !0

Q
=

Skriv en valfri fråga med svar, motivering och rubrik. Om den är bra
kommer den vara med i nästa utgåva av detta prov.
