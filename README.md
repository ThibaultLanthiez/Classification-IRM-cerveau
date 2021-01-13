[:arrow_left: Retour vers le portfolio](https://github.com/ThibaultLanthiez/Portfolio)

<img src="https://github.com/ThibaultLanthiez/Classification-IRM-cerveau/blob/main/image-data-tumor.PNG" width="140%" and height="120%"/>

# Classification d'IRM de cerveau pour la détection de tumeur

L'objectif de ce projet est de classer de images d'IRM de cerveau selon le niveau de gravité de la tumeur (4 classes). Le modèle doit être capable de classer les images dans les classes suivantes : pas de tumeur et 3 stades d'avancement de la tumeur.

Pour cela, j'ai téléchargé sur la plateforme Kaggle un dataset d'environ 400 image d'IRM de cerveau annotés d'une des 4 classes (100 images par classe).

Ensuite, avec le langage python, j'ai pu faire de l'augmentation d'image (data augmentation) en faisant par exemple des rotations et des zooms aux images. Cela permet d'augmenter le nombre d'images pour réduire le risque de sur-apprentissage.

Puis j'ai divisé ces images en jeux de d'apprentissage, de validation et de test.

Enfin, avec créé un modèle via transfer learning. C'est-à-dire que j'ai utilisé le modèle VGG19 qui est modèle déjà entrainé pour la reconnaisance d'image puis je gélé ses convolution pour entrainer juste sa partie supérieur sur mon type de reconnaissance d'image (içi la tumeur de cerveau). Pour cela, j'ai utilisé la bibliothèque Tensorflow.Keras.

Après entraînement, mon modèle arrive à prédire correctement 70% des images que l'on lui donne.

# Code

Voici le code du projet : [notebook](https://github.com/ThibaultLanthiez/Classification-IRM-cerveau/blob/main/tumor%20brain.ipynb)
