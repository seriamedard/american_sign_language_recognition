# Reconnaisance de l'alphabet en langue des signes americaines a l'aide de Resnet50V2

## Contexte
Nous constatons que l'intelligence artificielle existe pour aider a resoudre des problemes, pourtant elle est aussi connue pour etre biaise contre les personnes marginalisees comme les malentendantes. C'est pourquoi dans ce projet, nous avons developpe un programme en utulisant **Resnet** (reseau neuronal artificiel qui permet de resoudre le probleme de disparition du gradient.) pour transcrire la langue des signes americaines en langue ecrite.

## Objectifs
- Developper un modele d'apprentissage automatique pour transcrire les signaux manuels des alphabets avec un haut niveau d'adabtabilite a divers endroits;
- Obtenir une performance globale permettant la prediction en temps reel et qui distingue les gestes similaires tels que "A" avec "E", "M" et "S";
- Comparer l'apprentissage a partir de Zero et l'apprentissage par transfert

## Methodologie
Nous avons developper notre modele avec *python* en utilisant la bibliotheque *Keras* et demontrer en temps reel avec *OpenCV*.
- **Dataset**
Les donnees utulisees proviennent de [Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet), ce sont **87 000** images de taille **200 x 200** que nous avons redimentionnees a (64 x 64) pour un compromis avec la puissance de calcul que l'on dispose.
- **Modeles**
Nous avons utilise l'implementation du Resnet50V2 pour former notre modele a partir de Zero sur le dataset, puis nous l'avons comparee au modele preforme a adapter a notre tache ( apprentissage par transfert)

## Resultats


