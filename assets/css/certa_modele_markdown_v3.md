<head>
    <link rel="stylesheet" href="./style_certa.css">
</head>

# nom du thème de la publication

## description du thème

| Propriétés | Description |
| :----------| :-----------|
| Intitulé long | <span class="todo">Décrire en une phrase le thème (intitulé long)</span> |
| Formation(s) <br> concernée(s) | <label><input type="checkbox">Classes de première Sciences et technologies du management et de la gestion (STMG) </label> <br> <label><input type="checkbox">Terminale STMG Système d’information de gestion (SIG) </label> <br> <label><input type="checkbox" checked>BTS Services Informatiques aux Organisations</label>
| Matières | <label><input type="checkbox">Sciences de gestion </label> <br> <label><input type="checkbox" checked>SIG</label> <br> <label><input type="checkbox" checked>Bloc 1 – Support et mise à disposition de services informatiques</label> <br> <label><input type="checkbox">Bloc 2 SISR – Administration des systèmes et des réseaux</label> <br> <label><input type="checkbox">Bloc 3 SLAM – Cybersécurité des services informatiques</label>
| Présentation | <span class="todo">Décrire en quelques phrases les objectifs (Présentation)</span> |
| Savoirs | <span class="todo">Point du programme <br> Sous-point éventuel (savoirs)</span> |
| Compétences | Pour certains types de ressources : labo, exolab, ... |
| Transversalité | |
| Prérequis | |
| Outils | |
| Mots-clés | <span class="todo">Séparer les mots-clés par des virgules</span> |
| Durée | Indicative et non-obligatoire |
| Auteur.e.s | |
| Version | v <span class="todo">1</span> |
| Date de <br> publication | |

<br>
<br>

## dernières versions
Ce tableau contient les modifications apportées au document après sa publication uniquement.
<br>

| Date | Auteur.e | Description |
|:----:|:--------:|:-----------:|
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |

<br>
<br>


## SOMMAIRE

Par défaut, le markdown étant un langage simplifié pour réaliser des documents texte, il n'est pas possible de générer automatiquement un sommaire comme permet de le faire un éditeur tel que LibreOffice. Cependant vous pouvez utilisez différents outils pour réalisez cela, tel que Pandoc dont le fonctionnement est détaillé plus bas.  

Par défaut le Markdown permet d'insérer un seul saut de ligne en laissant une ligne vierge. Si vous désirez ajouter des sauts de ligne supplémentaires, il vous faudra utiliser la balise HTML `<br>`.

Pour aller à ligne (sans sauter une ligne), il faut ajouter **2 espaces** à la fin de la ligne précédente.

<blockquote class="info">
Les sauts de pages ne seront visibles que si vous générez le document markdown en PDF. Pour faire cela, vous pouvez utiliser l'instruction \newpage
</blockquote>


## notice pour les documents simples

Les informations qui suivent expliquent comment utiliser correctement ce modèle.

### Utilisation des titres

Ce modèle contient des classes CSS : elles permettent de changer les éléments d'un texte, tout en gardant un ensemble cohérent.
Pour les documents courts et simples, vous pouvez utiliser les quatre premiers titres définis :
- Titre principal ne s'utilise qu'une fois, en début de document.
- Titre 1 est le premier titre pour chaque section du document.
- Titre 2 est utilisé en sous-titre.
- Titre 3 permet de titrer des sections détaillées.

Avec le langage MarkDown, un titre est défini grâce au caractère # suivi d'un espace. Plus vous ajoutez de #, plus le niveau de titre est détaillé. Par exemple pour un titre de niveau 3, on utilisera ###.

Le reste du document est rédigé en "Corps de Texte".
Pour atteindre ces styles, on peut utiliser le menu déroulant "Styles" ou bien passer par les icônes du ruban (barre d'outils)

Ces titres ne sont pas numérotés.

Par exemple, pour un exercice on utilisera uniquement les titres de style "Titre 1" suivants :
- Énoncé
- Questions
- Annexes ou Documents
- Corrigé

### Textes masqués

Dans un texte qui doit être caché aux élèves (des réponses ou bien des indications pour les professeurs) utilisez les deux classes CSS : teacher (rouge) ou student (vert).

<span class="student">Réponse cachée aux élèves</span>

<span class="teacher">Partie destinée uniquement aux profs</span>

<p>
    <details>
        <summary>Code HTML pour un bloc à déplier</summary>
        These details <em>remain</em> <strong>hidden</strong> until expanded.
    </details>
</p>

### Partie de code
Le style **Codage > Titre_Code** permet de placer un nom de fichier à un code à suivre.
Le style **Codage > CODE** utilise une police compatible Windows et Linux (Liberation Mono) alignée à gauche.
De plus, les mots du bloc de texte de ce style ne seront pas vérifiés par le dictionnaire (dans style >  police, la langue est sur [Aucun(e)] )

Exemple de code :
```
Ceci est un bloc de code
```

Et `ceci est une partie de code` dans une phrase.

### Mise en évidence

Trois styles ont été ajoutés pour permettre d'avertir (orange-jaune), d'interdire (rouge-violet) ou d'informer (bleu) le lecteur, avec un symbole correspondant. Les contraintes techniques ne permettent pas d'agrandir les symboles ou de modifier facilement l'espacement des caractères et lignes.

<blockquote class="warning">
Pour utiliser ce bloc de mise en évidence, utilisez la balise HTML blockquote avec la classe CSS "warning".
</blockquote>

<br>

<blockquote class="danger">
Pour utiliser ce bloc de mise en évidence, utilisez la balise HTML blockquote avec la classe CSS "danger".
</blockquote>

<br>

<blockquote class="info">
Et voici l'écriture d'un simple texte en information. Pour utiliser ce bloc de mise en évidence, utilisez la balise HTML blockquote avec la classe CSS "info".
</blockquote>

<br>

### Autres instructions MarkDown

Pour mettre du texte en italique, il faut l'encadrer de *.
Exemple :
```
*Une phrase en italique*
```
 Donne à la prévisualisation :
*Une phrase en italique*

Pour mettre du texte en gras, il faut l'encadrer de **.
Exemple :
```
**Une phrase en gras**
```
 Donne à la prévisualisation :
**Une phrase en gras**

Pour barrer du texte, il faut l'encadrer de ~~.
Exemple :
```
~~Une phrase barrée~~
```
 Donne à la prévisualisation :
~~Une phrase barrée~~


## Documents structurés
### Les titres

Pour les documents nécessitant une structuration plus forte, vous pouvez utilisez la numérotation :
* **Titre principal** ne s'utilise qu'une fois, en début de document.
* **Titre 2** est le premier titre pour chaque section du document (numérotation A, B, C...)
* **Titre 3** est utilisé en sous-titre (numérotation 1, 2, 3...)
* **Titre 4** permet de titrer des sections détaillées (numérotation 1.1, 1.2, 1.3…)
* **Titre 5** décrit des sections très détaillées (numérotation 1.1.1, 1.1.2...)

La numérotation est réalisée automatiquement grâce aux styles CSS.

## Exemple titre 2
### Exemple titre 3
#### Exemple titre 4
##### Exemple titre 5
###### Exemple titre 6

<br>

### Autres éléments
#### Code
Le style CODE fonctionne de manière identique que la forme simple.

#### Sommaire
Utiliser le module Pandoc pour générer automatiquement le sommaire.

## Annexes
### Références des symbales de Certa

Les images ne sont pas directement intégrables dans un document MarkDown, il faut donc les avoir localement et utiliser un chemin relatif (ou absolu) ou les héberger sur un serveur web et utiliser l'URL.

![Texte alternatif](./info.png "Titre de l'image")
![Texte alternatif](./warning.png "Titre de l'image")
![Texte alternatif](./danger.png "Titre de l'image")

<br>

### Références des couleurs CERTA

De préférence, le document ne devrait utiliser que la charte graphique ci-dessous pour les titres, tableaux et éléments de fond.

![Texte alternatif](./charte_couleurs.png "Titre de l'image")

<br>

### Tableau

Les barres verticales (|) permettent d’éditer des tableaux avec Markdown. Chaque cellule du tableau est séparée d’une barre verticale. Pour créer des lignes de titre qui se distinguent du reste du tableau, vous devrez souligner les cellules concernées avec les tirets du 6.  
Exemple :
```markdown
| Nom | Valeur | Valeur |
|:----|:--------|:-----------|
| Dupond |5 |7 |
|Dupont | 7|8 |
```
Donne :

| Nom | Valeur | Valeur |
|:----|:--------|:-----------|
| Dupond |5 |7 |
|Dupont | 7|8 |

Le style correspondant a été défini dans le fichier CSS `style_certa.css`

<br>

### Utilisation des listes à puce
#### Listes spéciales

Les listes à puces normales utilisent un style par défaut défini dans le fichier CSS. Pour définir une liste à puce avec MarkDown, il suffit de mettre un "-" ou une "*" suivi d'un espace et ce, pour chaque élément de la liste. Un élément par ligne. Laisser une ligne vide avant et après la liste. Pour les listes ordonnées, utiliser un chiffre suivi d’un point et d’une espace.

Par exemple, dans le cas d'un exercice :
* Travail à faire 1  
Rédiger ici le travail à faire
    * Q1. Pour des sous-éléments, mettre 4 espaces suivis d'une "*"

<br>

#### Usage des listes

D'un point de vue rédactionnel, voici les recommandations d'usage des listes.
* Listes à puces introduites par deux points :
    * commencer la phrase par une minuscule même quand l’élément précédent se termine par un point ;
    * finir les items de préférence par une virgule ou un point-virgule ; un point quand la phrase l'exige.
    * le dernier élément se termine par un point.

* Listes à puces introduites par un point.
    * Commencer la phrase de chaque item par une majuscule.
    * Finir les items par un point.

<br>

### Choix de police
#### Police par défaut

Le choix a été fait d'après le tableau suivant : http://www.apaddedcell.com/sites/www.apaddedcell.com/files/fonts-article/final/index.html
En sérif, Times new Roman ou Georgia.
En sans sérif, sous LibreOffice, Liberation Sans ou Arial.
Par défaut la police est "Libération Sans", mais vous pouvez utiliser les polices ci-dessous grâce aux classes CSS "arial", "times" et "giorgia".

| | |
|---|---|
| Arial | <span class="arial">C'est en 1990 (époque joyeuse) que Bob prononça : "un temps ? Bof..."</span> |
| Times New Roman | <span class="times">C'est en 1990 (époque joyeuse) que Bob prononça : "un temps ? Bof..."</span> |
| Georgia | <span class="georgia">C'est en 1990 (époque joyeuse) que Bob prononça : "un temps ? Bof..."</span> |

#### Fonctionnement des blocs de code

Comme dit plus haut, un bloc de code en markdown s'insère grâce aux caractères **```**

Voici un exemple de code PHP :
```
<?php
$var = 12;
echo 'Var='.$var;
?>
```
Il est également possible d'ajouter la coloration syntaxique en spécifiant le langage : **```php**

``` php
<?php
$var = 12;
echo 'Var='.$var;
?>
```

Ou encore un exemple en C :

``` c
// Le code s'insère ici
int a=5;
printf ("%d",a);
```

Et en Javascript : 

``` javascript
let randomNumber = Math.floor(Math.random() * 100) + 1;

let guesses = document.querySelector('.guesses');
```