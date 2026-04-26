# Tutoriel : Introduction à Ubuntu

Ce tutoriel est une présentation générale pour comprendre ce qu'est Ubuntu, son fonctionnement et son architecture, avant de passer à la phase d'installation.

## 1. Qu'est-ce que Ubuntu ? (Chnahowa Ubuntu ?)

**Ubuntu** est un système d'exploitation (comme Windows ou macOS), mais il est basé sur **Linux** (plus précisément sur la distribution Debian). 
C'est un système **open-source** (son code est public) et totalement **gratuit**. Il est très utilisé par les développeurs, dans les entreprises pour les serveurs, mais aussi par les utilisateurs normaux pour leur ordinateur personnel.

Le mot "Ubuntu" vient d'une ancienne langue africaine et signifie *"Je suis ce que je suis grâce à ce que nous sommes tous"* (Humanité vers les autres). Cela reflète l'esprit de communauté et de partage du monde open-source. Il est développé et sponsorisé par la société anglaise **Canonical**.

## 2. Comment c'est structuré ? (Kifach Mqad ?)

L'architecture d'Ubuntu (et de Linux en général) est composée de plusieurs couches :

1. **Le Matériel (Hardware) :** Votre processeur, RAM, disque dur, etc.
2. **Le Noyau (Kernel Linux) :** C'est le cœur du système. Il sert de traducteur entre les logiciels (vos applications) et le matériel (votre PC).
3. **Le Shell (Terminal) :** C'est l'interface en ligne de commande (souvent `bash`) qui permet de donner des ordres directs au système.
4. **L'Environnement de Bureau (GUI) :** Contrairement aux serveurs, la version "Desktop" d'Ubuntu possède une interface graphique. Par défaut, Ubuntu utilise **GNOME**, qui gère les fenêtres, les icônes, la souris, etc.
5. **Les Applications :** Les navigateurs (Firefox), les éditeurs de code (VS Code), etc.

## 3. Le système de fichiers (File System)

Contrairement à Windows où on trouve les disques `C:\` ou `D:\`, sur Ubuntu, tout part de la "Racine" appelée **`/`** (Root).
Voici les dossiers les plus importants :
* `/home` : L'équivalent de "Utilisateurs" sur Windows. C'est ici que se trouvent vos fichiers personnels (Documents, Téléchargements, etc.).
* `/etc` : Contient tous les fichiers de configuration du système.
* `/var` : Contient les fichiers variables, comme les logs (historique des erreurs) ou les bases de données.
* `/bin` et `/usr/bin` : Contiennent les programmes exécutables (les commandes que vous tapez dans le terminal).

## 4. Gestion des logiciels (APT)

Sur Windows, on télécharge un fichier `.exe` sur internet pour installer un logiciel. 
Sur Ubuntu, on utilise un **Gestionnaire de paquets** appelé **APT** (Advanced Package Tool). C'est comme un "App Store" intégré au terminal.

* Pour mettre à jour la liste des logiciels : `sudo apt update`
* Pour installer un logiciel : `sudo apt install nom_du_logiciel`

*(Note : `sudo` est une commande magique qui vous donne les droits "Administrateur" temporairement pour faire des modifications importantes).*

## 5. Le cycle de vie des versions (LTS)

Ubuntu sort une nouvelle version tous les 6 mois (en avril et en octobre).
* **Les versions LTS (Long Term Support) :** Elles sortent tous les 2 ans (en avril des années paires, ex: 20.04, 22.04, 24.04). Elles sont super stables et reçoivent des mises à jour de sécurité pendant **5 ans**. C'est ce qu'on utilise en entreprise.
* **Les versions normales :** Elles ne sont supportées que pendant 9 mois et servent à tester de nouvelles fonctionnalités.

## 6. Les différentes saveurs (Flavors)

Ubuntu existe en plusieurs versions adaptées aux besoins :
* **Ubuntu Desktop :** Pour les ordinateurs personnels (ce que vous allez installer).
* **Ubuntu Server :** Pour les serveurs web ou bases de données. Il n'y a pas d'interface graphique, tout se gère en ligne de commande pour économiser la RAM et le processeur.
* **Kubuntu, Xubuntu, Lubuntu :** C'est le même Ubuntu, mais avec une interface graphique différente (plus légère pour les vieux PC, ou qui ressemble plus à Windows).

---
**En résumé :** Ubuntu est un système robuste, gratuit, sécurisé et très logique dans son fonctionnement. C'est la porte d'entrée parfaite pour découvrir le monde de Linux et de l'administration système !
