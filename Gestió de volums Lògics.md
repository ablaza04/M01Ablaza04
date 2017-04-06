# Gestió de volums Lògics

- És una capa d'abstracció entre un dispositiu d'emmagatzematge (per exemple un disc) i un sistema de fitxers, que està entre els nostres discos físics i els sistemes de fitxers.

##### Què volen dir les sigles, definició, analogies i exemples de comandes (explicant què fan) vistes a classe de:  

**PV**: ***Physical Volume → Identificació :***  

     Es un dispositiu d'emmagatzematge o un dispositiu de bloc. 
      Pot ser un disc dur, una partició, una targeta SD, un floppy, un dispositivo RAID,etc.
    - Ex: "pvcreate /dev/vda" 
    
**VG**: ***Volume group → Discs Virtuals :*** 

     Es una espècie de disc dur virtual, és un disc compost d'un o més PV's,   que creix posant o creant més PV.
    - Ex: "vgcreate <nom> /dev/vda" , "vgextend"
    
**LV**: ***Logical Volume → Particions :*** 

     S'utilitza per crear sistemes de fitxers, swap, discs per maquines virtuals, LV's són les particions.
    - Ex: "lvcreate" , "lvextend"

##### Entorn de pràctiques: Explicar com farem la pràctica detalladament (màquina virtual i afegir tres discs de 200M).

Primer creem 3 PV :

    - pvcreate /dev/vda 
    - pvcreate /dev/vdb 
    - pvcreate /dev/vdc
![Captura 3 discos](https://github.com/ablaza04/M01Ablaza04/blob/master/Captura%20de%20pantalla%20de%202017-04-06%2013-09-46.png)

##### Pràctica 1: Creació d'un volum lògic a partir d'un dels tres discs durs (vda per exemple). Aquest volum lògic ha de ser del total de capacitat del disc. El volum de grup s'ha de dir practica1 i el volum lògic dades.
Per fer això hem de posar una comanda :

    lvcreate -l +100%FREE -n practica1 dades
**lvcreate:**  es crea un Volum lògic.

**-l:**  aquest paràmetre es per determinar la mida o quantitat de LV que volguem, en aquesta pràctica es **+100%FREE**.

**-n:**  aquest paràmetre es per determinar el nom de lv que en aquest cas es **practica1**, deprés d'això posar el **<vg>** , que es dades. 

    
##### Pràctica 2: Creació d'un sistema de fitxers xfs al volum lògic creat i muntatge a /mnt. També s'ha de crear un fitxer amb dd de 180MB.
Hem de posar aquest comanda:
    
    

##### Pràctica 3: Creació d'un RAID 1 als dos discos sobrants (vdb i vdc per exemple).

##### Pràctica 4: Ampliació del volum lògic de dades al raid.

##### Pràctica 5: Ampliació del sistema de fitxers xfs al tamany actual del volum lògic dades (s'ha de poder fer sense desmuntar-lo de /mnt ja que és xfs). Una vegada creat crearem un nou fitxer de 180M.
