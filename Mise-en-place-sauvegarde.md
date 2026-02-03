Mise en place des sauvegardes avec Veeam Backup & Replication
Ce guide détaille les étapes nécessaires pour créer une infrastructure de sauvegarde opérationnelle avec Veeam Backup & Replication, incluant :

La création et la configuration d’un job de backup

La création et la configuration d’un job de SureBackup

1. Création et configuration d’un job de backup
Un job de backup est un plan de sauvegarde automatisé définissant quoi, comment, où et quand Veeam doit sauvegarder les données.
Il constitue l’élément central de toute stratégie de protection dans Veeam Backup & Replication.

Étape 1 — Accéder à la création de job
Ouvrir l’onglet Home

Aller dans Jobs

Clic droit → Backup → Virtual Machine

Étape 2 — Nommer le job
Donner un nom explicite au job

Cliquer sur Next

Étape 3 — Sélectionner les machines virtuelles
Dans Virtual Machines, ajouter les VMs du cluster à sauvegarder

Étape 4 — Choisir le stockage
Sélectionner le repository qui accueillera les sauvegardes

Étape 5 — Paramètres supplémentaires
Ne rien renseigner à cette étape

Étape 6 — Planifier l’exécution
Définir l’horaire de lancement du job

Recommandation : programmer l’exécution en dehors des heures de production

2. Création et configuration d’un job de SureBackup
Une fois le job de backup opérationnel, il est possible de configurer un job de SureBackup, permettant de vérifier automatiquement l’intégrité des sauvegardes via un Virtual Lab.

Étape 1 — Accéder à la création de job
Ouvrir l’onglet Home

Aller dans Jobs

Clic droit → SureBackup

Étape 2 — Nommer le job
Donner un nom explicite au job

Cliquer sur Next

Étape 3 — Sélectionner le Virtual Lab
Choisir le Virtual Lab précédemment créé

Étape 4 — Sélectionner l’Application Group
Choisir l’Application Group configuré auparavant

Étape 5 — Lier la sauvegarde
Cliquer sur Add pour associer le job de backup créé précédemment

Étape 6 — Paramètres supplémentaires
Ne rien renseigner à cette étape

Étape 7 — Planifier l’exécution
Définir l’horaire d’exécution du SureBackup

Comme pour le job de backup, privilégier une période hors production

Conclusion
Vous avez maintenant terminé la mise en place :

d’un job de backup pour protéger les VMs

d’un job de SureBackup pour valider automatiquement l’intégrité des sauvegardes

Cette configuration assure une stratégie de sauvegarde fiable, testée et conforme aux bonnes pratiques Veeam.
