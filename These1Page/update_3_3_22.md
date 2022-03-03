# Ma thèse en une page (3/3/22)


L'objectif de ma thèse est de définir/réaliser un accélérateur matériel pour les problèmes de calculs par intervals dans le cadre de la robotique.

La plupart des applications robotiques utlisant des intervals consistent à appliquer des contracteurs sur un domaine d'entrée que l'on souhaite réduire. Cette opération a un caractère éminemment parallélisable et profiterait grandement d'une architecture hardware. Cela permettrait aussi de résoudre les problèmes traditionnels de portabilité des bibliothèques software interval (rouding, dépendances, ...)

La majorité des applications robotiques doivent être traité dans un contexte embarqué avec des contraintes temps réel fortes. L'accent sera mis sur la vitesse et le caractère "garanti" des calculs au détriment de la précision des résultats (ce problème a déjà été traité par mpfr et l'équipe de Nathalie Revol et il est illusoire d'essayer de faire mieux).

Dans un premier temps je compte partir du standard IEEE1788 qui formalise les opérations les plus utilisées sur les intervals et ainsi assurer une compatibilité avec bon nombres d'applications.

Le gros du travail consistera à développer un DSL permettant à un utilisateur de spécifier son problème d'interval (contracteur ?), du compilateur associé qui va réaliser les passes d'optimisation et générer un code machine compréhensible par le coprocesseur.
L'architecture du processeur reste à définir mais à l'heure actuelle les premières recherches penchent pour du vliw (very long instruction word) qui semble bien adapté à nos problèmes. Ce choix impliquera plus ou moins de travail sur le compilateur. Un autre aspect important du travail est la discussion sur le jeu d'instruction à employer pour notre architecture (où fixer le curseur haut-niveau/bas niveau et quel est l'impact sur les performances)

L'objectif est d'améliorer incrémentalement les performances et la complétude de notre plateforme hardware (via simulation/émulation dans un premier temps). Les tests commenceront avec des contracteurs très basiques utilisées en robotique. A terme et si les résultats le permettent j'aimerais pouvoir implémenter un problème "réel" qui est difficilement réalisable sans accélération hardware et valider la plateforme dessus. Le couronnement des travaux serait la synthèse de notre coprocesseur sur un FPGA et l'utilisation dans des tests grandeur nature.