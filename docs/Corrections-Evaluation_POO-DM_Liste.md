## Nom Prénom : 

## Programmation Orientée Objet :
### Exercice 1
On considère l'extrait de code ci-dessous :
```python
bart = Simpson("fils", 12)
homer = Simpson("père", 41)
homer.ronfle()
```
Compléter les phrases ci-dessous  :

1. ```bart``` est une **instance** de la **classe**  ```Simpson```.
2. C'est donc un **objet** de type **Simpson**.
À la construction, l'**objet** ```homer``` possède (au moins) deux **attributs** qui valent ```"père"``` et ```41```.
Il possède aussi (au moins) une **méthode** appelée **ronfle()**.

### Exercice 2
On s'intéresse aux joueurs du Top14 de rugby.

1. Construire une classe ```Joueur``` où chaque instance contiendra les attributs ```nom```, ```club``` et ```age```.  
```python
class Joueur :
    def __init__(self, nom, club, age):
        self.nom = nom
        self.club = club
        self.age = age
```

2. Instancier le joueur Nans_DUCUING, joueur de 27 ans évoluant à l'UBB.
```python

nducuing = Joueur("Nans DUCUING", "UBB", 27)
```

3. Écrire une fonction prenant en paramètres deux joueurs de la classe ```Joueur``` et renvoyant le nom du joueur le plus âgé, ou celui des deux joueurs dans le cas d'une égalité d'âge.
```python
def compare(joueur1, joueur2) :
    if joueur1.age > joueur2.age :
        return joueur1.nom
    elif joueur2.age > joueur1.age :
        return joueur2.nom
    else :
        return joueur1.nom,joueur2.nom
```

## Listes chainées :

On considère des listes chaînées, avec la liste vide notée `nil` et les fonctions suivantes :

| Fonction | Description |
|:-:|:-:|
| `tete(liste)` | Renvoie la valeur du premier maillon de `liste`, qui ne doit pas être vide. |
| `queue(liste)` | Renvoie la liste sur laquelle pointe le premier maillon de `liste`, qui ne doit pas être vide. |
| `cons(valeur, liste)` | Renvoie une nouvelle liste correspondant à l’ajout de `valeur` en début de `liste`. |
| `est_vide(liste)` | Renvoie un booléen indiquant si `liste` est vide ou non. |

Le schéma suivant correspond à la représentation en mémoire des listes chaînées `l1`, `l2`, `l3` et `l4`.

![Schéma de définition des Listes](Listes.png)

### Exercice 1 :
Pour chacune des commandes suivantes, indiquer la réponse obtenue.

1. `tete(l2)` :  1
1. `queue(l1)`:  [1, 7]
1. `est_vide(queue(l1))`:  False
1. `tete(queue(queue(queue(l4))))`:  6
1. `est_vide(queue(queue(l2)))`:  True

### Exercice 2 :
L'instruction `l1 = cons(6, cons(1, cons(7, nil)))` définit la liste `l1`.
Donner les définitions des listes `l2`, `l3` et `l4` à l’aide des fonctions `cons` et `queue` et en réutilisant les listes déjà définies pour définir les suivantes :
1. `l2` = queue(l1)
2. `l3` = cons(3, cons(5, l1))
3. `l4` = cons(8, l3)

### Exercice 3 :
En utilisant les fonctions données ci-dessus,  proposer une version itérative et une version récursive pour la fonction `longueur(liste)` qui renvoie la longueur de la liste chaînée `liste` telle que :
```python
>>> longueur(nil)
0
>>> longueur(cons(7, cons(0, cons(12, nil))))
3
```
```python
def longueur(liste) : # version itérative
	


    
    
    
    


```
```python
def longueur(liste) : # version récursive
	

    
    
    
    




```


