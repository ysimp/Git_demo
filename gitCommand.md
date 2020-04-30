# Commande Git

## Commande de base
 Pour activer un dossier comme repository Git
  - git init

pour ajouter  tous les fichiers dans l’index (git add le nom du fichier)
- git add .

pour commiter en local avec un message du commit
- git commit – m "message du commit" 

pour voir l’état des fichiers
- git status 

affiche la liste de tous les commits que vous avez réalisés
- git log 

git commit -a –m "message du commit" :si vous ne faites que mettre à jour un fichier que vous aviez déjà ajouté à l'index, vous pouvez condenser ces deux étapes de la façon suivante

pour se positionner sur un commit precis (faire un git log pour afficher les commits et le sha)
- git checkout SHADuCommit 

pour se positionner sur la branche principale 
- git checkout master 

annuler un commit specifié c'est dire crée un nouveau commit qui fait l'inverse du précédent, avec la commande suivante.
- git revert SHADuCommit 

modifie simplement le message de votre dernier commit
- git commit --amend -m "Votre nouveau message" 

Je n'ai pas encore fait mon nouveau commit, mais je veux annuler tous les changements que je n'ai pas encore commités
- git reset --hard 

git clone https://github.com/facebook/react.git : pour cloner un repository

## create a new repository on the command line
echo "# Git_demo" >> README.md
* git init
* git add README.md
* git commit -m "first commit"
* git remote add origin https://github.com/ysimp/Git_demo.git
* git push -u origin master

## push an existing repository from the command line
* git remote add origin https://github.com/ysimp/Git_demo.git
* git push -u origin master

## git Pull pour recupérer les modifs des autres
* git pull origin master

## Les branches

pour voir la liste des branches
* git branch 

créer une nouvelle branche du nom nouvelle-branche
* git branch nouvelle-branche 

permet de se positionner sur cette branche
* git checkout nouvelle-branche 

Petite astuce pour manipuler vos branches : vous pouvez utiliser la commande 'git checkout -b' pour créer une branche et vous y positionner. Ainsi, au lieu de taper la commande suivante pour créer votre branche :
* git branch ma-branche
puis une deuxième commande pour vous y positionner :
* git checkout ma-branche
 vous pouvez regrouper ces deux opérations en une seule commande : 
* git checkout -b ma-branche

## Fusionner les branches

Se placer sur master
* git checkout master

ensuite merger avec la branche mon-test
* git merge mon-test
recpercution du contenu de mon-test sur master 

## Retrouvez qui a fait une modification

### Git Blame
Cette commande liste toutes les modifications qui ont été faites sur le fichier ligne par ligne. À chaque modification est associé le début du sha du commit correspondant

exemple :
	416f0e43 (yaya5 2020-04-30 17:21:45 +0200  1) # Commande Git

* git blame nomdufichier.extension

### Pour retrouver pourquoi cette modification a été faite, vous avez deux possibilités : 

Faire un git log et rechercher le commit dont le sha commence par 416f0e43. 

Utiliser la commande git show qui vous renvoie directement les détails du commit recherché en saisissant le début de son sha : 

* git show 416f0e43

les lignes colorées en rouge avec un "-" au debut signifie qu'elles ont été supprimées
et celles en vertes, signifie qu'elles ont été ajoutées