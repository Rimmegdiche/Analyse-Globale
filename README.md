# Analyse-Globale
# Réduction de dimensionnalité et classification des ensembles de données
Ce projet inclut le traitement de deux ensembles de données distinctes. Pour chaque ensemble, les étapes suivantes ont été exécutées : réduction de dimensionnalité, clustering par k-means, et utilisation des clusters comme cibles pour un modèle de régression logistique.

# 2.1 Prétraitement et extraction des composantes principales
Prétraitement des données :

Nettoyage des données pour éliminer ou imputer les valeurs manquantes.
Normalisation des caractéristiques pour que chaque variable contribue équitablement à l'analyse.
Extraction des composantes principales (PCA) :

Application de PCA pour réduire la dimensionnalité des ensembles de données, en identifiant le nombre de composantes principales qui expliquent au moins 85% de la variance totale.
Justification du nombre de composantes retenues basée sur le pourcentage de variance expliquée, permettant ainsi de conserver l'essentiel de l'information tout en particulier le bruit et la complexité des données.
# 2.2 Clustering par k-means
Application de k-means :

Utilisation des données transformées par PCA pour le clustering.
Détermination du nombre optimal de clusters en analysant la courbe de l'inertie pour identifier le "coude", qui suggère le nombre approprié de clusters à retenir.
Justification du choix des clusters :

Analyse de l'inertie qui décrit la somme des distances au carré des points à leur centre de cluster le plus proche. Le point où l'ajout de plus de clusters n'entraîne plus une diminution significative de l'inertie est choisi comme le nombre optimal de clusters.
# 2.3 Utilisation des clusters comme cibles pour la régression logistique
Formation du modèle de régression logistique :

Les étiquettes de cluster obtenues sont utilisées comme variable cible pour entraîner un modèle de régression logistique.
Séparation des données en ensembles d'entraînement et de test pour évaluer la performance du modèle.
Évaluation du modèle :

Le modèle est évalué sur la base de la précision, du rappel, et du score F1 sur l'ensemble de test pour déterminer son efficacité à classer correctement les nouvelles observations selon les clusters déterminés.
