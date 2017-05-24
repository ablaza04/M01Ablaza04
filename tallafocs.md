# Tallafocs
---

### 1. Tallafocs

1. Què es un sistema tallafocs? Quina és la seva finalitat?
    - És un programa o sistema de seguretat que controla les comunicacions,  permetent-les o prohibint-les segons les polítiques de xarxa. 
    
    
2. Quines generacions de tallafocs hi ha hagut i què millorava cadascun?
    - Primera generació - tallafocs de xarxa: filtrat de paquets
    - Segona generació - tallafocs d'estat
    - Tercera generació - tallafocs d'aplicació
    - Milloraven les inspeccions dels paquets en cada generació.


3. Quines capes té el model OSI?
    - Física
    - Enllaç de dades 
    - Xarxa 
    - Transport 
    - Sessió
    - Presentació
    - Aplicació
    
    
4. Quines capes té el model TCP/IP? En aquest cas feu una breu descripció de les funcionalitats de cada capa.
    - Nivell d'Aplicació : 
        - Serveis de xarxa a aplicacions 
        - Representació de dades 
        - Comunicació entre dispositius de la xarxa.
    - Nivell de Transport :
        - Connexió punt a punt i fiabilitat de les dades.
    - Nivell de Xarxa :
        - Determinació de ruta i IP.
    - Nivell d'accès a xarxa :
        - Direccionament físic (MAC i LLC), Senyal i transmisió binaria.
       
       
5. A quina capa/capes sol treballar tradicionalment un tallafocs?
    - Treballa en el Nivell d'Aplicació , capa 7 del model OSI.


### 2. Tallafocs Linux


1. Busqueu quins són els tradicionals sistemes de tallafocs incorporats en linux i anomeneu-los
    - Firestarter 
    - FirewallD
    - Iptables
    - Fail2ban
    - UFW


2. Quins dels anteriors tallafocs estan instal.lats al fedora de classe? Com ho comproveu?
    - FirewallD : Dynamic Firewall Manager
    - He fet un man de tots els possibles firewalls en la terminal.


3. Algun dels anteriors tallafocs es troba activat?
    - No, has d'entrar a root per activar-ho.


4. Instal.leu el servidor web httpd o nginx i activeu-ne el servei (dnf installl ...  ; systemctl ....). Indiqueu les comandes i comproveu que des d'una altra màquina podeu accedir via web a la vostra IP (digueu-li a un company). Hauria de sortir la plana per defecte.


5. Activeu el servei firewalld. Indiqueu com ho feu.
    - Entrar a root 
    - systemctl status firewalld per veure si està activat
    - systemctl start firewalld


6. Comproveu si ara es pot seguir accedint.
    - No.


### 3. Win7

1. Porta aquest SO algun tallafocs incorporat?



2. Arrenqueu una màquina win7 a isard.escoladeltreball.org



3. Indiqueu com arribar al tallafocs (passos i pantalles)
4. Es troba activat en aquest windows?



5. Busqueu un altre tallafocs per windows. Indiqueu la plana web i les prestacions que ens dona. Intenteu que NOMÉS sigui tallafocs.
