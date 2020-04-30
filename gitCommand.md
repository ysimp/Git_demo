# Commande Git

## Commande de base
git init : Pour activer un dossier comme repository Git

git add . : pour ajouter  tous les fichiers dans l’index (git add le nom du fichier)

git commit – m "message du commit" : pour commiter en local avec un message du commit

git status : pour voir l’état des fichiers

git log : affiche la liste de tous les commits que vous avez réalisés

git commit -a –m "message du commit" :si vous ne faites que mettre à jour un fichier que vous aviez déjà ajouté à l'index, vous pouvez condenser ces deux étapes de la façon suivante

git checkout SHADuCommit : pour se positionner sur un commit precis (faire un git log pour afficher les commits et le sha)

git checkout master : pour se positionner sur la branche principale 

git revert SHADuCommit : annule le commit specifié c'est dire crée un nouveau commit qui fait l'inverse du précédent, avec la commande suivante.

git commit --amend -m "Votre nouveau message" : modifie simplement le message de votre dernier commit

git reset --hard : Je n'ai pas encore fait mon nouveau commit, mais je veux annuler tous les changements que je n'ai pas encore commités

git clone https://github.com/facebook/react.git : pour cloner un repository

## create a new repository on the command line
echo "# Git_demo" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/ysimp/Git_demo.git
git push -u origin master

## push an existing repository from the command line
git remote add origin https://github.com/ysimp/Git_demo.git
git push -u origin master

## git Pull pour recupérer les modifs des autres
git pull origin master

## Les branches

git branch : pour voir la liste des branches

git branch nouvelle-branche : créer une nouvelle branche du nom nouvelle-branche

git checkout nouvelle-branche : permet de se positionner sur cette branche

Petite astuce pour manipuler vos branches : vous pouvez utiliser la commande 'git checkout -b' pour créer une branche et vous y positionner. Ainsi, au lieu de taper la commande suivante pour créer votre branche :

* git branch ma-branche

puis une deuxième commande pour vous y positionner :

* git checkout ma-branche
 vous pouvez regrouper ces deux opérations en une seule commande : 

* git checkout -b ma-branche