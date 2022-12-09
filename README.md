# Void Linux - CPLR Admin Linux - Manevy Maxence

![Void Linux Logo](https://bitcu.co/en/wp-content/uploads/2020/07/Void_Linux_logo.svg_.png)

## Introduction

Void Linux est une distribution mère qui tourne sur un init system de type Runit et avec le gestionnaire de packet XBPS. Il a aussi l'avantage de pouvoir tourner sur le compilateur C de notre choix comme glibc (commun à Debian, Ubuntu, Fedora, etc...) ou musl (commun à Alpine Linux). Elle fonctionne en rolling release au niveau de ses mises à jours.  

### Minimum requirements 

```yaml
-    CPU: Pentium 4 ou processeur 64-bit (selon l'architecture selectionné) 
-    RAM: 96 Mio de ram  
-    DD: 2 Gio d'espace libre
-    Un accès Internet
```

## Les avantages et les inconvénients 

### Les avantages :

    - Customisable
        - l'os à l'avantage d'être assez customisable, on peut choisir facilement son environnement de bureau, ses logiciels ainsi que ses composants systèmes. 
    - Runit
        - comparé au distribution basique comme Debian ou Red Hat, Void utilise runit qui est un init system plus léger qui peut être intéressant dans des cas d'usage comme le système embarqué ou les pc anciens. 
    - Choix de la lib c (musl ou gcc)
        - Void Linux nous offre une ouverture au choix de son compilateur C, on peut choisir entre musl (connu sur Alpine Linux) ou gcc (connu sur Debian/Red Hat). 
    - Distribution mère
        - La distribution n'est pas dépendant d'une autre. Elle est créé from scratch avec son propre gestionnaire de paquet. 
    - XBPS
        - Il s'agit d'un gestionnaire de paquet plus rapide mais qui permet aussi de détecter les soucis de conflit ou des librairies incompatible. 
    - XBPS-src
        - une autre partie du gestionnaire de paquet qui permet de compiler ses paquets avec leurs codes sources à la manière de Gentoo. 

### Les inconvénients 

    - Rolling release
        - Ce mode de fonctionnement n'apporte pas forcément beaucoup de stabilité et donc peu recommandé dans l'usage de système industriel ou de serveur. 


## Void et son runit

Void à la particularité d'avoir un init system assez léger comparé à SystemD, il aura peut-être moins de fonction mais peut-être intéressant dans le cadre de système embarqué, du client léger diskless ou un pc un peu ancien. 

on peut retrouver les fonctions suivants avec cette init system : 

    - Les services fonctionne sous forme de dossier 
        L'enssemble des services qui sont en marche au démarrage sont dans /var/service/
    - Création de service par utilisateur
        - Prévoir un service qui s'éxecute avec un compte utilisateur spécifique et ses propres droits. 
    - Init léger qui peut tourner facilement sur des machines avec moins de 256 Mio de ram.


