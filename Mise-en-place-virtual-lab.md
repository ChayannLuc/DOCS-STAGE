Mise en place d’un Virtual Lab
Introduction
Pour créer un Virtual Lab, on utilise la solution Veeam Backup & Replication.
Le Virtual Lab permet d’exécuter des tests de restauration isolés, notamment pour SureBackup.

1. Création du Virtual Lab
Étape 1 — Accéder à la création
Dans Veeam, aller dans Backup Infrastructure

Dans la section SureBackup, faire un clic droit sur Virtual Labs

Cliquer sur Add Virtual Lab

Étape 2 — Nommer le Virtual Lab
Donner un nom explicite

Cliquer sur Next

Étape 3 — Sélectionner l’hôte ESXi
Cliquer sur Choose

Sélectionner l’hôte ESXi sur lequel sera créé le Virtual Lab

Exigences de l’hôte ESXi :

L’hôte doit être situé dans le même datacenter que les réplicas des VMs

L’hôte doit disposer de ressources CPU et RAM suffisantes

Étape 4 — Base de données
Ne rien renseigner

Cliquer sur Next

Étape 5 — Configuration du Proxy
Cocher Use proxy appliance in this virtual lab

Rôle du proxy :  
Le proxy sert de passerelle entre le serveur de sauvegarde et les VMs du Virtual Lab.
Sans proxy, Veeam ne fera qu’un test de présence des VMs, sans vérification approfondie.

Étape 6 — Modifier les paramètres du Proxy
Cliquer sur Edit pour modifier le nom ou le datastore

Sélectionner le réseau de production sur lequel le proxy sera créé

Cliquer sur Configure

Choisir IPv4, IPv6 ou les deux

Spécifier :

L’adresse IP du proxy

Le masque

La passerelle

Le DNS

Étape 7 — Mode de configuration
Choisir Basic single host

Étape 8 — Création
Une fois validé, le Virtual Lab est créé sur l’hôte ESXi sélectionné.

2. Création d’un Application Group
Une fois le Virtual Lab en place, il faut créer un Application Group.
Cet ensemble regroupe les VMs nécessaires au bon fonctionnement des tests SureBackup (DNS, DHCP, SQL, fichiers, etc.).

Étape 1 — Création
Clic droit → Add Application Group

Donner un nom explicite

Étape 2 — Ajouter les VMs utilitaires
Cliquer sur Add

Choisir From Backup

Étape 3 — Sélectionner les VMs nécessaires
Ajouter toutes les VMs indispensables au fonctionnement de l’infrastructure, par exemple :

Serveur DNS

Serveur DHCP

Serveur SQL

Serveur de fichiers

Contrôleurs de domaine

Résultat
Vous disposez maintenant d’un Application Group prêt à l’emploi pour les tests SureBackup.
