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