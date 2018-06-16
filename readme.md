Ce projet a été développé au cours du hackathon Datafin 2018.
Un fil des ressources de l'équipe est disponible ici : (https://forum.datafin.fr/t/etude-des-projets-de-loi-de-finance-dans-le-temps/247/5)[https://forum.datafin.fr/t/etude-des-projets-de-loi-de-finance-dans-le-temps/247/5]

Ce projet a pour but initial de comparer deux nomenclatures successives du Projet de Loi de Finance français.
Le cadre d'application est cependant plus large : il s'agit, étant donnés deux graphes A et B, de former des associations de noeuds entre ces deux graphes.

La difficulté du problème vient de plusieurs points :
* plusieurs noeuds de A peuvent être associés à un même point de B, et vice-versa
* il est possible qu'un noeud de A ne soit associé à aucun noeud de B (à dessin), et vice-versa

Ce repo contient un notebook Jupyter en Python 3.5 qui crée des paires de noeuds de la façon suivante :
* pour chacun des deux graphes, on construit pour chaque noeud une représentation (un embedding) de son intitulé
* pour chaque noeud du graphe A, on calcule les k noeuds les plus proches dans le graphe B
* pour chaque noeud du graphe B, on calcule les k noeuds les plus proches dans le graphe A
* on sélectionne parmi les paires ainsi générées celles qu'il faut conserver (TODO)

Nous utilisons des FastText et des embeddings pré-entrainés disponibles ici : (https://s3-us-west-1.amazonaws.com/fasttext-vectors/wiki.fr.vec)[https://s3-us-west-1.amazonaws.com/fasttext-vectors/wiki.fr.vec]
