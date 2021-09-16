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

A l'adresse [https://github.com/new](https://github.com/new){target="_blank"} créer un nouveau répertoire de dépot nommé comme votre dossier de travail sur le serveur ou par exemple `pNomRepo` :

<img src="https://ericecmorlaix.github.io/img/GitHub01.png" alt="nouveau repo GitHub" width=50%>

Cocher la case "Initialize this repository with a README" puis cliquer sur le bouton "Create repository".

Voilà, vous faites maintenant parti d'un autre réseau social mondial celui des développeur de code...

> Remarquer que le fichier `Readme` à pour extension `.md` pour **Mardown** si vous ne connaissez pas ce langage de description rudimentaire rendez-vous sur le bloc-note [Markdown](./MarkDown-Le_BN_pour_rapporter).

Il est possible de gérer un compte GitHub via son interface graphique depuis un navigateur ou sur un ordinateur personnel ou une tablette en y installant l'application GitHub Desktop adaptée.
Pour vous initier plus complètement dans ce sens https://guides.github.com/activities/hello-world/.

La suite présente le recours *"aux supers pouvoirs"* de **la ligne de commande** et à l'interface graphique de Visual Studio Code...

Pour la gestion en ligne de commande, depuis le 13 août 2021, l'identification par simple mot de passe n'est plus autorisé, il vous faudra définir une [clef personnelle d'identification](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token).

## Visual Studio Code :

Voir : [https://ericecmorlaix.github.io/mkdocs_tutor/Windows10/](https://ericecmorlaix.github.io/mkdocs_tutor/Windows10/)

## En ligne de commande :

### Cloner un dépôt :

Sans préciser d'identification :
```bash
$ git clone https://github.com/username/repo.git
```

Avec identification :
```bash
$ git clone https://github.com/username/repo.git
Username: your_username
Password: your_token
```
Quelques commande de base :
```bash
git config --global user.name "votrePseudoGitHub" # enlever le global si configuration pour ce dossier uniquement
git config --global user.email "prenom.nom@eleves.ecmorlaix.fr" # enlever le global si configuration pour ce dossier uniquement
git config --list # vérifier la configuration du dossier
```
```bash
git pull
```

```bash
git status
git add *
git commit -m "premier commit"
git push -u origin main
```

Voir aussi :

- [Git-Un_BN_pour_gerer_un_depot_GitHub.ipynb](https://nbviewer.jupyter.org/github/ericECmorlaix/1NSI_2020-2021/blob/master/Git-Un_BN_pour_gerer_un_depot_GitHub.ipynb)




 

