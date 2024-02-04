# Analyse de Sentiments sur X
## Analyse de sentiments sur 1,6 million de tweets
- Trouvez le jeu de données ici : https://www.kaggle.com/karan842/twitter-sentimental-analysis/data


<img src='https://github.com/issaniang5/Analyseur-de-sentiments-sur-X/blob/main/tweet%202.jpg' height=800px width=800px></img>

- Suivez-moi sur Twitter : https://twitter.com/KuchBhiKaran

# 🔵 À propos du projet

- Twitter est l'une des plateformes de médias sociaux les plus populaires sur laquelle nous pouvons partager nos pensées, opinions et tweets tendance sous forme de texte, d'images et de vidéos. Dans ce projet, je vais analyser les sentiments des tweets qui sont sous forme de texte. J'ai collecté ces données depuis Kaggle. Comme la tâche repose sur des tweets sous forme de texte, il s'agit d'un problème de Traitement du Langage Naturel. Il y a 1,6 million de tweets dans ce jeu de données, ce qui le rend très volumineux.

- L'objectif principal est de prédire le sentiment derrière chaque tweet, c'est-à-dire, est-ce un tweet positif ou négatif ? Avec cette stratégie, nous pouvons identifier les tweets positifs ou négatifs, c'est-à-dire ceux qui sont nuisibles et irrespectueux selon les lignes directrices de Twitter.
# 🔵 Contexte :
- Le jeu de données utilisé est le sentiment140 dataset. Il contient 1 600 000 tweets extraits via l'API de Twitter. Les tweets ont été annotés (0 = Négatif, 4 = Positif) et peuvent être utilisés pour détecter le sentiment.

- [Les données d'entraînement ne sont pas parfaitement catégorisées, car elles ont été créées en étiquetant le texte en fonction des emojis présents. Ainsi, tout modèle construit avec ce jeu de données pourrait avoir une précision inférieure à celle attendue, car le jeu de données n'est pas parfaitement catégorisé.]

- Il contient les 6 champs suivants :

- sentiment : La polarité du tweet (0 = négatif, 4 = positif)
- ids : L'ID du tweet (2087)
- date : La date du tweet (sam. 16 mai 23:58:44 UTC 2009)
- flag : La requête (lyx). Si aucune requête n'est présente, la valeur est NO_QUERY.
- user : L'utilisateur qui a tweeté (robotickilldozr)
- text : Le texte du tweet (Lyx est cool)
- Nous n'avons besoin que des champs sentiment et text, donc nous éliminons le reste.

- De plus, nous modifions le champ sentiment pour qu'il ait de nouvelles valeurs reflétant le sentiment. (0 = Négatif, 1 = Positif).

# 🔵 Approche :
- Collecte des données depuis Kaggle
- Importation avec les étapes essentielles et création d'une visualisation décrivant le nombre de tweets positifs et négatifs.
- Traitement du texte : les étapes prises sont la conversion en minuscules,
Remplacement des emojis,
Remplacement des noms d'utilisateur,
Suppression des caractères non alphabétiques,
Suppression des lettres consécutives,
Suppression des mots courts,
Suppression des stopwords,
Lemmatization.
- Pour ce projet, j'utilise la bibliothèque NLTK. Vous pouvez utiliser spaCy3 ou une autre bibliothèque.
- Par WordCloud, j'ai affiché les mots importants des tweets négatifs et positifs.
- Division des données en ensembles d'entraînement et de test.
- Création de 3 types de modèles différents pour de meilleurs résultats et une meilleure précision : Bernoulli Naive Baye (Bernoulli), Linear Support Vector Classification (LinearSVC), Logistic Regression (LR).
- Évaluation des 3 modèles à l'aide du rapport de classification et de la matrice de confusion.
- Sélection du meilleur modèle parmi eux.
- Sauvegarde des modèles.
- Écriture d'une fonction qui peut prédire le sentiment des tweets.
- Test de quelques phrases et détermination de leur sentiment.



🔵 Merci ! <3