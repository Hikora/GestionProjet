# GestionProjet

Le sujet de ce projet était de fournir un outil pour segmenter un format vidéo long format en plusieurs vidéos court format pour alimenter les réseaux sociaux des clients automatiquement .
Nous avons constaté que par Tiktok la consommation des formats vidéos a changé drastiquement et plus généralement les monteurs de cinéma ont aussi besoin d'outils similaires pour repérer les "bonnes prises" .
C'est dans ce but que nous nous sommes lancé dans ce projet .




1) Tout d'abord nous avons dû récupérer le graphique de popularité de chaque vidéo pour ensuite repérer les moments les plus populaires de chaque vidéo .
Après avoir pre-filtrer les points de la vidéo un algorithme de clustering a était employé pour regrouper les points de chacun des moments populaires .


A ce stade nous avons des courts extraits de vidéos (1min30) qui représentent les N moments les plus visionnés .


2) Nous avons récupéré les sous-titres associés à ces N moments, une sélection d'images et le son .


3) Nous avons résumé les sous-titres avec la librairie spacy pour ne garder que les mots-clefs qui seront les futurs taggs de notre format short , nous avons aussi classifié le son en 4 catégories que sont :
[ neutre , content , triste , en colère ] .
 En plus de cela grâce aux méta-données comme la description de la vidéo nous avons récupérer les taggs vers les featuring de la vidéo , le chapitrage ect tout ceci nous servira a mieux  le futur contenu




Une fois l'intégralité des données extraites efficacement et labellisées, nous avons fait une rétrospective de notre travail et nous nous sommes aperçu que pour les très longues vidéos le sampling rate du graphe de popularité était supérieure à 1 min 30 (durée d'un short max ) ainsi il nous a été nécessaire de reconsidérer la stratégie que nous avons adoptée à la partie 1) ( clustering ) .




Pour ce type de vidéo nous devons utiliser le contexte (son , texte , image : partie 2 & 3 ) pour détecter les moments importants entre deux des points du graphe de popularité . La stratégie employée a été de se concentrer sur le son car nous avons remarqué que le fichier audio présenté souvent une discontinuité dans les moments importants ( silence , cris , ect) la simple intensité ne suffit pas toujours en effet bien souvent la discontinuité sémantique ( des mots plus forts : hyperlatif ) est le meilleur moyen pour discriminer ces moments .

Nous avons pu trouver de solution dans le temps imparti pour récupérer et traiter efficacement ces longs moments .




