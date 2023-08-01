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

### Faire la liaison avec le repo distant
Vous venez d'initialiser git sur votre machine, mais il ne sait pas encore qu'il doit être lié à votre repository distant.
Pouer cela, vous allez devoir connecter l'origine à votre repository distant.

Commençons par ajouter un petit message qui précise ce qu'on a fait comme modification/ajout/suppression

* ``git commit -m "explicationdu commit"``
exemple : 
* ``git commit -m "ajout du fichier readme``

Une fois que le message de commit est défini, on va choisir la branche sur laquelle on va travailler.

Lorsque vous souhaitez stocker vos fichier sur github, si vous le souhaitez, vous pouvez stocker différentes versions de vos fichiers. Cela s'appelle des branches.
La branche principale sur laquelle vos fichiers sont enregistrés s'appelle "main".

* ``git branch -m main``

Cette commande indique qu'on selectionne la branche "main".

Il est maintenant temps de connecter votre repo local (votre machine) à votre repo distant (github). Pour cela, utilisez cette commande : 
* ``git remote add origin LIEN_DE_VOTRE_REPO``

Exemple : 
* ``git remote add origin https://github.JackAdamsJenkins/rockpaperscisors.git``

Maintenant que le repo local et distant sont connectés, il vous reste à envoyer vos fichiers sur github. Cela se fait avec la commande ``git push -u origin main``

## En résumé
Voici le scommandes a lancer :
* ``git init`` pour initialiser le repo github
* ``git add NomDuFichier`` pour ajouter un fichier
* ``git commit -m "Nom du commit`` pour ajouter une description de al modification/ajout
* ``git branch -m mian`` pour choisir la branche principale
* ``git remote add origin URL_REPO_GITHUB`` pour connecter repo local et distant
* ``git push -u origin main`` pour envoyer les modifications à github

## Information :
Les commandes ``github init``, ``git branch`` et ``git remote``, ``add origin`` sont à lacer UNE SEULE FOIS au moment de l'initialisation du repo.

Une fois que ces commandes ont été faites, pendant  le reste du développement de votre projet, vous pouvez utiliser les commandes suivantes : ``git commit -m "message de modification"``, ``git add NomDuFichierModifié``, ``git push``.

Cest ces trois commandes que vous utiliserez à chaque fois :
* ``git add NmDuFichierModifié"``
* ``git commit -m "message de modification"``
* ``git push``

# Ecrire un bon message de commit
Ecrire un bon message de commit est essentiel pour la maintenance et la compréhension d'un projet. Cela aide à suivre l'évolution du projet et à comprendre les raisons derrière chaque modification.

Voici une norme généralement accéptée pour rediriger des messages de commit.

## Structure d'un message de commit
Un message de commit se compose généralement de deux parties :
* Un titre (ou en-tête) : C'est une brève description des modifications. Il doit être conci et ne pas dépasser les 50 caractères. Il doit commencer par une majuscule.
* Un corps : Il donne des détails supplémentaires sur les modifications. Il est séparé du titre par une ligne blanche.

```
Titre court et description

Corps du message : ici, on explique en détail le pourquoi et comment des changements si nécessaire. Essayez de garder chaque lignes à moins de 72 caractères.
```

## Conseils pour un bon mesage de commit
* Utilisez l'impératif : Le titre doit idéalement être écrit à la voix impérative (ex. Ajoute, Corrige, Refactorise au lieu de Ajouté, Corrigé)
* Titre clair et concis : Doit être  court et descriptif
* Séparez les sujets : Si vous avez plusieurs modifications qui n'ont pas de rapport entre elles, envisagez de les séparer en plusieurs commits
* Expliquer le pourquoi, pas le comment : Le code lui-même montre comment une certaine chose a été faite. Ce qui n'est pas toujours clair, c'est pourquoi cette modification a été apportée. Assurez-vous d'expliquer les raisons dans le corps du message.
* Evitez les messages vagues : "Corrections diverses" ou "Mises à jour" ne sont PAS des messages utiles. Soyez aussi descriptif que possible.
* Utilisez des références ausx issues/tracker : Si votre commit fait référence à une issue ou à un ticket, ajoutez cette référence dans le corp du message.
* Respectez les conventions de l'équipe : Si votre équipe a des conventions spécifiques pour les messages de commit, suivez-les.

### Exemple d'un bon message de commit
```
Ajoute une fonctionnalité de recherche

La page d'accueil avait besoin d'une fonctionnalité de recherche pour aider les utilisateurs à trouver des contenus spécifiques.
Cette modification ajoute un moteur de recherche et utilise l'API de recherche pour les résultats.
Relatif à l'issue #123.
```
# En savoir plus sur le langage markdown
Pour la rédaction de vos fichiers Readme, n'hésitez pas à vous pencher sur la documentation markdown. Voici un lien pour vous aider :
[Lien pour apprendre le markdown](https://programminghistorian.org/fr/lecons/debuter-avec-markdown)

![Texte associé à l'image](pierre.gif)

# Pull request (Pr)

C'est une fonctionnalité clé des systemes de gestion de version bassées sur Github, gitLab, Bitbucket..
Elle represente une demande de fusion des modificatons (commits) d'une branche vers une autre, généralement de la branche d'une fonctionnalité vers la branche principale d'un projet.

## Concept de  la Pull Request (PR)

Collaboration et revue de code : La Pr n'est pas seulement un mécanisque de fusion de code. c'est aussi un outil de collaboration. Lorsqu'un développeur soumet un PR, d'autres membres de l'équipe peuvent la consulter, laisser des commentaires, suggérer des modifications et même proposer des commits pour améliorer la PR avant qu'elle ne soit fusionnée.

**Point de contrôle :** Avaant la fusion, la PR fournit un point de contrôle pour s'assurer que le code respsecte les nombres de qulité, passe tous les tests et n'introduit pas de régressions.

**Intégration avec CI/CD :** Les pull sont souvent intégrées avec des outils d'intégration continue et de livraison continue (CI/CD). Lorsqu'une pr est soumise, des tests automatisés peuvent être declenchés, et le résultat de ces tests est souvent signalé directement dans l'interface de la PR.

## Faire une pull request
## Fork du repository
Avant de pouvoir  soumettre une PR, vous devez avoir une copie du repository sur votre compte. Si ce n'est pas déja fait :

1. Rendez-vous sur la page Github du projet auquel vous voulez contribuer.
2. Cliquez sur le bouton "Fork" en haut à droite de la page. Cela créera une copie du projet sur votre compte Github personnel.

## Clonez votre Fork
Clonez votre fork sur votre machine : 
```
git clone URL_DU_REPO_A_CLONER
git clone https://github.com/ELYPSE18/Pierrepapierciseaux
```

## Créez une nouvelle branche
Il est conseillé de créer une nouvelle branche pour chaque nouvelle fonctionnalité ou correction. Cela vous permet de garder le travail organisé et séparé.

Pour créer une nouvelle branche , vous devez utiliser la commande ``git checkout -b``

```
git checkout -b nom_de_la_brache
git checkout -b fonctionnalite_timer
```

## Apportez les modifications
MOdifiez le fichiers nécessaires et ajoutes les à l'index : 
```
git add nom_du_fichier
```
ou pour ajouter tous les fichiers modifiés :
```
git add
```
Ensuite, faites un commit de vos modifications"
```
git commit -m "Description des modifications"
```
## Pousser la branche vers le fork
```
git push origin nom_de_la_branche
```
## Créez le pull request
1. Allez sur la page github de votre fork
2. Cliquez sur le bouton "New pull request"
3. Séléctionnez votre nouvelle branche dans le menu déroulant "compare"
4. Assurez-vous que la branche de base (**main**) est celle du projet original et non celle du projet original et non celle de votre fork
5. Vérifiez vos modifications et cliquez sur "Creat pull request"
6. Donnez un titre à votre PR et décrivez vos modifications ou les raisons de votre PR
7. Cliquez sur "Create pull request" pour soumettre votre pr
