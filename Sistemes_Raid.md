# SISTEMES RAID

1. Resum de sistemes RAID fent servir una taula com la vista a classe.

| Nivells | Nº Mín. Discs | Nº Màx. Discs Fallats | Capacitat | Read | Write |
------------ | :------------: | :------------: | ------------ | ------------ | ------------ |
|    RAID 0     |       2        |       0        |      100%      |   Excel·lent   |    Excel·lent | 
|    RAID 1     |       2 (máx)  |       1        |      50%       |   Very Good    |    Good | 
|    RAID 5     |       3        |       1        |   67% - 94%    |   Very Good    |    Good |
|    RAID 6     |       4        |       2        |   50% - 88%    |     Good       |    Good |
|    RAID 10    |       4        |   1/Mirror     |      50%       |   Very Good    |    Good |
    
2. Descripció de la metodologia utilitzada a classe per a fer proves amb màquines virtuals.
- mdadm: S'utilitza per l'ús de gestionar i controlar el software RAID dispositius.
- create: pots crear el nom del dispositiu que vulguis.
- level=mirror: poses el nivell de RAID que vols.
- raid-devices: Nº de discos que vols 
- disc1 , disc2 , etc: quantitat de discos que vols posar-hi 

3. Comandes i descripció de les mateixes per tal de crear un sistema RAID1
- Per crear un Sistema RAID1 es posar la comanda: 
    - mdadm --create dev/md0 --level=1 --raid-devices=2 dev/vda /dev/vdb

4. Comandes i descripció de les mateixes per tal de crear un sistema RAID5
- Per crear un Sistema RAID5 es posar la comanda: 
    - mdadm --create dev/md0 --level=5 --raid-devices=2 dev/vda /dev/vdb

5. Comandes i descripció de les mateixes per tal de crear un sistema RAID6
- Per crear un Sistema RAID6 es posar la comanda: 
    - mdadm --create dev/md0 --level=6 --raid-devices=2 dev/vda /dev/vdb

6. Comandes i descripció de les mateixes per tal de crear un sistema RAID10
- Per crear un Sistema RAID10 es posar la comanda: 
    - mdadm --create dev/md0 --level=10 --raid-devices=2 dev/vda /dev/vdb
