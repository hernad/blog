# UOS netačno

## 1) Prepoznaj desktop operativne sisteme

1. windows(9x, 2000, XP)
2. Linux
3. MacOS
4. unix
5. solaris
6. FreeBSD

### Očekivani odgovor je navodno:

1, 2, 3.


### Komentar

#### Linux 

Linux je operativni sistem koji se koristi i na serverskoj strani i na klijentskoj strani.

Linux je klasični general-purpose OS.

Informacija iz prve ruke: mi stavljamo na server ubuntu. 

Jedina razlika je ta što na serveru uobičajeno stavljamo jedan od *server-tuniranih* kernela, 
a na klijentu jedan od desktop tuniranih kernela.

Glavna razlika je scheduling koji je kod serverskih kernela prilagođen back-end procesima dok je kod desktopa prilagođena front-end procesima.

Na server uobičajeno ne stavljamo XWindows, ali mi niko ne brani da ga stavim.

Slično, na desktopu je uobičajeno XWindows/GUI login default, ali mi opet niko ne brani da sve što radim radim na konzoli.

[Wikipedia ubuntu stranica]:http://en.wikipedia.org/wiki/Ubuntu_%28operating_system%29 priča o Ubuntu kao jednom operativnom sistemu.

Desktop, serverske, cloud session ... sve su to varijante jednog te istog OS-a.

#### FreeBSD

Što se [FreeBSD-a](http://en.wikipedia.org/wiki/FreeBSD) tiče, njegovi fun-ovi takođe koriste ovaj operativni sistem i na serverskoj i na korisničkoj strani - kao desktop.

Otiđite pa provjerite.

#### Unix

Za [Unix]:http://en.wikipedia.org/wiki/Unix se komotno može reći da je ovdje ubačen "po babe i žabe zajedno" principu.

Postoji niz implementacija Unix-a, pa bi se moglo pričati o Unix-like operativnim sistemima (plural), ali ne o Unix operativnom sistemu.

Ako tako kažemo, upadamo u novu grešku, iz razloga što su [Linux]:(http://en.wikipedia.org/wiki/Linux), FreeBSD unix, Solaris "Unix-like" operativni sistemi.

Sve je to znači jedna familija operativnih sistema


### Zaključak

Klasifikacija je pogrešna, i kod studenata može izazvati samo totalnu konfuziju.

Ovo je klasični primjer "Babe i žabe zajedno" klasifikacije.

## 2) Računarske mreže se sastoje od hardverskog i softverskog dijela ?

1. računar
2. software (sistem i aplikativni)
3. komunikacijski uređaj
4. tačan odgovor je 1, 2, 4
5. samo 1, 2, 3
6. komunikacijski medij


### Odgovor je navodno:

**1**, **2**, **3**, **6**

### Komentari

Ovo navodno zato što sam prepisao odogovre koje je naveo nepoznati student.

Navodno i radi toga što **pojma nemam šta je pisac pitanja htio da pita !?**

Računarska mreža, kada ja u svom poslu pričam se ne sastoji od računara.

Ona se sastoji samo od mrežnih uređaja (gore je to 3), kablova (gore je to 6).

Međutim, u drugom **kontekstu** termin se koristi i za sve ovo zajedno sa računarima koji su dio te mreže.

Pa onda kada ponovo počnem razmišljati, svaki današnji mrežni uređaj ima svoj firmware na kome je operativni sistem sa dodatnim aplikacijama.

### Mreža a) Neka mi neko kaže od čega se sastoji računarska mreža koju sam ja napravio ?!

Evo ja sjedim u firmi koja ima računarsku mrežu.

*Na tu mrežu* je prikopčano putem LAN i WIFI konekcija više računara. 

Uočite sad formulaciju moje rečenice. Ja implicite smatram da računari *nisu* dio mreže.

Računarska mreža je preko mrežnog router-a WRT54GL prikopčana na internet.

Naš internet provajder je BH Telecom, a način konekcije je ADSL.

Unutar mreže nalazi se par malih (5x i 8x  10/100MB i 1GB ) switch-eva i jedan pametni 16 portni.

Ovaj 16x je tako pametan da ima i svoj web interfejs. 

Na internet router-u se vrti linux koji smo mi podesili prema našim potrebama. 

Dio te mrežne infrastrukture je naša aplikacija koja prilikom promjene publi IP adrese na našem router-u osvježava naše vanjske DNS servere.

To smo tako uradili jer ne damo da nas BH telecom guli za +200-300 KM/mjesečno radi fiksne IP adrese.

Suma sumarum, dio *naše* računarske mreže je gomila mrežnih uređaja, koji imaju na sebi sistemski i aplikativni software. Sve to je povezano mrežnim kablovima.

### Mreža b)

Međutim, negdje drugdje računarsku mreža može biti sastavljena od dva računara povezana crosslink kablom.

### Mreža c)

Na trećem mjestu može biti jedan mali glupi switch koji se smatra komadom hardware-a koji se upali i to je to.

### Zaključak

Po meni bi odgovori za svaku od mreža bili različiti

Za mrežu a):

**2**, **3**, **6** 

(iako je router u principu obični računar, on se u kontekstu mrežne infrastrukture svrstava u komunikacijski uređaj)


Za mrežu b):

**6**

Za mrežu c):

**3** i **6**

Ovo pitanje nije dobro formulisano. 'Tice znaju šta je pisac mislio kad je ovo pitao.


## 3) Spoji mreznu topologiju sa najčešće korištenim standardima kartica i konektora

Topologije:
1. BUS
2. Zvijezda
3. Prsten

Kartice i konektori:
1. centralni čvor, RJ45
2. koaksijalni kabel, T konektor, na krajevima terminator
3. ring topologija, RJ45


### Odgovor 

?

### Komentar

Kako može biti u skupini kartica i konektora **"ring topologija, RJ45"**


Probaću raspetljati uz pomoć [wikipedije](http://en.wikipedia.org/wiki/Network_topology)


Zvijezda (star) => centralni čvor sa RJ45

BUS => koaksijalni kabl, T konektor, terminator

sistemom eliminacije dolazim do

Prsten (ring) => ring topologija, RJ45

Konkretno [ring network](http://en.wikipedia.org/wiki/Ring_network)

Disadvantages
* One malfunctioning workstation or bad port in the MAU can create problems for the entire network
* Moves, adds and changes of devices can affect the network
* Network adapter cards and MAU's are much more expensive than Ethernet cards and hubs
* Much slower than an Ethernet network under normal load

Pa da, zato se sa ovim nisam sretao nikada - ovo više niko ne koristi.

Što se tiče T konektora, koaksijalnog kabla, sjećam se patnji koje smo imali i ganjanja sa kliještima sa rješavanjem problema: "Gdje je prekid ?"

Čovječe jest ta mreža bila nestabilna. Svaki drugi dan kod nekog korisnika iskoči. Kad su se pojavili hub-ovi sa RJ-45 konektorima to je bilo pravo slavlje.

Da li mlade kolege kontaju o čemu ja uopšte pričam ? Da li ih je UOS šta naučio sa ovim pitanjem ?

Ubjeđen sam da je odgovor 2 x **NE**.

### Zaključak

Još jedan set nejasnih i beskorisnih pitanja i odgovora.
