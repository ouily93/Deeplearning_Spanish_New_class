
Dans ce projet nous utilisons un ensemble de données Natural Language Processing   en spagnole.
Ce projet utilise un modèle BERT personnalisé pour la classification de modèles supervisés à utiliser dans une recommandation News des catégories tels que:
macroeconomics;
Sustainability;
Innovation;
Regulations;
Alliances;
Reputati:
Other;

Le modèle  BERT personnalisé est entrainé  et évalué sur  ses performances. Voici les principales étapes et composants :

# Chargement et Prétraitement des Données :

Le dataset Spanish_News est chargé à partir d'un fichier CSV et splité en deux parties. 80% des donnée on permis de faire l'entrainement du modèle.
Les Types que nous avons renomée sentiment sont mappés à des indices numériques.
Les données textuelles de la colonnes News et rénommées review  sont tokenisés en utilisant un tokenizer BERT.


# Définition du Modèle :

Un modèle BERT personnalisé est défini avec une couche de classification finale.
Le modèle utilise les poids pré-entraînés de BERT et ajoute une couche linéaire pour la classification en 7 classe (macroeconomics;Sustainability;Innovation; Regulations; Alliances; Reputati,Other) .

# Étapes d'Entraînement :

La fonction training_step entraîne le modèle sur les données d'entraînement.
La perte est calculée en utilisant CrossEntropyLoss et le modèle est optimisé avec Adam.

# Évaluation :

La fonction evaluation évalue les performances du modèle sur les données de test.
Les prédictions correctes sont comptabilisées et la perte moyenne est calculée.

# Main :

Définit les hyperparamètres et le dispositif de calcul (GPU ou CPU).
Charge les datasets d'entraînement et de test.
Entraîne le modèle et évalue ses performances pour chaque époque.
Sauvegarde le modèle entraîné.

# Phase inférece 
Dans cette phase nous avons utilise gradio afin d'évaluer la  performence du modèle  



## une partie très intéressante devrait être ajouté mais compte tenu du temps nous allons nous limiter sur Gradio 

