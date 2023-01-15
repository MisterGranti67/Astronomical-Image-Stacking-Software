
# (LEPI) Logiciel d'Édition Profesionnel d'Image



## 1. Le but du projet
Lors d'un projet tutoré pour notre BUT informatique, nous devons réaliser un logiciel d'édition d'image (basé sur un .fits, .fit)

## 2. Les prérequis
### 2.1 Le langage de programmation
Nous avons choisis le langage de programmation Python (**Version 3.10.4 recommandée**), étant simplifié d'utilisation et riche en bibliothèque, il est nous est plus facile de développer grâce à celui-ci. L'inconvénient s'est qu'il est lourd d'utilisation, certains fonctions peuvent mettre plusieurs dizaines de minutes à s'exécuter.
### 2.2 Les bibliothèques
#### 2.2.1 Astropy
Utilisez le ```pip install astropy[all]``` pour télécharger la dernière version de la bibliothèque. Elle sert à simplifier nos fonctions, notamment sur les images FITS 
#### 2.2.1 Matplotlib
Utilisez le ```pip install matplotlib``` pour télécharger la dernière version de la bibliothèque. Elle sert à afficher nos images et graphiques sur l'application
#### 2.2.1 Numpy
Utilisez le ```pip install numpy``` pour télécharger la dernière version de la bibliothèque. Elle sert à calculer facilement grâces aux différentes fonctions
#### 2.2.1 scipy
Utilisez le ```pip install scipy``` pour télécharger la dernière version de la bibliothèque. Elle sert à faire la rotation d'une matrice
#### 2.2.1 Pyinstaller
Utilisez le ```pip install Pyinstaller``` pour télécharger la dernière version de la bibliothèque. Elle sert à générer un fichier .exe
## 3. Installation
### 3.1 Avec le .exe
> a. Créez un dossier
>> b. Placez le .exe dans celui-ci
>>> c. Créez un dossier img dans ce dossier
>>>> d. Placez votre dossier "M13_blue" détenant les images fit de nom "M13_blue_000X"
>>>>> e. Executez le fichier .exe

### 3.1 Sans le .exe
> a. Créez un dossier
>> b. Placez les fichiers main.py, Calculation.py, Filters.py, Interface_front.py, Normalization.py, Stacking.py, Stacking_front.py dans le dossier
>>> c. Créez un dossier img dans ce dossier
>>>> d. Placez votre dossier "M13_blue" détenant les images fit de nom "M13_blue_000X"
>>>>> e. Ouvrez le fichier main.py et exécutez la commande "```python main.py```"

## 4. Les fonctionnalités
### 4.1 Stacking
#### 4.1.1 Somme
Assemblage de plusieurs images en additionnant les pixels de chaque images représentée par un tableau 2d
#### 4.1.1 Moyenne
Assemblage de plusieurs images en realisant la moyenne de chaque pixel des différentes images de représentée par un tableau 2d
#### 4.1.1 Médiane
Assemblage de plusieurs images en déterminant la mediane de chaque pixel des différentes images de représentée par un tableau 2d.
#### 4.1.1 Sigma
Assemblage par addition de plusieurs images en ajoutant chaque image avec leur valeurs abérantes filtrer par l'écart et la dispersion de la médiane pour les différentes images de représentée par un tableau 2d
### 4.2 Filters
#### 4.2.1 Valeur abérantes
##### 4.2.1.1 Médiane
Permet de retirer les valeurs abérantes de chaque image d'une liste comportant plusieurs images et de remplacer les valeurs abérantes par la médiane en fonction de l'écart/dispersion autour de la médiane de Q1 et de Q3 avec l'écart interquartile
##### 4.2.1.2 Moyenne
Permet de retirer les valeurs abérantes de chaque image d'une liste comportant plusieurs images et de remplacer les valeurs abérantes par la moyenne en fonction de l'écart/dispersion autour de la médiane de Q1 et de Q3 avec l'écart interquartile
##### 4.2.1.3 Sigma
Permet de retirer les valeurs abérantes de chaque image d'une liste comportant plusieurs images et de remplacer les valeurs abérantes par l'écart et la dispersion de la médiane en fonction de l'écart/dispersion autour de la médiane de Q1 et de Q3 avec l'écart interquartile

#### 4.2.2 Butterworth
##### 4.2.2.1 Passe Haut
Permet d'appliquer une image représenter via un tableau 2d un filtre passe haut de butterworth en convertisant notre image en fréquence via la transformation de fourier et en appliquant le filtre passe haut de butterworth et de la reconvertisant en pixel
##### 4.2.2.2 Passe Bas
Permet d'appliquer une image représenter via un tableau 2d un filtre passe bas de butterworth en convertisant notre image en fréquence via la transformation de fourier et en appliquant le filtre passe bas de butterworth et de la reconvertisant en pixel
#### 4.2.3 Gaussian
##### 4.2.3.1 Passe Haut
Permet d'appliquer un filtre passe haut gaussien qui applique une matrice de convolution gaussienne sur un chaque pixel d'une image représenter via un tableau 2d et la soustrait à l'image de base fessant un high = data-low(gauss)
##### 4.2.3.2 Simple
d'appliquer une matrice de convolution gaussienne donnant un effet de flou sur un chaque pixel d'une image représenter via un tableau 2d

#### 4.2.4 Médiane
Permet de donner une image filtrer de chaque pixel en les remplaçants par la médiane de chaque pixel voisin à un diamètre choisi 
#### 4.2.5 Moyenne
Permet de donner une image filtrer de chaque pixel en les remplaçants par la moyenne de chaque pixel voisin à un diamètre choisi 
#### 4.2.6 Convolution
Permet d'appliquer une matrice de convolution sur un chaque pixel d'une image représenter via un tableau 2d La matrice s'applique en fonction des voisins situer en fonction de la taille/diametre de la matrice directements sur les pixels de l'image
#### 4.2.7 Sobel
Permet d'appliquer une matrice de convolution de sobel en vertical et en horizontal donnant un effet de accentuation des bords des objets de l'image et s'appliquant sur un chaque pixel d'une image représenter via un tableau 2d
#### 4.2.8 Bilateral
Permet d'appliquer un filtre bilateral sur une image donnant un effet de flou/adoucicement sur un chaque pixel d'une image représenter via un tableau 2d via la valeur de la distribution gaussienne et la distance entre les points dans le diametre de voisin choisi permettant d'avoir une distribution plus équitable qu'un filtre gaussien classique

## 5. Crédit
- [Gauthier Corion]
- [Matthieu CZARKOWSKI]


