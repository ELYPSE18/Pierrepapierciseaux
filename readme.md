# Les commandes de base de Github

## Première étape

* Créez dans Github, un nouveau repository
* Nommez le comme vous le souhaitez
* Vous pouvez choisir sa visibilité :
    * Public : Si vous souhaitez que tout le monde puisse y avoir accès
    * Private : Si vous souhaitez être le seul à y accéder
* La déscription est optinnelle : remplissez-la si vous le souhaitez
* Allez en bas de page, cliquez sur "Create repository"

Votre repository est maintenant crée, vous allez pouvoir faire votre premier commit

## Faire son premier commit

Vous allez vous rendre compte qu'il y a un petit encadré nommé "Quick setup" qui vous propose deux possibilités : HTTPS et SSH.

Si ce n'est pas fait par défaut, choisissez HHTPS.

### Initialisation de Github sur votre machine

Sur Visual Studio Code : 
* Ouvrez un terminal
 * Ctrl + ù

Initialisez Github sur le dossier qui est ouvert : ``git init``
 
Une fois que git est initialisé, vous allez devoir indiquer quel fichier vous souhaitez envoyer sue Github. Pour cela : 
* ``git add`` Pour ajouter TOUS les fichiers
* ``git add nomDuFichier`` pour ajouter UN fivhier en particulier.

Pour info, vous ne devez PAS entrer vous-meme le nom complet du dossier ou du fichier. Ca augmente le risque d'erreur. Au lieu d'écrire le nom complet vous-mêmes, vous devez écrire seulement la ou le spremières lettres et appuyer sur la touche ``tab``

DAns le cas ou il existe plusieurs fichiers qui commencent avec le smêmes letters, il vous suffit de continuer à appuyer sur ``tab`` jusqu'à arriver au bon fichier.

Si vous avez plusieurs fichiers à ajouter, MAIS que vous ne souhaitez paas ajouter tous les fivhiers qui se trouvent dans votre dossier de travail, vous pouvez faire plusieurs fois ``git add nomDuFichier``

#### En rusumé

* ``git init`` - Pour initialiser le repo github
* `` git add NomDuFichier`` - Pour ajouter un fichier

## Exercice
* Initialisez le repo github sur VSCode
* Ajoutez le fichier readme