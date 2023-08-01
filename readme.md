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

# Ecrire un bon message de commit

Ecrire un bon message de commit est essentiel pour la maintenance et la compréhension d'un projet. Cela aide à suivre l'évolution du projet et à comprendre les raisons derrière chaque modification.

Voici une norme généralement acceptée pour rédiger des messages de commit.

## Structure d'un message de commit

Un message de commit se compose généralement de 2 parties :

* Un titre (ou en-tête) : C'est une brêve description des modifs. Il doit être concis et ne pas dépasser les 50 caractères. Il doit commencer par une majuscule.
* Un coprs : Il donne des détails supplémentaires sur les modifications. Il est séparé du titre par une ligne blanche.

```
Titre court et descriptif

Corps du message : ici, on explique en détail le pourquioi et le comment
des changements si nécessaire. Essayez de garder chaque ligne à moins
de 72 caractères.
```

```
git commit -m "Titre [ne pas fermer les "" pour passer à la ligne]
[saut de ligne]
Corps du message
Deuxième ligne du message"  [fermer les "" à la fin]
```

## Conseil pour un bon message de commit

* Utiliser l'impératif : le titre doit idéalement être écrit à l'impératif (ex: ajoute, corrige, refactorise au lieu de ajouter, corriger, factoriser)

* Titre clair et concis : doit être court et descriptif
* Séparer les sujets : si vous avez plusieurs modifications qui n'ont pas de rapport entre elles, envisagez de les séparer en plusieurs commits
* Expliquez le pourquoi, pas le comment : le code lui-même montre comment une certaine chose a été faite. Ce qui n'est pas clair, c'est pourquoi cette modification a été apportée.
* Evitez les messages vagues : "Corrections diverses", "Mise à jour" ne sont pas des messages utiles. Soyez aussi descriptif que possible.
* Utiliser des références aux issues/tracker : si votre commit fait référence à une issue ou un ticket, ajoutez cette référence dans le corps du message.
* Respecter les coventions de l'équipe : si votre équipe a des conventions spécifiques pour les messages de commit, suivez-les.

### Exemple d'un bon message de commit

```
Ajoute une fonctionnalité de recherche

La page d'accueil avait besoin d'une fonctionnalité de recherche pour aider les utilisateurs à trouver des contenus spécifiques.
Cette modification ajoute un moteur de recherche et utilise l'API de recherche pour récupérer les resultats.

Relatif à l'issue #123.
```
# En savoir plus sur le langage markdown

Pour la rédaction de vos fichiers Readme, n'hésitez pas à vous pencher sur la documentation markdown. Voici un lien pour vous aider :
[Lien pour vous apprendre le markdown](https://programminghistorian.org/fr/lecons/debuter-avec-markdown)




### Tegmelko was here ~



