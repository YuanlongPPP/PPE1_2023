#Journal de bord du projet encadré  

# Séance 1 
C'est le premier cours de PPE. Dans ce cours, nous avons eu une vision globale du cours. Le projet de notre cours peut être divisé en deux phases, à savoir la construction du corpus et l'exploration du corpus.  Afin de le réaliser, nous avons besoin d'une bonne gestion de projet. Il est ainsi qu'on doit utiliser un outil pour déposer les fichiers, consulter l'historique du projet, communiquer et aussi organiser le travail. 
Nous commençons à voir le système de fichier, qui correspond à une sorte d'arborescence. Plusieurs éléments se présentent dans ce système : les chemins (exemple: / désigne la racine de l'arbre, ~/ désigne le dossier personnel de l'utilisateur ('Home')), qui peuvent être divisés en deux catégories principales : chemins absolus et chemins relatifs. On a abordé également un notion très importante : les commandes. La syntaxe d'une commande joue un rôle très important pour notre travail informatique. Il faut notamment connaître voire retenir les commandes suivantes : cd, ls, pwd, cat, less, wc, etc. 
Au niveau pratique, nous avons eu un exercice pour créer classer les documents.
Problème : je n'ai pas eu la base d'informatique, c'est un peu difficile pour moi de comprendre certains termes informatiques. Au niveau pratique, c'est également difficile pour moi de suivre quelques commandes en cours. 
solution : j'ai besoin de passer beaucoup de temps d'apprendre les connaissances de base sur l'informatique en lisant les livres et aussi de les partiquer sur internet. Je dois chercher une solution pour suivre le cours. 

pour l'exercice : on fait mv 2017_02_* ../txt/2017/02 pour déplacer le fichier vers un autre dossier. 


# Séance 2 
Dans le deuxième cours, nous avons commencé à apprendre comment utiliser le github : l'installation du git, la création du compte Github, la création du clé, etc. Et nous avons appris les commandes principaux de git qui servent à gérer les changements : git clone, git pull, git fetch, git add, git rm, git commit, git push, git status et git log.   

difficulté : j'arrive pas à synchroniser le status entre le git et mon local avec des commandes.
solution : C'est le problème de mes commandes. J'ai réessayé, ça marchait. 

J'ai créé un compte Github, le dépôt depuis Github, la récupération du dépôt. En plus, j'ai réalisé certains changements par rapport à mon journal de bord. Je vais synchroniser depuis et vers le dépôt. Finalement, j'ai créé un tag nommé "seance 2" avec un message "version finie séance 2" 

Notes : comment syncroniser vers le dépôt : après avoir fini les modifications par rapport au fichier, on utilise "git add "nom du fichier"", ensuite nous utilisons "git commit [-m message]", et enfin on utilise la commande : "git push" 
Notes : comment syncroniser depuis le dépôt : on utilise "git pull". Cependant, au cas où on fait des modifications dans le local, alors on a besoin de repasser les étapes de "comment syncroniser vers le dépôt" pour éviter des "conflits". 
Difficulté : je n'arrive pas à ajouter un tag avec la commande "git tag -a -m "version finie séance 2" seance2 <commit> "
Solution : en supprimant <commit>, je peux réaliser mon but. 

Je vais maintenant écrire quelque chose : donc il faut ajouter une ou des lignes à la fin de ce journal de bord. ok  

# Séance 3 
En récupérant l'identifiant SHA, nous pouvons utiliser la commande "git log" pour voir les identifiants de commit. En utilisant la commande "git revert + identifiant", nous pouvons annuler le commit qu'on a fait. 
Problème : comment syncroniser les données sur le github et sur l'ordinateur dans le cas où il y a plusieurs branches.  

# Séance 4 
dans ce cours, nous avons abordé le concept de "pipelines", et on a appris quelques commandes : wc, cat, grep, sort, uniq, echo. 
Pour les exercices 
1). on utilise "cat ./*/*/* |wc -l" pour compter le nombre d'annotations dans le texte :  
par exemple, ann cat./2016/*/* |wc -l, cat./2017/*/* |wc -l, cat./2018/*/* |wc -l permettent de compter le nombre d'annotations pour l'année 2016 (9442), 2017 (7179), 2018 (7561).
2). on utilise "cat./2016/*/* | grep location | wc -l；cat./2017/*/*.ann| grep location | wc -l; cat.2018/*/*.ann |grep location | wc -l" pour limiter ce comptage aux lieux (location) 
3). on utilise "echo "Location en 2016"> Location .txt cat 2016/*/*.ann|grep location|wc -l >> Location.txt", "echo "Location en 2016"> Location .txt cat 2017/*/*.ann|grep location|wc -l >> Location.txt", "echo "Location en 2018"> Location .txt cat 2016/*/*.ann|grep location|wc -l >> Location.txt pour sauvegarder ces résultats dans un (seul) fichier.
4). on utilise "echo " Classement des lieux les plus cités en 2016">lieux.txt cat 2016/*/*.ann|grep location|cut -f 3|sort|uniq -c|sort -nr|head -n 15>>lieux,txt ",  Classement des lieux les plus cités en 2017">lieux.txt cat 2017/*/*.ann|grep location|cut -f 3|sort|uniq -c|sort -nr|head -n 15>>lieux,txt " Classement des lieux les plus cités en 2018">lieux.txt cat 2018/*/*.ann|grep location|cut -f 3|sort|uniq -c|sort -nr|head -n 15>>lieux,txt " pour établir le classement des lieux les plus cités. 
5). on utilise "cat */*/.ann|grep "\bmai\b"|cut -f 3|sort|uniq -c|sort -nr pour trouver les annotations les plus fréquentes pour votre mois de naissance, toutes années confondues. 

# Séance 5
Dans ce cours, nous avons abordé les notions telles que l'instruction conditionnelle et validation des arguments. il faut quand même entraînter et partiquer. 
pour le projet en commun, nous avons décidé de travailler sur "désinoformation" ("desinformation") ("虚假消息") dans les trois langues. On va extraire les données sur les sites de langues différentes. Il faut aussi préciser nos hypothèses de recherche pour décider qu'on travaille sur quels types de corpus (presse, blog, etc). 
