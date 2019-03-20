<p align="center">
  <img src="https://www.alsacreations.com/xmedia/doc/original/gulp-bann.png" alt="Gulp-logo">
</p>

</br>

# GulpJS - Workshop par Dylan, Gary, Jérémy et Meroine

## GulpJS, qu'est-ce que c'est ?

Gulp est un task runner, autrement dit un "automatiseur de tâches". Autrement dit, il lance des bouts de scripts à notre place,ce qui va nous permettre de gagner énormément de temps.

Les tâches prises en main par Gulp peuvent être très variées :

- Minifier ou concaténer du CSS ou du Javascript;
- Créer ou supprimer des dossiers ou des fichiers (il peut permettre de créer un projet à partir de zéro);
- L'optimisation et/ou la compression d'images;
- Créer un serveur local  afin de tester notre code sur différents périphériques en même temps;
- Simuler des navigateurs fantômes pour parcourir et tester les régressions d'affichage d'une page.

Afin d'avoir une idée du nombre d'actions possibles avec Gulp, il faut savoir que plus de 2.000 plugins uniques sont recensés à l'heure actuelle, autrement dit autant de tâches exécutables au sein du projet. 

Intégrer Gulp à un projet va donc être significatif d'un énorme gain de temps puisqu'il va nous permettre d'automatiser les tâches répétitives. Il ne restera donc plus qu'à se concentrer sur le principal : produire un code fonctionnel.

## Prérequis et installation
 	
  Pour utiliser gulp vous aurez besoin de Node.js pour l'installer utiliser les commandes suivantes:
	
	```bash
	$ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
	```
	```bash
	$ sudo apt-get install nodejs npm
	```

Une fois que l'installation de Node.js est terminée tapez la commande suivante afin d'installer gulp de manière globale sur votre ordinateur:

	```bash
	$ sudo npm install gulp -g
	```


## Le fichier Gulpfile.js

Le fichier gulpfile.js est le fichier le plus important puisqu'il va s'occuper de gérer les tâches à réaliser, leurs options, leurs sources et destination. En gros, c'est le fichier qui va gérer tout notre projet.

Une tâche Gulp ressemble à ça :

```javascript
gulp.task('css', function () {
  return gulp.src(ici-ma-source)
    /* ici les plugins Gulp à exécuter */
    .pipe(gulp.dest(ici-ma-destination));
});

```

Dans ce bout de code, voici ce qu'il faut retenir :

- **'css'** : le nom que l'on a donné à la tâche;

- **ici-ma-source** : chemin indiquant l'endroit où se trouve le(s) fichier(s) source à traiter;

- **ici-ma-destination** : chemin vers lequel les fichiers seront créés après l'exécution des tâches Gulp.

Nous pouvons maintentenant déclarer toutes les variables dont nous aurons besoin au début de notre fichier gulpfile.js. Ces variables sont celles des plugins, le dossier source et le dossier de destination. Nous allons faire ça de cette manière :

```javascript
// Requis
let gulp = require('gulp');

// Include plugins
let plugins = require('gulp-load-plugins')(); // tous les plugins de package.json

// Variables de chemins
let source = './src'; // dossier de travail
let destination = './dist'; // dossier à livrer
```

## Livecoding

<!-- parler en quelques mots de ce que Gary et Dylan vont présenter -->

## Ressources utiles

- https://gulpjs.com/
