# qrcodes

  Il s’agit de développer une application basée sur le scanning de QR Code pour de la
vente automatisée.
il s’agit de pouvoir scanner des QR Codes soi-même sur des produits physiques dans un
magasin au fur et à mesure qu’on les collecte en rayon, et passer au paiement de son
panier depuis la même application avant de quitter le magasin.
On créera quelques produits sur un back-end Symfony ainsi qu’un système simple
d’utilisateurs, de manière à pouvoir se créer un compte et disposer d’un panier dans
lequel on pourra mettre des produits, dans le but de pouvoir simuler ensuite un
paiement. Les produits auront un nom, un prix, optionnellement une image, et ont les
créera directement sur l’application Symfony dans le back-oce (desktop).
L’application de front-end sera soit simplement en web à utiliser depuis l’explorateur
web mobile (framework au choix : Vue, Angular, React), soit basée sur Expo avec React
Native. Elle permettra à l’utilisateur de se connecter (via JWT) et de scanner les QR
Codes des produits avec l’appareil photo du téléphone. Chaque produit scanné sera
ajouté au panier, et on simulera une fonctionnalité de paiement qui videra le panier et
enregistrera la commande du client en tant que payée. L’application devra pouvoir
acher l’historique des commandes et de leurs produits, et le back oce devra
permettre d’acher également l’historique de toutes les commandes, en cas de
contrôle physique de panier en sortie de magasin.
Il nous faudra donc préparer des QR Codes associés au produits pour avoir de la
matière. Le back oce sur Symfony doit donc être en mesure de générer un QR Code
pour chaque produit et de les imprimer sur papier (simple export PDF, ou page web à
imprimer) de manière à ce que vous puissiez en imprimer quelques-uns à l’école pour
pouvoir les scanner avec l’application de front-end. (Si problème technique
d’impression, il est toujours possible d’acher les QR codes sur l’écran d’un autre
ordinateur pour remplacer le papier)
Le flow de l’application de front-end pourra ainsi être testé en temps réel au fur et à
mesure de son développement : il faudra pouvoir se connecter à son compte avec son
identifiant et mot de passe pour obtenir un JWT, et pouvoir scanner les QR Codes
imprimés pour automatiquement remplir son panier, et ensuite passer au paiement
(simulé) . Également, on devra pouvoir y consulter l’historique de ses commandes.
Partie Creative Coding :
En utilisant la librairie Three.JS, il vous faudra intégrer deux animations de votre choix à
l’application :
-La première est l’animation de chargement au lancement de l’application/premiere
ouverture de la page web
-La seconde se déclenchera sur la validation/le paiement confirmé d’un panier.
Elles devront toutes deux être équilibrées par rapport à la page (taille et ton de
couleurs) et ne devront pas durer plus de quelques secondes (1,5 à 4 secondes
idéalement)
Les modèles 3D peuvent être de votre propre conception (Spline, etc) ou encore venir
d’une des bibliothèques d’objets 3D libres de droit, attention à la compatibilité des
formats avec Three.JS
Pour résumer les fonctionnalités :
Back end (Symfony + PostGRESQL) :
-Connexion en tant qu’admin
-ajout de produits
-génération de QR Codes
-export des QR Codes pour impression*
-historiques des commandes payées pour vérification des achats à la sortie du
magasin
Front-end (En web avec Vue, React ou Angular, ou Expo et React Native)
-Se connecter / s’enregistrer
-scanner un produit pour l’ajouter au panier
-payer son panier (paiement simulé)
-acher son historique de commandes
-animations de chargement et de validation/paiement de panier
Rendu : Dépot Github + Dépot Gitlab
Back End déployé et lié à un nom de domaine
Front-end : Déployé et lié a un nom de domaine si WEB, export Android si Expo
Ressources
