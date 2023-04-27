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
### Pile de technologie
- Python, notebook
- Tensorflow, Keras, OpenCV

## Resultats
Apres avoir forme les modeles , nous obtenues les resultats suivants. 
### Entrainement a partir de Zero
### Apprentissage par transfert
Nous observons une croissance exponentielle de la precision au debut de la formation puis elle se stabilise du 8e epochs, le modele a donc bien appris.
Nous avons obtenu globalement un **f1-score** de **97 %** . Nous acceptons ce modele car sa performance est grandement significative ( > **95 %**)
### Predictions en temps reel
Notre modele a atteint des perfomances de prediction impressionnantes ou, dans la plupart des cas, des predictions precises ont ete faites et soutenues par un taux de confiance significatif (> **90 %**). Il faut noter que le modele a reussi a distinguer meme les gestes les plus similaires tels que "A" avec "E" et "S" , "U" avec "V" et "W"
## Conclusion et perspectives
- En conclusion , nous avons pu creer un systeme de reconnaissance de l'alphabet **LSA** a l'aide de ResNet-50 preforme de la bibliotheque **Keras** et mettre en oeuvre la prediction en temps reel avec **OpenCV**. Le systeme arrive a une precision de **97 %%**.
- Les projets impliquant des images peuvent etre fortement affectes par de nombreux facteurs tels que la distance de l'objet (la main dans ce projet) et la resolution/luminoisite de l'image capturee a partir de la video en direct. Afin de gerer les facteurs comme les objets se trouvant dans l'image affectant la prediction, nous conseillons de combiner ce modele avec un modele de detection d'objets comme **YOLO**

Nous esperons que ce projet constituera la base pour les futurs projets traitant de la langue des signes.

## Contributeurs
Tous les contributeurs @seriamedard, @
