# Arbalet 127 Snap

Ce dépôt contient un serveur Python qui permet de programmer `Arbalet 127` à partir de plusieurs ordinateurs clients connectés sur le même réseau Wifi qu'Arbalet 127.

## Installation du serveur
* Télécharger (clôner) le dépôt et décompresser
* Ouvrir un terminal puis se placer dans le dossier contenant `setup.py`
* Taper `python setup.py install` (Sous Linux préfixer avec `sudo` pour installer sur le système)
* Si l'installation n'indique aucune erreur, démarrer le serveur en tapant `python -m arbalet.frontage.snap`
* Une simulation doit démarrer mais les pixels restent noirs ... il faut maintenant les programmer avec un client Snap

## Installation du client
Bonne nouvelle, Snap fonctionne dans un navigateur Web et il n'y a donc rien à installer sur le client.

Il suffit de cliquer sur ce lien : [Snap pour Arbalet](http://snap.berkeley.edu/snapsource/snap.html#present:Username=yoan&ProjectName=arbalet&editMode)
Une simulation des pixels est affichée à droite en dessous du nom aléatoire qui a été attribué à ce client. Le programme de l'utilisateur s'affiche au milieu, il contient deux blocs qui affichent des couleurs aléatoires sur les pixels. En cliquant sur "When I am clicked" le bloc se met en surbrillance et s'exécute : on voit alors la simulation à droite s'allumer de façon aléatoire.

Si la simulation du serveur est toujours ouverte, elle reste toujours noir tandis que la simulation du client s'anime. C'est normal, car cette seconde simulation est le reflet du vrai mur Arbalet. Pour que ce client la contrôle, l'administrateur doit autoriser ce client à prendre le contrôle du mur.

Pour ce faire charger l'[interface d'administration](http://127.0.0.1:33450/admin). Une liste s'affiche avec le nom des clients connectés (il n'y en a qu'un normalement à cette étape). Il suffit de sléectionner le client souhaité pour qu'il prenne le contrôle du mur à partir de son programme Snap.

Note : dans le navigateur, s'il y a plusieurs onglets ouverts et qu'un onglet différent de Snap est sélectionné, alors le programme Snap cesse de mettre à jour les pixels, il ne reprend que lorsque l'onglet Snap est à nouveau celui sélectionné.
