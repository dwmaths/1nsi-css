# Les feuilles de style

## Pour commencer

Le langage HTML sert principalement à fournir du contenu à une page Web et il n'est donc pas utilisé pour la rendre élégante.  
C'est le travail du langage CSS (Cascading Style Sheets) qui permet d'enjoliver le contenu fourni par HTML.

### Interface de développement

Pour développer efficacement un site Web, on propose d'utiliser le logiciel **VSCodium** qui existe sous différentes plateformes et qui est la version libre du logiciel **Visual Studio Code** (propriété de Microsoft). Vous pouvez télécharger la dernière version directement sur [le site](https://vscodium.com/#install){:target="_blank"}.

<center>
    <img src="./images/logo_vs.png" width=200px/>
</center>

!!! tip "Concernant l'installation sur Windows"

    Préférez l'installation **utilisateur** plutôt que l'installation **système**.

### Mise en place

Une fois l'installation terminée, ouvrez le logiciel puis dans votre explorateur de fichiers, créez un dossier **TP_CSS**.  
Faites alors glisser ce dossier dans le logiciel **VSCodium** comme dans la vidéo ci-dessous.

<center>
    <video controls src="./videos/css1.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

Pour davantage d'efficacité dans la gestion du projet, installez l'extension **Live Server** comme dans la vidéo ci-dessous :

<center>
    <video controls src="./videos/css2.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

### Premier exemple

Dans l'explorateur de dossiers de **VSCodium**, ajoutez un fichier nommé **index.html**
et tapez à l'intérieur le texte ```!``` validez par **Entrée** pour ajouter
la structure de base d'un fichier HTML.  

Ajoutez un titre principal en copiant le code suivant entre les balises ```<body></body>```:

``` html title="Ajout d'un titre" linenums="1"
<header>
    <h1>Le pixel art</h1>
</header>
```

!!! tip "Important"

    La balise ```<header></header>``` permet d'apporter une véritable structure à la page Web.  

Cliquez ensuite en bas à droite sur le bouton **Go Live** pour observez votre page Web.  

L'ensemble de ces manipulations est observable dans la vidéo ci-dessous.

<center>
    <video controls src="./videos/css3.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

Pour rendre ce titre agréable à regarder, on va le mettre en forme grâce au CSS.  
Pour cela, créez un fichier nommé **style.css** dans lequel vous allez écrire ces lignes :

``` css title="Mise en forme" linenums="1"
h1 {
    text-transform: uppercase;
    letter-spacing: 3px;
    color: red;
    text-align: center;
}
```

Enregistrez et observez qu'il ne se passe rien sur votre page Web !!!

!!! warning "Mise en relation"

    Il est important de lier le fichier **css** avec votre page web.

Retournez à présent sur la page **index.html** et en dessous de la balise ```<title></title>``` tapez le mot **link** puis cliquez sur **css**.
Enregistrez et observez comme sur la vidéo ci-dessous.

<center>
    <video controls src="./videos/css4.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

### Les outils de développement

Les navigateurs disposent également de leur propre outils de développement.  

Là où se trouve votre page Web, appuyez sur **F12** et en cliquant sur **Élément** vous pouvez survoler les différents blocs qui constituent votre page. 
Il est également possible de désactiver certaines propriétés ou d'en paramétrer d'autres comme dans la vidéo ci-dessous.

<center>
    <video controls src="./videos/css5.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

La propriété ```text-shadow``` permet donc de gérer l'ombre d'un texte mais est difficilement paramétrable à la main. On préfère
utiliser les outils de développement du navigateur pour trouver les valeurs les plus adaptées.

## Les boîtes

La partie qui suit permet de remplir le corps de la page.  
Habituellement, on place le contenu de la page entre les balises ```<main></main>``` pour privilégier 
une structure correcte.

Commencez par ajoutez ces balises au fichier **HTML** puis copier le style proposé dans le fichier **css**.

!!! example "Mise à jour du code"

    === "Fichier HTML"

        ``` html title="Partie principale" linenums="1"
        <main>
            
        </main>
        ```

    === "Fichier CSS"

        ``` css title="Mise en forme" linenums="1"
        main {
            background: lightblue;
        }
        ```

Comme dans la vidéo ci-dessous, on peut observer qu'il ne se passe rien sur la page web !!!

<center>
    <video controls src="./videos/css6.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

!!! important "Raccourci"

    Remarquez que pour écrire les balises ```<main></main>``` il suffit de taper ```main``` et de valider par **Entrée**.

L'idée est de forcer cette section à avoir une taille minimale. Pour cela, on utilise l'attribut **min-height**. On peut également gérer la largeur de la section avec **width**
comme dans la vidéo ci-dessous.

<center>
    <video controls src="./videos/css7.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

Remarquez les différentes unités utilisées. D'abord des pixels pour la hauteur puis un pourcentage pour la largeur.  
Pour centrer la boîte, on ne peut pas utiliser l'attribut **text-align** car ce n'est pas un texte. On utilise plutôt la notion de **marges**.  

Les deux paramètres fournis sont respectivement :

- la hauteur au dessus et en dessous ;
- la hauteur à gauche et à droite.

Observez grâce aux outils de développement du navigateur que les marges correspondent à votre demande.

### Les boîtes personnelles

Nous avons pour l'instant modifier l'apparence des éléments officiels du langage HTML.  
Il est également possible de définir nos propres éléments à l'aide de la balise ```<div></div>```.  

Une div est une **division** de la page Web et qui prend donc par défaut toute la largeur possible.   
Pour identifier une divison personnelle, on lui associe une **classe** grâce à l'attribut ```class```.  
Pour modifier son apparence en CSS, on utilisera l'identifiant de la classe précédé d'un point (```.```).  

Imaginons un instant que l'on souhaite établir une galerie d'images.  
On procédérait comme dans la vidéo ci-dessous.

<center>
    <video controls src="./videos/css8.mp4" poster="./images/apercu.png" width=800 height=auto></video>
</center>

Ajoutons trois images (toutes situées dans le dossiers images) à l'intérieur de cette galerie.  

<center>
    <video controls src="./videos/css9.mp4" poster="./images/apercu.png" width=900 height=auto></video>
</center>

Ces images sont situées les unes à la suite des autres dans notre galerie (dont la hauteur a été modifiée au passage). Pour s'en rendre compte, on peut ajouter une couleur de fond aux images à l'aide du code CSS suivant :

``` css title="Fond des images" linenums="1"
img {
    background: red;
}
```

Cependant, cela affectera toutes les images de la page Web comme le montre la vidéo ci-dessous :

<center>
    <video controls src="./videos/css10.mp4" poster="./images/apercu.png" width=900 height=auto></video>
</center>

Comme le montre la vidéo, si on souhaite modifier exclusivement l'aspect des images de la galerie, on utilise le sélecteur **.galerie > img**.

La position des images n'est donc pas satisfaisante et on devrait pourvoir obtenir un résultat plus agréable en positionnant précisément les images.  
Il existe en réalité un outil beaucoup plus pratique appelé **Flex**.

### Affichage Flex

Le module des boîtes flexibles, aussi appelé « flexbox », a été conçu comme un modèle de disposition unidimensionnel et comme une méthode permettant de distribuer l'espace entre des objets d'une interface ainsi que de les aligner.

Pour attribuer cette propriété, on utilise le code

``` css title="Flexbox" linenums="1"
display: flex;
```

dans le sélecteur représentant le conteneur (ici, notre galerie).  
Une fois cette propriété ajoutée, on peut gérer l'alignement horizontal grâce à la propriété **justify-content** et à l'alignement vertical grâce à la propriété **align-items** comme le montre la vidéo ci-dessous.

<center>
    <video controls src="./videos/css11.mp4" poster="./images/apercu.png" width=900 height=auto></video>
</center>

Il est possible d'utiliser le module de développement du navigateur pour voir l'effet des différents paramètres.

<center>
    <video controls src="./videos/css12.mp4" poster="./images/apercu.png" width=900 height=auto></video>
</center>

## À vous !

Choisir un pays et réaliser une page Web (une seule) sur celui-ci en y intégrant du code CSS pour l'enjoliver.