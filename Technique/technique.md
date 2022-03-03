# Liste des sujets techniques

## Standard Interval

+ S1 : Partir du document de standard IEEE1788 pour lister les opérations sur les intervals qui doivent être supportées


## Cas de tests simples

+ T1 : Lister avec Luc quelques expressions de contracteurs simples utilisés en robotique et balayant la plupart des opérations identifiées en tâche S1

````
Actuellement identifiés : 

        - Contracteur sur un anneau
````

## Compilateur - Expression

+ CE1 : Réaliser un outil en ruby permettant de charger une expression de contracteur utilisant des opérations du standard IEEE1788 sous forme d'arbre syntaxique. Test sur les contracteurs identifiés en T1.

+ CE2 : Réaliser un outil ruby utilisant la représentation obtenue en CE1 pour générer les opérations à appliquer pour réaliser le forward-back. Test sur les contracteurs identifiés en T1.

+ CE3 : A partir de CE2 on génère 2 graphes de dépendance sur les opérations forward et backward. Test sur les contracteurs identifiés en T1.

## Choix d'une architecture HW 

+ A1 : Identifier ce qu'on attend du coprocesseur. Evaluation de contracteurs seulement ? Logique ?

+ A2 : Quel genre de parallélisme veut on exposer ? Parallélisme sur le contracteur ? Parallélisme sur les boites ?

+ A3 : Faire un état de l'art des solutions d'architecture hardware existantes et identifier la plus pertinente (riscv ? vliw ? .....).Quels sont les critères de choix ?