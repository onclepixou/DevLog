# Motivation du sujet

Dans le but de construire un discours sur mon sujet de thèse, j'aimerais clarifier plusieurs points qui me semblent essentiels pour justifier l'intérêt de mes travaux. Voici la liste des questions auxquelles il faut selon moi répondre :

## Justification de l'emploi des intervals en robotique

- Quels sont les problèmes types : (localisation ?, ...)
- Quel est l'avantage d'utiliser des intervals par rapport à d'autres méthodes plus classiques (ex : Kalman, Fap pour la localisation)

## Formalisation des problèmes d'intervals en robotique

- Est ce que les problèmes d'intervals rencontrés en robotique se résument tous à des évaluations de contracteurs ?

## Limitations rencontrées  dans l'utilisation des intervals en robotique (en mode software)

- Problèmes de portabilité ?
- Problèmes de temps réel ?
- Bibliothèques pas maintenues ?
- Problèmes de précision des flottants ?

## Fil rouge de la thèse

- Il faut identifier un cas d'usage réel (robotique sous marine ?) qui est compliqué à traiter en temps réel pour des questions de quantité de données.
Ce problème serait idéalement réglé en embarqué par une implémentation hardware. Même si le cas est trop compliqué pour être traité immédiatement cela permettrait de fixer un but à long terme et de justifier l'intérêt du sujet.

## Pertinence d'une solution hardware "maison"

- Dans un contexte d'une utlisation embarquée, quel serait l'apport de notre solution alors qu'il existe d'autres accélérateurs : GPU, ...

- Peut on réellement espérer faire mieux que NVIDIA ?