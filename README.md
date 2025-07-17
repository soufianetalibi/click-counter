# Compteur de clics

Petit projet pour tester GitHub. Ce projet affiche un compteur qui s'incrémente à chaque clic sur un bouton.

## Technologies
- HTML
- JavaScript
- Git / GitHub

## Lancer le projet
Ouvrir `index.html` dans votre navigateur.

=================================================================================

click-counter/
│
├── index.html
├── script.js
└── README.md

1-Crée un dossier local click-counter
2-Mets les 3 fichiers ci-dessus dedans
3-Initialise Git :

  git init
  git add .
  git commit -m "Initial commit"

4-Crée un dépôt vide sur GitHub nommé "click-counter"

5-push : 

  git remote add origin https://github.com/ton-nom-utilisateur/click-counter.git
  git push -u origin master
  
  -->si je modifie le contenu d'un fichier et je veux synchroniser vers github : 

  modifier le fichier en local   
  git status
  git add .
  git commit -m "Mise à jour du fichier README.md"
  git push
  
  -->si je n'ai plus le contenu de mon repo en local, je peux faire un pull : 
  git remote -v  (voir le repository distant)
  créer le dossier "click-counter"
  cd click-counter  
  git pull origin master  # (ou master selon ta branche)
  
  -->je peux cloner un répo publique en local : 
  
  git clone https://github.com/octocat/Spoon-Knife.git
  cd Spoon-Knife
  git branch
  git remote -v
  
  =====================================

1.Synchroniser : Local ⇄ GitHub (push, pull)

2.Branches : Travailler sur des fonctionnalités isolées, créer une branche pour chaque nouvelle fonctionnalité, à la fin la fusionner avec la branche main.

3.Collaboration : Travailler à plusieurs, je fais un push et mon collègue fait un pull : git pull origin main

 Réinitialisation locale depuis GitHub
 Tu veux revenir à l’état exact du dépôt GitHub  (perds les modifs locales)
   git fetch origin
   git reset --hard origin/main

git log            # voir les commits
git diff           # voir les différences non commitées
git diff HEAD~1    # voir les changements du dernier commit

7. Créer un tag ou une release

git tag v1.0.0
git push origin v1.0.0

====GitHub Workflows : 

 ou plus précisément GitHub Actions

 permettent d’automatiser des tâches quand quelque chose se passe sur le dépôt GitHub, ex : commit, push, pull request : 

-Compiler ton code

-Lancer des tests

-Déployer sur un serveur

-Créer une release

-Exécuter un script

=========================================


============================
1-Enregistrer mes MAJ sur la branche DEV
2-transférer de la branche DEV vers la branche main puis envoyer la main local vers gitHUB 
3-voir les MAJ sur la gitpage liée à la branche main
=====================================

1-Enregistrer mes MAJ sur la branche DEV

Accéder au dossier ayant les fichiers à transférer.
git init
git remote -v
git remote add origin https://github.com/soufianetalibi/click-counter.git
git remote set-url origin https://github.com/soufianetalibi/click-counter.git
git remote -v
git branch
git checkout DEV
git add .
git status
git commit -m "sauvegarder les MAJ"
git push origin DEV

2-transférer de la branche DEV vers la branche main puis envoyer la main local vers gitHUB

 La merge : 
 git checkout main
 git branch
 git merge DEV (mais c'est local)
 
 transférer la MAJ main du local vers gitHUB: 
 git add . 
 git status
 git commit -m "Mise a jour"
 git push origin main

 ================================================================
 si je perds le dossier en local, je peux retélécharger en local : 

 cd projets
 git clone https://github.com/soufianetalibi/click-counter.git
 cd click-counter
 git checkout DEV

