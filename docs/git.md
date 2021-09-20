# Note pour gérer vos dépots GitHub :

> Ce document a pour objectif de vous accompagner dans la création d'un compte [GitHub](https://github.com/){target="_blank"} et pour sa gestion via différentes solutions...


## Mise en situation :

GitHub en lui-même n’est rien de plus qu’un réseau social comme Facebook ou Flickr. Vous construisez un profil, vous y déposez des projets à partager et vous vous connectez avec d’autres utilisateurs en suivant leurs comptes. Même si la plupart des utilisateurs y déposent des projets de programmes ou de code, rien ne vous empêche d’y placer des textes ou tout type de fichier à présenter dans vos répertoires de projets.

**GitHub** est basé sur **Git**, une création de [Linus Torwald](https://fr.wikipedia.org/wiki/Linus_Torvalds){target="_blank"} qui est l'inventeur du [noyau Linux](https://fr.wikipedia.org/wiki/Noyau_Linux){target="_blank"}. Il en est arrivé à créer [Git](https://fr.wikipedia.org/wiki/Git){target="_blank"} pour justement pouvoir gérer le développement du projet Linux...

Git est un logiciel de contrôle de version, ce qui signifie qu’il gère les modifications d’un projet sans écraser n’importe quelle partie du projet.

Pourquoi utiliser quelque chose comme Git ? Supposons que vous mettiez à jour avec un collègue des pages sur le même site web. Vous faites des modifications, vous les sauvegardez et les versez sur le site. À ce stade, tout va bien. Le problème survient quand votre collègue travaille sur la même page que vous en même temps. L’un de vous va voir son travail écrasé.

Une application de contrôle de version comme Git empêche ça d’arriver. Vous et votre collègue pouvez chacun de votre côté verser vos révisions sur la même page, et Git sauvegardera deux copies. Plus tard, vous pourrez fusionner vos modifications sans perdre le travail dans le processus. Vous pouvez même revenir en arrière à tout moment, parce que Git conserve une « copie instantanée » de tous les changements produits.

Créer un compte sur GitHub.com apporte les contrôles de versions à vos projets numériques, et leur confère des fonctionnalités de réseaux sociaux. Vous pouvez parcourir les projets d’autres utilisateurs de Github, et même y télécharger des copies pour vous-même afin de les modifier, apprendre ou les enrichir. D’autres utilisateurs peuvent faire la même chose avec vos projets publics, repérer vos erreurs et suggérer des corrections. De toute façon, aucune donnée ne se perd parce que Git enregistre un “instantané” de chaque modification.

source : [github-pour-nuls-partie-1](https://www.christopheducamp.com/2013/12/15/github-pour-nuls-partie-1/){target="_blank"}
et [github-pour-nuls-partie-2](https://www.christopheducamp.com/2013/12/16/github-pour-nuls-partie-2/){target="_blank"}

## Créer un dépot GitHub :
Créer un compte sur GitHub (Sign up) depuis un navigateur à l'adresse [https://github.com/](https://github.com/){target="_blank"}, ou identifier vous (Sign in) si vous avez déjà un compte.

<img src="https://ericecmorlaix.github.io/img/GitHub00.png" alt="inscription GitHub" width=30%>

A l'adresse [https://github.com/new](https://github.com/new){target="_blank"} créer un nouveau répertoire de dépot nommé, par exemple `pNomProjet` :

<img src="https://ericecmorlaix.github.io/img/GitHub01.png" alt="nouveau repo GitHub" width=50%>

Cocher la case "Initialize this repository with a README" puis cliquer sur le bouton "Create repository".

Voilà, vous faites maintenant parti d'un autre réseau social mondial celui des développeur de code...

> Remarquer que le fichier `Readme` à pour extension `.md` pour **Mardown** si vous ne connaissez pas ce langage de description rudimentaire rendez-vous sur le bloc-note [Markdown](./MarkDown-Le_BN_pour_rapporter).

Il est possible de gérer un compte GitHub via son interface graphique depuis un navigateur sur un ordinateur personnel comme sur une tablette ou y installant l'application GitHub Desktop adaptée.
Pour vous initier plus complètement dans ce sens https://guides.github.com/activities/hello-world/.

La suite présente le recours à l'interface graphique de Visual Studio Code et *"aux supers pouvoirs"* de **la ligne de commande**...

## Visual Studio Code :

- Télécharger et installer la dernière version de [Visual Studio Code](https://code.visualstudio.com/download) ;

- Dans Visual Studio Code (VSC), cliquer sur le bouton "Contrôle de code source" (1) (`Source Control` ++"Ctrl"+"Maj"+"G"++) ;

![VisualStudioCode.png](images/VisualStudioCodeGit00.png)

- Cliquer sur le bouton "Cloner le dépôt" (2), saisir l'URL du dépôt (3) puis valider (4) ;
- Choisir alors un dossier parent pour recevoir un clone local de votre dépôt distant ;
- apporter des modifications à vos fichiers en utilisant l'éditeur de VSC... ;
- Dans "Changement" (`Changes`) cliquer sur le `+` pour ajouter les fichiers modifiés à indexer dans cette phase (stage) de développement ;
- Ajouter un message sous "CONTROLE DE CODE SOURCE" (`SOURCE CONTROL`) pour définir cette phase de développement puis cliquer sur `✓` pour valider ce commit ;
- Enfin, cliquer sur les `...` et choisir `Push` ;

Votre dépôt sur GitHub devrait se mettre à jour avec vos modifications après quelques temps...

Voir aussi : [https://ericecmorlaix.github.io/mkdocs_tutor/Windows10/](https://ericecmorlaix.github.io/mkdocs_tutor/Windows10/)

## En ligne de commande :

Pour la gestion en ligne de commande, depuis le 13 août 2021, l'identification par simple mot de passe n'est plus supportée, il vous faudra définir une [clef personnelle d'identification](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token).

### Cloner un dépôt :

Sans préciser de nom de dossier ni d'identification :
```bash
$ git clone https://github.com/username/repo.git
```

Avec nom de dossier et identification :
```bash
$ git clone https://github.com/username/repo.git nom_du_dossier_clone
Username: your_username
Password: your_token
```

> Si on ne précise pas le nom du dossier à la fin de l'instruction, alors c'est le nom du dépôt GitHub cloné qui est attribué par défaut au dossier auquel il sera lié.

### Configuration du dossier :

```bash
git config --global user.name "votrePseudoGitHub" # pour limiter la configuration à ce dossier uniquement, enlever le --global
git config --global user.email "prenom.nom@eleves.ecmorlaix.fr" # pour limiter la configuration à ce dossier uniquement, enlever le --global
git config --list # vérifier la configuration du dossier
```

## Récupérer les données actualisées du dépôt GitHub vers votre dossier clone = "Tirer"
```bash
git pull
```

## Vérifier l'état de votre copie de travail :
```bash
git status
```

## Visualiser tous les changements réalisés à ce stade :
```bash
git diff
```
> Les suppresions apparaissent en rouge précédées d'un signe **`-`**, et les ajouts apparaissent en vert prédédés d'un signe **`+`**.

> Utiliser avec la commande `git diff nomDuFichier` pour ne voir que les modifications effectuées sur un fichier 

## Ajouter les changements à mettre à jour à ce stade
```bash
git add nom_du_fichier
```
> La commande `git add *` permet d'ajouter tous les fichiers modifiés en une fois.
> 
> La commande `git add dossier/`permet d'ajouter un dossier et tout sont contenu.
>
> La commande `git reset HEAD -- nomDuFichier` permet d'enlever un fichier ajouté par erreur.
>
> La commande `git checkout nomDuFichier` permet d'annuler les modifications faites sur un fichier depuis l'état précédent.

## Valider et consigner vos modifications = "Commiter"
```bash
git commit -m "message du commit"
```
> La commande `git commit -a -m "mon message"` permet de directement valider et consigner les modifications qui concernent tous les fichiers déjà suivis sans avoir à passer préalablement par une commande `add`.
> 
> La commande `git commit` sans argument ouvre l'éditeur définit par défaut pour permettre d'écrire le message de `commit`...

## Mettre à jour votre dépôt GitHub avec votre copie de travail = "Pousser" :

```bash
git push origin main
```

Voir aussi :

- [Git-Un_BN_pour_gerer_un_depot_GitHub.ipynb](https://nbviewer.jupyter.org/github/ericECmorlaix/1NSI_2020-2021/blob/master/Git-Un_BN_pour_gerer_un_depot_GitHub.ipynb)




 

