
# Notice d’installation sur Windows 64 bits

## Python

Télécharger Python 2.7.10 [https://www.python.org/downloads/](https://www.python.org/downloads/)

Si il y a un problème dans la suite de l’installation avec un message d’erreur « there is a problem with this windows installer package », le problème peut venir de « pip ». Pensez à le désélectionner peut résoudre votre problème.

## Pour editer

Seulment est necessaire de télécharger un des options suivants :

### Visual Studio Code

Télécharger Visual Studio Code [https://code.visualstudio.com/](https://code.visualstudio.com/)

### NotePad++

Télécharger NotePad ++ [https://notepad-plus-plus.org/download/v6.7.8.2.html](https://notepad-plus-plus.org/download/v6.7.8.2.html)

---

## Docker

Docker est une plate-forme logicielle qui vous permet de concevoir, tester et déployer des applications rapidement. Docker vous offre une méthode standard pour l'exécution de votre code. Docker est un système d'exploitation pour conteneurs. Docker vous permet d'envoyer du code plus rapidement, de standardiser les opérations de vos applications, de migrer aisément du code et de faire des économies en améliorant l'utilisation des ressources. 

Télécharger Docker [https://www.docker.com/](https://www.docker.com/)

Guide d'installation de Docker sur Windows : [https://docs.docker.com/desktop/install/windows-install/](https://docs.docker.com/desktop/install/windows-install/)

Guide d'installation de Docker sur Mac : [https://docs.docker.com/desktop/install/mac-install/](https://docs.docker.com/desktop/install/mac-install/)

Guide d'installation de Docker sur Linux : [https://docs.docker.com/desktop/install/linux-install/](https://docs.docker.com/desktop/install/linux-install/)



Docker guides pour aprendre plus de l'utilisation de Docker [https://docs.docker.com/get-started/](https://docs.docker.com/get-started/)

### Lacer le projet avec Docker

```
docker-compose up --build
```

# Bibliothèques Python nécéssaires

### Numpy

http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy choisir le numpy‑1.9.2+mkl‑cp26‑none‑win_amd64.whl

### Scipy
http://www.lfd.uci.edu/~gohlke/pythonlibs/#scipy choisir le scipy‑0.15.1‑cp26‑none‑win_amd64.whl

### Sympy
http://www.sympy.org/fr/index.html

### Bottle
Ecrire  « pip install bottle » directement dans le projet ou faire « wget http://bottlepy.org/bottle.py » dans le dossier du projet.

### Matplolib
http://matplotlib.org/downloads.html et choisir le fichier matplotlib-1.4.3-cp26-none-win_amd64.whl

### XlsxWriter
Ecrire directement dans le projet « sudo pip install XlsxWriter » si cela ne marche pas essayez d’écrire  « sudo easy_install XlsxWriter » dans le code.

### Openpyxl
https://pypi.python.org/pypi/openpyxl

Travail MAJ par le groupe du semestre 2 2015 https://github.com/leosayous21/asses

Aller sur https://assess2.herokuapp.com/ pour voir le rendu du projet

Procédure de lancement

**En local**
```
python website.py local
```

**Sur heroku**

http://assess2.herokuapp.com
Tout se fait automatiquement en important la branche git

# Structure des fichiers

- `static`: Contient les dossiers et fichiers statiques de la web app

    - `css`: Tout ce qui a un rapport avec le design
        - bootstrap.css
        - bootstrap.min.css
        - sb-admin.css
        - sb-admin2.css
    - `fonts`
    - `font-awesome`
    - `img`: Contient les images utilisées dans le site
    - `js`: Les fichiers et fonctions javascript
        - `plugins`
        - `ZeroClipboard`: permet de faire “Copy to clipboard”
        - `bootstrap.js`
        - `boostrap.min.js`
        - `export.js`
        - `jquery-1.11.0.js`
        - `k_calculus.js`: fichier javascript relié au template k_calculus
        - `plot.min.js`
        - `tree.js`: fichier javascript content l’objet tree utilisé pour faire la lotterie
- `views`: fichiers qui sont appelées par website.py lorsque l’on fait une requète du style  http://assess2.herokuapp.com/questions ou http://assess2.herokuapp.com/exports
    - `Attributes.tpl`
    - `blank-page.tp`
    - `exports.tpl`
    - `header_end.tpl`
    - `header_init.tpl`
    - `import.tpl`
    - `js.tpl`
    - `k_calculus.tpl`
    - `questions.tpl`
- `bottle.py`: Ceci est la librairie python permettant de faire tourner le serveur http
- `export_xls.py`: Permet de faire l’exportation au format xls à l’aide de la librairie :
- `fit.py`: Contient la fonction regressions(liste_cord): permettant de renvoyer les fonctions exponentiels, quadratiques, puissance, logarithmique, linéaires à partir d’une liste de points.
- `kcalc.py`
- `methods.py`
- `plot.py`: fichiers permettant de tracer les graphs svg. ll contient la fonction suivante
- `website.py`: Fichier python permettant de connecter les requettes http aux fichiers en question.
- `requirements.txt`: Permet à heroku de connaitre les librairies à installer
