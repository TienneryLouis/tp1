# Answers

Nom : Tiennery
Prénom : Louis

# 1.
Qu'est-ce qu'une instance EC2 ?

Une instance EC2 (pour Elastic Compute Cloud) est un serveur virtuel permettant d'exécuter des commandes, applications sur la plateforme proposée par AWS.

# 2.
Qu'est-ce qu'un VPC ?

VPC tient pour Virtual Private Cloud. Comme son nom l'indique, un VPC permet de fournir un certain niveau d'isolement dans le cloud public afin d'avoir une sphère privée et sécurisée. Il est possible de configurer cette cellule isolée en y intégrant différentes ressources. Des sous-réseaux sont utilisés pour sécuriser les différents VPC entre les utilisateurs. Il est en général complété par un VPN.

# 3.
A quoi sert un NSG ?

# 4.
Quelles sont les 5 propriétés désirables du cloud ?

Le cloud doit être :
- élastique (scalable)
- ouvert
- mutualisé
- on veut pouvoir payer la ressource uniquement lors de son usage
- doit pouvoir être en libre-service

# 5.
Qu'est-ce que l'A/B Testing ?

L'A/B testing consiste à offrir aux utilisateurs deux versions d'un même produit / application (50%/50%).
Différents indicateurs sont mis en place afin de déterminer quelle version conserver.

# 6.
Comment programmer le cloud ?

# 7.
Quelle est la technique pour faire un déploiement sans interruption de service ?

Pour faire un déploiement sans aucune interruption de service, la technique utilisée est celle du Zero Downtime Deployment
Dans un premier temps, on shutdown une partie de l'infrastructure pour faire basculer tout l'infrastructure sur la partie restante, tout en mettant en place la nouvelle version. 
Quand celle-ci est prête, on y fait basculer une partie des utilisateurs quand l'autre est encore sur l'ancienne version. Ensuite, le reste de la nouvelle version se créée quand l'on fait basculer tout le monde dans la nouvelle version, ne pouvant accueillir tout le monde de façon définitive. 
A terme, toute l'infrastructure mise à jour accueille l'ensemble des utilisateurs.

Aucune interruption, juste quelques ralentissement lors des bascules des utilisateurs dans les infrastructures temporaires, fonctionnelles mais pas les plus optimales pour accueillir tout le monde. 


# 8.
Qu'est-ce que le Canary release ?

On place une partie (5%) des utilisateurs sur une nouvelle version quand les 95% restants restent sur l'ancienne. Si tout se passe bien pour les utilisateurs de la nouvelle version au bout d'une certaine période, tous les utilisateurs basculent sur la nouvelle. Le partage des utilisateurs entre les 5% et 95% se fait de façon aléatoire à tous les niveaux de management pour couvrir le plus de types d'utilisateurs possibles lors des tests.

# 9.
Comment changer de taille de machine virtuelle ?

On peut le faire en :
- créant une nouvelle machine virtuelle, plus puissante (amélioration verticale)
- paramétrant une machine pour qu'elle soit scalable avec un intervalle de machines permettant d'adapter la puissance au besoin (défini par l'utilisateur, amélioration horizontale)
- paramétrant une machine virtuelle auto-scalable (amélioration horizontale automatique)

# 10.
Qu'est-ce que le Blue/Green deployment ?

A l'aide d'un système de routeur, il est possible en ayant push une nouvelle version de l'application de faire basculer une partie des utilisateurs sur cette dernière. Cependant, si un problème survient, il est possible de faire un retour immédiat à la version précédente. Ces allers-retours se font jusqu'à ce que la nouvelle version n'ait plus de problèmes, auquel cas tous les utilisateurs basculent sur la nouvelle version.
