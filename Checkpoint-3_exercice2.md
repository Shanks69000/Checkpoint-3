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

#### Q.2.3.2 Quel type de système de stockage ils utilisent ?

#### Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID

#### Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.

#### Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?
