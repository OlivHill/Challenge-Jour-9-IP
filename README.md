# Challenge-Jour-9 - IP

## Consignes :
Pour les adresses IP et masques de sous-réseau suivants, calculez :
    l’adresse de réseau
    l’adresse de broadcast
    le nombre d’adresses utilisables par des machines
    la plage d’adresses disponibles

Certains utilisent la notation « classique », d’autres la notation CIDR :
    192.168.13.67/24
    172.16.0.1 – 255.255.255.0
    172.16.27.32/23
    10.7.5.1 – 255.255.128.0
    10.42.0.82/12


### Exercice 1 : 192.168.13.67/24
#### Détermination du masque sous réseau, calcul de l'adresse de réseau et du broadcast :

##### Calcul de l'adresse de réseau et du broadcast :
Adresse IP : 192.168.13.67
Masque sous-réseau : /24 = 24 premiers bits réseau puis 8 bits machine) = équivaut à 255.255.255.0

###### Formule du chiffre magique :
 - octet significatif = 0
 - détermination du chiffre magique = 256 - 0 = 256
 - Multiples du nombre magique jusqu'à 256 = 0  256 (il faudra retenir 255)
 - Adresse IP 192.168.13.67 => **192.168.13.0** (0 étant le multiple inférieur ou égal le plus proche de 67)
 - Adresse de broadcast : 192.168.13.67 => **192.168.13.255** (255 étant le multiple supérieur le plus proche de 67)

###### Nombre d'adresses utilisables par des machines: Masque sous réseau : /24 (CIDR) ou 255.255.255.0
- Méthode manuelle : le masque sous réseau 255.255.255.0 correspond en binaire à 3 octets de 1 (=24 bits) puis 1 octet (8 bits) de 0 : 11111111 11111111 11111111 00000000 : en décimal = 256 -2 = **254**
- Notation CIDR : /24, c'est à dire 24 bits 1 puis 8 bits 0. Il y a donc 8 bits disponibles pour les machines.
  On applique la formule (2 puissance n)-2 où n=8 : (2 puissance 8)-2 = 256 - 2 = **254**

#### Réponses :
- l’adresse de réseau : 192.168.13.0
- l’adresse de broadcast : 192.168.13.255
- le nombre d’adresses utilisables par des machines : 254
- la plage d’adresses disponibles : 192.168.13.1 à 192.168.13.254


### Exercice 2 : 172.16.0.1 – 255.255.255.0
#### Détermination du masque sous réseau, calcul de l'adresse de réseau et du broadcast :

##### Calcul de l'adresse de réseau et du broadcast :
Adresse IP : 172.16.0.1
Masque sous-réseau : 255.255.255.0

###### Formule du chiffre magique :
 - octet significatif = 0
 - détermination du chiffre magique = 256 - 0 = 256
 - Multiples du nombre magique jusqu'à 256 = 0  256 (il faudra retenir 255)
 - Adresse IP 172.16.0.1 => **172.16.0.0** (0 étant le multiple inférieur ou égal le plus proche de 0)
 - Adresse de broadcast : 172.16.0.1 => **172.16.0.255** (255 étant le multiple supérieur le plus proche de 67)

###### Nombre d'adresses utilisables par des machines: Masque sous réseau : 255.255.255.0
- Méthode manuelle : le masque sous réseau 255.255.255.0 correspond en binaire à 3 octets de 1 (=24 bits) puis 1 octet (8 bits) de 0 : 11111111 11111111 11111111 00000000 : en décimal = 256 -2 = **254**
- Notation CIDR : /24, c'est à dire 24 bits 1 puis 8 bits 0. Il y a donc 8 bits disponibles pour les machines.
  On applique la formule (2 puissance n)-2 où n=8 : (2 puissance 8)-2 = 256 - 2 = **254**

#### Réponses :
- l’adresse de réseau : 172.16.0.0
- l’adresse de broadcast : 172.16.0.255
- le nombre d’adresses utilisables par des machines : 254
- la plage d’adresses disponibles : 172.16.0.1 à 172.16.0.254


### Exercice 3 :  172.16.27.32/23
#### Détermination du masque sous réseau, calcul de l'adresse de réseau et du broadcast :

##### Calcul de l'adresse de réseau et du broadcast :
Adresse IP : 172.16.27.32
Masque sous-réseau : /23 = 23 premiers bits réseau puis 9 bits machine) = équivaut à 255.255.254.0

###### Formule du chiffre magique :
 - octet significatif = 27
 - détermination du chiffre magique = 256 - 27 = 229
 - Multiples du nombre magique jusqu'à 256 = 0  229
 - Adresse IP 172.16.27.32 => **172.16.0.0** (0 étant le multiple inférieur ou égal le plus proche de 27)
 - Adresse de broadcast : 172.16.27.32 => **172.16.229.255** (229 étant le multiple supérieur le plus proche de 27)

###### Nombre d'adresses utilisables par des machines: Masque sous réseau : 255.255.254.0
- Méthode manuelle : le masque sous réseau 255.255.254.0 correspond en binaire à 2 octets de 1 (=16 bits) puis 11111110 00000000 (c'est à dire 9 bits de 0) : en décimal = 512 -2 = **510**
- Notation CIDR : /23, c'est à dire 23 bits 1 puis 9 bits 0. Il y a donc 9 bits disponibles pour les machines.
  On applique la formule (2 puissance n)-2 où n=9 : (2 puissance 9)-2 = 512 - 2 = **510**

#### Réponses :
- l’adresse de réseau : 172.16.0.0
- l’adresse de broadcast : 172.16.229.255
- le nombre d’adresses utilisables par des machines : 510
- la plage d’adresses disponibles : 172.16.0.1 à 172.16.0.254


### Exercice 4 :  10.7.5.1 – 255.255.128.0
#### Détermination du masque sous réseau, calcul de l'adresse de réseau et du broadcast :

##### Calcul de l'adresse de réseau et du broadcast :
Adresse IP : 10.7.5.1
Masque sous-réseau : 255.255.128.0

###### Formule du chiffre magique :
 - octet significatif = 128
 - détermination du chiffre magique = 256 - 128 = 128
 - Multiples du nombre magique jusqu'à 256 = 0  128  256
 - Adresse IP 10.7.5.1 => **10.7.0.0** (0 étant le multiple inférieur ou égal le plus proche de 128)
 - Adresse de broadcast : 10.7.5.1 => **10.7.128.255** (128 étant le multiple supérieur le plus proche de 5)

###### Nombre d'adresses utilisables par des machines: Masque sous réseau : 255.255.128.0
- Méthode manuelle : le masque sous réseau 255.255.128.0 correspond en binaire à 2 octets de 1 (=16 bits) puis 10000000 00000000 (c'est à dire 15 bits de 0) : en décimal = 32768 -2 = **32766**
- Notation CIDR : /17, c'est à dire 17 bits 1 puis 15 bits 0. Il y a donc 15 bits disponibles pour les machines.
  On applique la formule (2 puissance n)-2 où n=15 : (2 puissance 15)-2 = 32768 - 2 = **32766**

#### Réponses :
- l’adresse de réseau : 10.7.0.0
- l’adresse de broadcast : 10.7.128.255
- le nombre d’adresses utilisables par des machines : 32766
- la plage d’adresses disponibles : 10.7.0.1 à 10.7.127.255


### Exercice 5 :  10.42.0.82/12
#### Détermination du masque sous réseau, calcul de l'adresse de réseau et du broadcast :

##### Calcul de l'adresse de réseau et du broadcast :
Adresse IP : 10.42.0.82
Masque sous-réseau : /12 = 12 premiers bits réseau puis 20 bits machine = équivaut à 255.240.0.0

###### Formule du chiffre magique :
 - octet significatif = 240
 - détermination du chiffre magique = 256 - 240 = 16
 - Multiples du nombre magique jusqu'à 256 = 0  16 32 48
 - Adresse IP 10.42.0.82 => **10.32.0.0** (32 étant le multiple inférieur ou égal le plus proche de 42)
 - Adresse de broadcast : 10.42.0.82 => **10.48.255.255** (48 étant le multiple supérieur le plus proche de 42)

###### Nombre d'adresses utilisables par des machines: Masque sous réseau : 255.240.0.0
- Méthode manuelle : le masque sous réseau 255.240.0.0 correspond en binaire à 1 octets de 1 (=8 bits) puis 11110000 puis 2 octets de 0 (c'est à dire 20 bits de 0) : en décimal = 1 048 576 -2 = **1 048 574**
- Notation CIDR : /12, c'est à dire 12 bits 1 puis 20 bits 0. Il y a donc 20 bits disponibles pour les machines.
  On applique la formule (2 puissance n)-2 où n=20 : (2 puissance 20)-2 = 1 048 576 - 2 = **1 048 574**

#### Réponses :
- l’adresse de réseau : 10.32.0.0
- l’adresse de broadcast : 10.48.255.255
- le nombre d’adresses utilisables par des machines : 1 048 574
- la plage d’adresses disponibles : 10.32.0.1 à 10.47.255.255
