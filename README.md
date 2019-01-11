# En-quete-de-Lumiere
En-Quête de Lumière is a multiplayer video game developed in 2018 by four third year undergraduate students of the French engineering 
school Telecom SudParis. The development of this application was supervised by Denis Conan who shared with us his knowledge and experience
throughout this project period.


The principle of this video game is basic: 4 players and few AIs are in a mansion where a murder is about to happen. 3 of these 4 players 
must find the suspect played by the last player. The 3 investigators can increase their chance of finding the suspect by analyzing the 
behavior of each entity and looking for the clue generated on the map. Of course, each investigator has only one try to stop the suspect.


The purpose of this project was to improve our knowledge of JAVA, and to discover some key concepts for the development of an application. 
Indeed, while developing this application, we faced numerous challenges, including the implementation of a client-server model, the use of 
a physics engine, the design of our video game, the render of our User Interface and the management of AIs. Of course, the development of 
this application was also an opportunity to apply our skills in project management. 

## Disclaimer
Since we developed this game for a French jury, the comments and the documentation of this project are written in French.


# EN'QUETE DE LUMIERE
### Jeu multijoueur en ligne écrit en Java

## Outils utilisés
* Le framework coeur du jeu est [Libgdx](https://libgdx.badlogicgames.com/), c'est un bibliothèque Java
fournissant des outils de bases à la création d'un jeu (rendu, sprite, gestion des inputs, etc ...)
* [Box2D](http://box2d.org/) est un moteur physique pur jeux videos qui permet la gestion des mouvements et des collisions
* [Gdx-AI](https://github.com/libgdx/gdx-ai/wiki) est un extension qui fournit de nombreuses outils pour l'intelligence artificielle (behavior trees, A* pathfinding)
* [Kryonet](https://github.com/EsotericSoftware/kryonet) est une bibliothèque Java fournissant les outils nécessaires à la partie réseau du projet. 

## Mettre en place le projet
Le project fonctionne avec le gestionnaire de dépendance Gradle. Il suffit d'importer un projet Graddle sur Eclipse et de
configurer dans les paramètres d'exécution le dossier `..\PRO3600-18-CON-5\core\assets` en tant que working directory dans l'onglet "argument" afin que Libgdx sache ou chercher les fichiers externes (sprites, cartes, sons, etc ...).
Pour éxécuter le jeu, il faut lancer la classe `Game-desktop.src.com.mygdx.game.desktop.DesktopLauncher`

## Découpage du code
LibGdx fonctionne par "fenêtre" qui sont en réaltion des implémentations de la classe `Screen`, ainsi nous découpons nos
différents tests en différents screen. Pour définir le screen éxécuté, il suffit d'ecrire `setScreen(new NomDuSCreen(this));`dans la classe `gdx.mygdx.game.Game`.
Actuellement, deux fenêtres sont disponibles :
* `PlayScreen` qui est une carte simple avec collision ou un joueur peut se déplacer avec les touches ZQSD.
* `MutliPlayScreen` qui est une carte simple avec collision ou deux joueurs peuvent se déplacer avec les touches ZQSD et les flèches.


