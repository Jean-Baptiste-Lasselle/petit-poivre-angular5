# Cuisine

Ce repository versionne le client angular 5, de [l'application petit-poivre-jee](https://github.com/Jean-Baptiste-Lasselle/petit-poivre-jee)

Il sert à tester [le petit-duc-mvn-plugin](https://github.com/Jean-Baptiste-Lasselle/petit-duc-mvn-plugin)

mais avant de créer ma propre application Angular 5, je vais en utilsier une autre, présente sur le repository:

https://github.com/KrunalLathiya/Angular5CRUD

cette application est censée être le résultat du tutoriel suivant:

https://appdividend.com/2018/01/21/angular-5-crud-tutorial-example-scratch/

L'intéressant est qu'il met en oeuvre mongodb pour la persistance.

l'entier code source de l'application est présent dans le répertoire `./exemple` du présent repository GIt.




Cette application est l'un des composants d'une expérimentation mettant en jeu:
* une application jee web, avec client angular 5, et base de données mongodb:
  * la partie Java de l'application est versionnée par le repository [petit-poivre-jee](https://github.com/Jean-Baptiste-Lasselle/petit-poivre-jee)
  * la partie Java de l'application est versionnée par le repository [petit-poivre-angular5](https://github.com/Jean-Baptiste-Lasselle/petit-poivre-angular5)
* un plugin maven à la vue perçante [petit-duc-mvn-plugin](https://github.com/Jean-Baptiste-Lasselle/petit-duc-mvn-plugin)
* une recette de provision d'une cible de déploiement tomcat / mongodb "dockerisée",  versionnée par le repository [petit-poivre-cible-deploiement](https://github.com/Jean-Baptiste-Lasselle/cible-deploiement-petit-poivre)


Le but de l'expérimentation est de proposer un processus de développement, et les outils qui permettent de le mettre en oeuvre, pour deux 
équipes séparées géographiquement et/ou technologiquement, et travaillant sur la même application.

L'intention est de chercher comment une équipe technique peut faire du pilote de projet 
un homme aux 5 sens augmentés.


# Architecture de l'application

On met en oeuvre des "Endpoints" de REST API, compatibles JAX-RS,  
Cette recette de déploiement permet de monter une cible de déploiement:
* conteneur docker Tomcat
* conteneur docker mongodb

Les conteneurs peuvent:
* être démarrés individuellement, avec support du CHECK_HEALTH
* être démarré et orchestrés par docker-compose (cf. fichier docker-compose.yml)
<!-- * À venir: être démarrés et orchestrés par Kubernetes -->







