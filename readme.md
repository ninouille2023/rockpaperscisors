# Les commandes de bases de GitHub
Readme.md : fichier de base qui s'envoi sur GitHub et s'affiche sous le repository GitHub

## Première étape

* Créer dans Github, un nouveau repository
* Nommez le comme vous le souhaitez
* Vous pouvez choisir sa visibilité :
    * Public : Si vous souhaitez que tout le monde puisse y avoir accès
    * Private : Si vous souhaitez être le seul à y accéder
* La description est optionnelle : remplissez-la si vous le souhaitez
* Allez en bas de page, cliquez sur "Create repository"

Votre repository est maintenant créé, vous allez pouvoir faire votre premier commit.

## Faire son premier commit

Vous allez vous rendre compte qu'il y a un petit encadré nommé "Quick setup" qui propose 2 possibilités : HTTPS et SSH.

Si ce n'est pas encore fait par défaut, choisissez HTTPS.

### Initialisation de Github sur votre machine

Sur Visual Studio Code : 
* Ouvrez un terminal (3 ossibilités)
* CTRL + ù
* En bas à gauche, vous avez une icone triangle et rond. Cliquez dessus

Initialisez github sur le dossier qui est ouvert : 
``git init``
Une fois que github est initialisé, vous allez devoir indiquer quel(s) fichier(s) vous souhaitez envoyer sur github. Pour cela :
* ``git add *`` : pour ajouter TOUS les fichiers
* ``git add nomFichier`` : pour ajouter un fichier en particulier

Pour info, vous ne devez pas rentrer vous-même le nom complet du dossier ou du fichier. Cela augmente le risque d'erreur. Au lieu d'écrire le nom complet vous-mêmes, vous devez écrire seulement la ou les premières lettres et appuyer sur la touche ``tab``.

Dans le cas où il existe plusieurs fichiers qui commencent avec les mêmes lettres, il vous suffit de continuer à appuyer sur ``tab`` jusqu'à arriver au bon fichier.

Si vous avez plusieurs fichiers à ajouter mais que vous ne souhaitez pas ajouter tous les fichiers qui se trouvent dans votre dossier de travail, vous poouvez faire plusieurs fois ``git add nomFichier``.

#### En résumé

* ``git init`` : pour initialiser le repo
* ``git add nomFichier`` : pour ajouter un fichier

## Exercice
* Initialiser le repo github sur VSCode
* Ajouter le fichier readme

### Faire la liaison avec le repo distant
Vous venez d'initialiser git sur votre machine mais il ne sait pas encore qu'il doit être lié à votre repository distant
Pour cela vous allez devoir connecter l'origine à votre repository à votre repository distant

Commançons par ajouter un petit message qui précise ce qu'on a fait comme modification/ajout/suppression

* ``git commit -m "explication du commit"`` 

Exemple :
* ``git commit -m "Ajout du fichier readme"``

Une fois que le message de commit est définit, on va choisir la branche sur laquelle on va travailler.

Lorsue vous souhaitez stocker vos fichiers sur github si vous le souhaitez vous pouves stocker differentes versions de vos fichiers cela s'appelle des branches.

* ``git branch -m main``

on selectionne la branche "main"

on connecte le lien de repo local machine a githup avec cette commmande

* ``git remote add origin LIEN_DE_VOTRE_REPO``

exemple :
* ``git remote add origin https://github.com/JackAdamsJenkins/rockpaperscisors.git``

maintenant que c'est connecté, il faut envoyer les fichiers sur github avec la commande ``git push -u origin main``

## En résumé

Voici les commandes à lancer : 
* ``git init`` : initialiser le repo github
* ``git add NomFichier`` : ajouter un fichier
* ``git commit -m "Nom du commit`` : ajouter une description de la modif
* ``git branch -m main`` : choisir la branche principale
* ``git remote add origin URL_REPO_GITHUB`` : connecter le repo local et distant
* ``git push -u origin main`` : envoyer les modifications à github

## Informations

Les commandes ``git init``, ``git branch`` et ``git remot add origin`` : sont à lancer UNE SEULE FOIS au moment de l'initialisation du repo.

Une fois que ces commandes ont été faites, pendant le reste du développement de votre projet, vous pouvez utiliser les commandes suivantes : 
* ``git add NomFichierModifié``, ``git commit -m "Message de modification"``, ``git push``.

C'est ces 3 commandes que vous réutiliserez à chaque fois :
* ``git add NomFichierModifié``
* ``git commit -m "Message de modification"``
* ``git push``










