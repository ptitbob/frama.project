# frama.project
####Portage docker des applications framasoft via une exposition docker-compose

> Le but avoué et assumé est de créer un ensemble de container permettant de monter l'ensemble des aplications framasoft dans le cadre de l'opération "*[Dégooglisons Internet](https://degooglisons-internet.org/liste/)*" de permettre leur mise en place sur un serveur ayant docker via la seule commande ```docker-compose``` !

Chaque application est décrite dans son répertoire spécifique portant son nom et  le developpement des container de celle-ci se fait dans la branche portant le nom de l'application (*eh oui, cela va en faire des branches, c'est qu'ils sont prolixe les bougres - pour notre plus grand bien - merci aux maintener*)

En front, un proxy [Træfɪk](https://traefik.io/) permettra l'exposition de chaque application et permettra la redirection (et réécriture d'url) vers les application. 

Donc hors les applications, nous allons mettre (***todo***) les container suivant : 

* Træfɪk (reverse proxy) - ***todo***
  * voir pour une mise en place des certificats [Let’s Encrypt](https://letsencrypt.org/)
* phpmysql (si possible connecté à chaque serveur de base de donnée) ***todo***
* frontal nginx afin de permettre la mise en place d'une *belle page d'acceuil* ***todo***

> Rien ne vous empeche de forker ce projet pour :
* Monter votre propre infrastructure
* Intégrer une autre application framasoft (*pensez à faire une pull request ;)*)

---

##Liste de applications

Liste des applications et des containers les concernant.

* framadate
  * core - serveur apache/php pour l'application
  * mysql - serveur MySQL
