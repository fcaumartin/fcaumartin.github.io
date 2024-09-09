---
theme: afpa
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: 'linux2.webp'
marp: true
----------------------------------------------------------------
# Présentation Linux
(20 minutes pour découvrir `Linux`)

----------------------------------------------------------------
# Histoire d'Unix
Dans les années 1970, le laboratoire **Bell Lab** de l'entreprise **AT&T** crée le système d'exploitation multi-utilisateurs Unix.

Ce système sera repris par beaucoup d'entreprises et donnera naissance à une multitude de variantes d'`Unix`.

Les survivants actuels:
- **BSD** (**FreeBSD**, **NetBSD**, **OpenBSD**)
- **iOS**, **macOSX**
- **AIX**, **Solaris**, **HP-UX**

----------------------------------------------------------------
# Linux

Linux est un système inspiré du système Unix.

Il existe une multitude (>500) de distributions RedHat, Suze, Ubuntu... (Debian et Fedora ont servi de base) 

Freebox, BouyguesBox..., Andoid utilisent aussi un noyau `Linux`


----------------------------------------------------------------
# Organisation du système de fichiers

`/etc`          fichiers de configuration du système

`/root`         répertoire home du super utilisateur
`/sbin`         outils réservés à l'administrateur

`/home`         répertoire pour les profils utilisateurs

`/var`          
`/usr`          programmes du système pour les utilisateurs
`/lib`
`...`


----------------------------------------------------------------
# sudo

`sudo` permet d'obtenir les droits `su` ou `root` pour exécuter une commande.

Exemple:
```
sudo kill xxx
```

*Le système vous demande de saisir **votre** mot de passe !*

*L'utilisateur qui lance cette commande doit être habilité (autorisé à utiliser `sudo`) !*


----------------------------------------------------------------
# APT (Gestion des packages)

- Mettre à jour la liste de paquets
`sudo apt update`
- Mettre à jour le système
`sudo apt upgrade`
- Installer une application
`sudo apt install mc`
- Supprimer une application
`sudo apt remove mc --purge`



----------------------------------------------------------------
# la console

Ouvrir un terminal `Ctrl-Alt-T` 

Copier/Coller avec `Ctrl-Maj-C` / `Ctrl-Maj-V`

Basculer en mode texte `Ctrl-F3` **...** `Ctrl-F6`

Pour manipuler les fichiers dans la console
- Afficher `ls`
- changer de répertoire `cd`
- Créer ou supprimer de répertoires `mkdir`, `rm` 

----------------------------------------------------------------
# Quelques commandes...

|  | Commandes |
|--|--|
|Afficher la liste des processus|`ps ax`|
|Tuer le processus xxx|`kill -9 xxx`|
|Liste des périphériques USB|`lsusb`|
|Liste des périphériques `block` (disques durs) |`lsblk`|
|Utilitaire de gestion des partitions |`fdisk /dev/sda`|
|Afficher les addresses `IP` des interfaces réseaux|`ip a`|
|Liste des connexions réseaux en cours|`ss`|
|Outils de découverte du réseau|`nmap`|


----------------------------------------------------------------
# Gestion des droits

`chmod`

|r|w|x|r|w|x|r|w|x|
|-|-|-|-|-|-|-|-|-|
|4|2|1|4|2|1|4|2|1|



----------------------------------------------------------------
# Gestion des droits


`setfacl`

----------------------------------------------------------------
# Gestion des utilisateurs

`adduser`

`passwd`

`usermod`

----------------------------------------------------------------
# Gestion des services (systemd)

`systemd` est les gestionnaire de services.

`systemctl` est l'outil de gestion de `systemd`

----------------------------------------------------------------
# Gestion des services (systemd)



| Commandes |
|--|
|`systemctl start apache2`|
|`systemctl stop apache2`|
|`systemctl restart apache2`|
||
|`systemctl enable apache2`|
|`systemctl desable apache2`|

**
----------------------------------------------------------------
# Ressources



### 1. Documentation locale
    man


### 2. Guide d'aministration en ligne
[https://debian-handbook.info/browse/fr-FR/stable/index.html](https://debian-handbook.info/browse/fr-FR/stable/index.html)
