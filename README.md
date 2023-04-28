# Reconnaissance de l'alphabet en langue des signes américaine a l'aide de Resnet50V2

## Contexte
Nous constatons que l'intelligence artificielle existe pour aider à résoudre des problèmes, pourtant elle est aussi connue pour être biaisée contre les personnes marginalisées comme les malentendantes. C'est pourquoi dans ce projet, nous avons developpé un programme en utilisant **Resnet (réseau neuronal artificiel qui permet de résoudre le problème de disparition du gradient.) pour transcrire la langue des signes americaine en langue ecrite.

## Objectifs
- Développer un modèle d'apprentissage automatique pour transcrire les signaux manuels des alphabets avec un haut niveau d'adaptabilité à divers endroits;
- Obtenir une performance globale permettant la prediction en temps réel et qui distingue les gestes similaires tels que "A" avec "E", "M" et "S";
- Comparer l'apprentissage à partir de Zéro et l'apprentissage par transfert.

## Methodologie
Nous avons développé notre modèle avec **python** en utilisant la bibliothèque **Keras** et démontrer en temps réel avec **OpenCv.**
- **Dataset**
Les données utilisés proviennent de [Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet), ce sont **87 000** images de taille **200 x 200** que nous avons redimensionnées à (64 x 64) pour un compromis avec la puissance de calcul que l'on dispose.
<img href = "./figure/dataset.jpg"/>
- **Modeles**
Nous avons utilisé l'implementation du Resnet50V2 pour former notre modèle à partir de Zéro sur le dataset, puis nous l'avons comparée au modèle préformé à adapter à notre tâche ( apprentissage par transfert).

### Pile de technologie
- Python, notebook
- Tensorflow, Keras, OpenCV

## Resultats
Après avoir formé les modèles, nous obtenues les résultats suivants.

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
<a href="https://github.com/seriamedard/american_sign_language_recognition/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=seriamedard/american_sign_language_recognition" />
</a>

Made with [contrib.rocks](https://contrib.rocks).
