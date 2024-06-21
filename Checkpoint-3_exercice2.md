# Exercice 2

## Exercice 2 : Manipulations pratiques sur VM Linux (temps estimé : 2h30)


### Partie 1 : Gestion des utilisateurs

#### Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-1/exo2-part-1_1.png)

#### Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?

- Je préconise l'utilisation d'un mot de passe fort comme au moins 8 caractères avec une complexité, comme au moins une majuscule, un minuscules, chiffres et des symboles.
- Des privilèges limités, pour ne pas risquer des erreurs fatals. Exemple la suppression d'un dossier important.

### Partie 2 : Configuration de SSH

#### Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.

Nous allons dans le dossier "/etc/ssh/sshd_config"

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-2/exo2-part-2_1.png)

Puis, rajoutons la ligne 

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-2/exo2-part-2_2.png)

#### Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-2/exo2-part-2_3.png)

#### Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-2/exo2-part-2_4.png)

Et enfin nous redémarrons le service sshd pour prendre en compte les changements

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-2/exo2-part-2_5.png)

### Partie 3 : Analyse du stockage

#### Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?



![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-2_1.png)

#### Q.2.3.2 Quel type de système de stockage ils utilisent ?

Le type de stockage actuel est le "raid" et "lvm"

#### Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID

Nous allons dans virtualbox, selectionnons la vm, ensuite sur configuration et nous suivons les etapes en dessous

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-2_2.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-2_3.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-2_4.png)

On peut voir les deux disques.

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-2_5.png)

on vérifie avec "lsblk"

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-3_6.png)

On partitionne le disk sdb avec la commande ci-dessous. Et on utilise les option "n" nouvelle partition, "p" pour partition primaire. Puis on valide le reste par defaut et w a la fin pour écrire les modifications.

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-3_7.png)

On verifie "lsblk"

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-3_8.png)

ensuite j'ajoute  au raid 

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-3_9.png)

On vérifie que c'est activé et qu'il y a les deux "UU" 

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-3_11.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo2-part-3/exo2-part-3_10.png)

#### Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.

#### Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?

### Partie 4 : Sauvegardes

#### Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM.

### Partie 5 : Filtrage et analyse réseau

#### Q.2.5.1 Quelles sont actuellement les règles appliquées sur Netfilter ?

#### Q.2.5.2 Quels types de communications sont autorisées ?

#### Q.2.5.3 Quels types sont interdit ?

#### Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.

### Partie 6 : Analyse de logs

#### Q.2.6.1 Lister les 10 derniers échecs de connexion ayant eu lieu sur le serveur en indiquant pour chacun :

La date et l'heure de la tentative
L'adresse IP de la machine ayant fait la tentative
