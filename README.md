Vegetal ML
================

Un modèle Core ML pour la classification d'images de fruits et légumes.

Aperçu
------

Vegetal ML est un modèle Core ML de classification d'images de fruits et légumes. Le modèle a été entraîné sur plus de 85 000 images de 143 classes différentes, y compris des fruits et légumes courants tels que la pomme, la banane, la tomate, le poivron, etc. Le modèle peut être utilisé pour la classification d'images dans une application iOS ou macOS.

Caractéristiques
------------

* Modèle Core ML de 2,3 Mo.
* 143 classes de fruits et légumes.
* 99 % de précision sur l'ensemble d'entraînement.
* 98 % de précision sur l'ensemble de validation.
* 86 % de précision sur l'ensemble de test.
* Entraîné en 25 itérations sur un iMac 2015 2,8 GHz Quad-Core. 
* Entraîné sur un total de 85 940 images et testé sur 22 688 images.
* Durée de l'entraînement : 24h

Ensemble de données
------------

Les ensembles de données utilisés pour entraîner Vegetal ML proviennent des sources suivantes :

* [Fruit-Images-Dataset](https://github.com/Horea94/Fruit-Images-Dataset)
* [Vegetable-Image-Dataset](https://www.kaggle.com/datasets/misrakahmed/vegetable-image-dataset)
* VegNet

Liste des classes
-----------------

Voici la liste complète des classes de fruits et légumes que Vegetal ML peut reconnaître :
```sql
Nom
Watermelon
m Walnut
 Tomato Yellow
 Tomato not Ripened
 Tomato Maroon
 Tomato Heart
 Tomato Cherry Red
 Tomato
 langelo
Tamarillo
Strawberry Wedge
Strawberry
Salak
 Redcurrant
 Raspberry
Rambutan
 Radish
Quince
Pumpkin
 Potato White
Potato Sweet
Potato Red Washed
Potato Red
 Potato
 Pomelo Sweetie
Pomegranate
 Plum 3
 Plum 2
 Plum
 Pitahaya Red
 Pineapple Mini
Pineapple
 Physalis with Husk
 Physalis
Pepper Yellow
 Pepper Red
Pepper Orange
 Pepper Green
Pepino
Pear Williams
Pear Stone
 Pear Red
 Pear Monster
Pear Kaiser
Pear Forelle
 Pear Abate
Pear 2
Pear
Peach Flat
Peach 2
Peach
Passion Fruit
Papaya
Orange
Onion White
Onion Red Peeled
Onion Red
Nut Pecan
Nut Forest
New Mexico Green Chile
Nectarine Flat
Nectarine
Mulberry
Melon Piel de Sapo
Maracuja
Mangostan
Mango Red
Mango
Mandarine
Lychee
Limes
Lemon Meyer
Lemon
Kumquats
Kohlrabi
Kiwi
Kaki
Huckleberry
Hazelnut
Guava
Grapefruit White
Grapefruit Pink
Grape White 4
Grape White 3
Grape White 2
Grape White
Grape Pink
Grape Blue
Granadilla
Ginger Root
Fig
Eggplant
Dates
Cucumber Ripe 2
Cucumber Ripe
Cucumber
Corn Husk
Corn
Cocos
Clementine

Cocos
Clementine
Chile Pepper
Chestnut
Cherry Wax Yellow
Cherry Wax Red
Cherry Wax Black
Cherry Rainier
Cherry 2
Cherry 1
Cauliflower
Carrot
Carambula
Capsicum
Cantaloupe 2
Cantaloupe 1
Cactus fruit
Cabbage
Broccoli
Brinjal
Bottle Gourd
Blueberry
Bitter_Gourd
Bell Pepper
Beetroot
Bean
Banana Red
Banana Lady Finger
Banana
Avocado ripe
Avocado
Apricot
Apple Red Yellow 2
Apple Red Yellow 1
Apple Red Delicious
Apple Red 3
Apple Red 2
Apple Red 1

Apple Pink Lady
Apple Granny Smith
Apple Golden 3
Apple Golden 2
Apple Golden 1
Apple Crimson Snow
Apple Braeburn
```
Captures d'écran
------------

Voici quelques captures d'écran de Vegetal ML en action :

![Capture d'écran 1](capture1.png)

![Capture d'écran 2](capture2.png)

![Capture d'écran 3](capture3.png)

Utilisation
-----------

Pour utiliser Vegetal ML dans votre application, suivez ces étapes :

1. Téléchargez le fichier `vegetal_ML.mlmodel` depuis le répertoire `Models` de ce dépôt.
2. Ajoutez le fichier `vegetal_ML.mlmodel` à votre projet Xcode.
3. Importez Core ML dans votre fichier Swift :
```swift
import CoreML
```
4. Créez une instance du modèle :
```swift
let model = try? VNCoreMLModel(for: vegetal_ML().model)
```
5. Créez une requête de classification d'images à l'aide du modèle :
```swift
let request = VNCoreMLRequest(model: model!) { (request, error) in
    // Traiter les résultats ici
}
```
6. Effectuez la requête de classification d'images sur une image :
```swift
let handler = VNImageRequestHandler(ciImage: ciImage)
try? handler.perform([request])
```

Contribution
------------

Les contributions à Vegetal ML sont les bienvenues ! Si vous souhaitez contribuer, veuillez ouvrir une pull request avec vos modifications.

License
-------

Vegetal ML est publié sous la licence MIT. Consultez le fichier `LICENSE` pour plus de détails.
