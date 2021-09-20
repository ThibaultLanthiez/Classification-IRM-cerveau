[:arrow_left: Retour vers le portfolio](https://github.com/ThibaultLanthiez/Portfolio)

<img src="https://github.com/ThibaultLanthiez/Classification-IRM-cerveau/blob/main/image-data-tumor.PNG" width="140%" and height="120%"/>

# Classification d'IRM de cerveau pour la détection de tumeur

L'objectif de ce projet est de classer des images d'IRM de cerveau ayant ou non une tumeur. Le modèle doit être capable de classer les images dans les classes suivantes : pas de tumeur et 3 stades d'avancement de la tumeur.

Pour cela, j'ai téléchargé sur la plateforme Kaggle un dataset d'environ 400 image d'IRM de cerveau annotées d'une des 4 classes (100 images par classe).

Ensuite, avec le langage Python, j'ai pu faire de l'augmentation d'images (data augmentation) en faisant par exemple subir des rotations et des zooms aux images. Cela permet d'augmenter le nombre d'images pour réduire le risque de sur-apprentissage.

Puis j'ai divisé ces images en jeux de d'apprentissage, de validation et de test.

Enfin, avec créé un modèle via apprentissage par transfert. C'est-à-dire que j'ai utilisé le modèle VGG19 qui est modèle déjà entrainé pour la reconnaissance d'images puis j'ai gelé ses convolutions pour entrainer juste sa partie supérieure sur mon type de reconnaissance d'image (ici la tumeur de cerveau). Pour cela, j'ai utilisé la bibliothèque Keras.

Après entraînement, mon modèle arrive à prédire correctement 70% des images que l'on lui donne.

# Code

Voici le code du projet : [notebook](https://github.com/ThibaultLanthiez/Classification-IRM-cerveau/blob/main/tumor%20brain.ipynb)
