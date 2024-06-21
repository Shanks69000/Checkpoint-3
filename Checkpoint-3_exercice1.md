# Exercice 1

### Partie 1 : Gestion des utilisateurs
L'utilisateur Kelly Rhameur a quitté l'entreprise.
Elle est remplacée par Lionel Lemarchand

#### Q.1.1.1 Créer l'utilisateur Lionel Lemarchand avec les même attribut de société que Kelly Rhameur.

Pour créer l'utilisateur nous recherchons ou est placer kdans le domaine Kelly Rhameur. Puis, clique droit sur l'ou concerné

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_4.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_6.png)

puis nous rajoutons les mêmes attribut

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_5.png)

ainsi que le même manager et les personnes qu'il managera à la place de Kelly, nous retrouvons la liste des personnes a manager et changeons par Lionel

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_7.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_8.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_9.png)

on peut voir que Kelly ne manage plus

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_10.png)


#### Q.1.1.2 Créer une OU DeactivatedUsers et déplace le compte désactivé de Kelly Rhameur dedans.

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_11.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_12.png)

une fois l'ou créé on clique droit sur Kelly , puis "move" et on choisi l'ou "DesactivedUsers"

Puis clique droit de nouveau et on desactive le compte.
![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_16.png)


#### Q.1.1.3 Modifier le groupe de l'OU dans laquelle était Kelly Rhameur en conséquence.

clique droit sur le groupe dans l'ou direction des ressources humaines, puis on selectionne Kelly et "Remove". et enfin nous faisons "Add" et ajoutons Lionel a sa place

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_14.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_15.png)

#### Q.1.1.4 Créer le dossier Individuel du nouvel utilisateur et archive celui de Kelly Rhameur en le suffixant par -ARCHIVE.

Allons dans le disque "F" pour retrouver les dossiers individuels 

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_18.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-1/Exo1-part1_17.png)

### Partie 2 : Restriction utilisateurs

#### Q.1.2.1 Faire en sorte que l'utilisateur Gabriel Ghul ne puisse se connecter que du lundi au vendredi, de 7h à 17h.

Ouvrir les propriétés de Gabriel Ghul, allons dans l'onglet Account et cliquer sur Logon Hours, sélectionnons les jours et heures autorisées

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_1.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_2.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_3.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_4.png)

#### Q.1.2.2 De même, bloquer sa connexion au seul ordinateur CLIENT01.

Idem dans les propriétés de l'utilisateur dans "Account", "Log ON To";

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_5.png)

#### Q.1.2.3 Mettre en place une stratégie de mot de passe pour durcir les comptes des utilisateurs de l'OU LabUsers.

Ouvrir la console "Group Policy Management", créer une nouvelle GPO(GPO_Password) pour l'OU LabUsers.
Configurons la stratégie de mot de passe (Computer Configuration -> Policies -> Windows Settings -> Security Settings -> Account Policies -> Password Policy)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_6.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_7.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_8.png)

Puis, nous allons modifier la GPO.

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_9.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_10.png)

voici les règles que j'ai choisi.

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-2/eco1-part-2_11.png)

### Partie 3 : Lecteurs réseaux

#### Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.

Suivre les étapes ci-dessous

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_1.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_2.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_3.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_4.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_5.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_6.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_7.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_6.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_8.png)

![](https://github.com/Shanks69000/Checkpoint-3/blob/main/Ressources/exo1-part-3/eco1-part-3_9.png)
