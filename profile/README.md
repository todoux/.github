# 💻 Projet web
  
## 🧑‍💻 Membres de l'équipe
- Matias Taillade
- Rémi Mandart
- Thomas Bonin

## 📋 Présentation du projet ✨**Todoux**✨
<p align="center">
    <img src="https://github.com/todoux/.github/assets/94057745/53d862f0-448f-4a1f-affe-4f7bf3e9b3af" style="width: 200px">
</p>
L'application est une To Do list multiplateforme. Les Framework utilisés sont **Angular** (web) et **Flutter** (principalement mobile).

Les données et la gestion des users sont gérées par **Firebase** en passant par un **midleware** en **Python** pour ne pas dupiquer la logique metier.

Les 3 repositories sont accessibles par l'organisation ou par les liens suivants:
- [<img src="https://github.com/todoux/.github/assets/94057745/b0c91bad-560d-4f43-94b4-b66af1cd7a17" alt="drawing" width="15"/> Back-end Python](https://github.com/todoux/back-end)
- [<img src="https://github.com/todoux/.github/assets/94057745/afc62395-32e6-4acd-bb60-706c9b515a71" alt="drawing" width="20"/> Angular](https://github.com/todoux/angular-app)
- [<img src="https://github.com/todoux/.github/assets/94057745/3ee8e42a-d247-4428-82af-af853aeb9190" alt="drawing" width="18"/> Flutter](https://github.com/todoux/flutter-app)

Lien du [<img src="https://github.com/todoux/.github/assets/94057745/c56b79d8-e0c2-4bee-8aa1-0c5efb855ebb" alt="drawing" width="18"/> Firebase](https://console.firebase.google.com/u/1/project/toudoux-46f4b/overview).


## 📜 Organisation

Le développement, c'est fait en **agilité**. Nous avons prévu 3 **sprint** pour le développement de ce qui est attendu. 
Les tâches de chaque sprint se retrouvent dans le [Board](https://github.com/orgs/todoux/projects/1).  
Chaque branche est reliée à une tâche. Un Pull Request est demandé pour merge dans dev pour avoir une relecture de chaque implémentation. Cela nous a permis de faire le suivi du projet et aussi de s'adapter.  
Chaque jour de travail nous avons fait un petit :sparkles:*daily meeting*:sparkles:. Les [résumés](#ici) de chacun se trouvent en bas de ce document.

## 🔍 Détails des repositories

### <img src="https://github.com/todoux/.github/assets/94057745/b0c91bad-560d-4f43-94b4-b66af1cd7a17" alt="drawing" width="15"/> Back-end Python

Cette application est un middleware en **Python** qui utilise le framework **BlackSheep** avec une architecture en **DDD** (Domain Driven Design). Elle fait les liens entre **Firebase** (qui nous permet le stockage des données/users) et nos **applications**.  
Elle permet de faire toutes les **implémentations** métier: ajout, modification et suppression des todo, task... Mais aussi la gestion des users. Grâce à cela nous ne dupliquons pas cette logique sur Angular et Flutter (gain de temps et limitation d'erreurs).

Le projet a été **conteneurisé** avec **Docker**: [Dockerfile](https://github.com/todoux/back-end/blob/prod/Dockerfile) et [Makefile](https://github.com/todoux/back-end/blob/prod/Makefile). 
Nous avons aussi ajouté un [CI](https://github.com/todoux/back-end/actions/workflows/ci.yml) avec un lint. 
La mise a jours des dépendances est automatisée par **Dependabot**.

### <img src="https://github.com/todoux/.github/assets/94057745/afc62395-32e6-4acd-bb60-706c9b515a71" alt="drawing" width="20"/> Angular

Cette application **Angular**  permet de gérer les todos, les task et les utilisateurs. Elle communique avec le back-end pour les données. La gestion des utilisateurs est elle effectuée par Firebase.  
Ici c'est une application orianté web.

Le projet a été **conteneurisé** avec **Docker**

### <img src="https://github.com/todoux/.github/assets/94057745/3ee8e42a-d247-4428-82af-af853aeb9190" alt="drawing" width="18"/> Flutter

Cette application **Flutter** permet de gérer les todos, les task et les utilisateurs. Elle communique avec le back-end pour les données. La gestion des utilisateurs est elle effectuée par Firebase.   
Ici c'est une application orianté mobile.

Le projet n'a pas été **conteneurisé** avec **Docker** par manque de temps. 

## <a id="ici" />:sparkles:*Daily meeting*:sparkles:

Je ne touche pas au résumé et ils ont été fait sur le fil des réunions donc désolé si ce n'est pas bien structuré ou si il y a des fautes.

### 📆 1er *daily meeting*

*Je le mets dans daily meeting mais cette première section est surtout la mise en place des idées, le choix des rôles et de ce qui peut être fait dans les délais. Je sais que ce n'est pas réellement un daily mais je pense que c'est intéressant de le mettre ici.
Au début du projet nous sommes que 2 (Rémi et Matias) et Thomas nous a rejoins plus tard.*

Nous voulons mettre en place rapidement un midleware pour pouvoir nous simplifier la logique metier et pouvoir nous concentrer sur le front dans les projets Angular et Flutter.  
C'est Rémi qui s'occupe de la mise en place du projet Python et qui choisit la stack (BlackSheep, architecture DDD, etc...) car c'est un spécialiste dans le domène.
Matias s'occupe de la mise en place du board, des issues futur et de l'écriture des daily (et oui c'est moi 🙋) etc... Puis du projet Angular.  
Nous allons faire la connexion avec Firebase et Flutter que dans le 2eme sprint.

### 📆 2ème *daily meeting*
Thomas est rentré dans l'équipe hier apres-midi. Nous lui avons fait un point sur le projet et les tâches à faire. Il va donc s'occuper de la partie Angular car il maitrise le framework contrairement a Matias (le nullos).

#### 🧑‍💻 Matias
Hier j'ai commencé le board avec les issue des 2 premiers spints, Aujourd'hui je vais adapter les issues avec l'arrivé de Thomas. Notemment la mise en place du Firebase va revenir dans le sptint 1 et je vais m'en occuper et l'intégrer au Back. J'ai aussi start le projet Angular.
Pas de blocage les bg

#### 🧑‍💻 Rémi
La base du projet est en place, je vais commencer à implémenter les premières routes pour les todos. Un jknkjgnk a été mis en place pour tester les requêtes. Je vais aider Matias a mettre en place Firebase cette aprèm.
Pas de blocage

#### 🧑‍💻 Thomas
J'avance sur le Angular en préparant les templates pour les todos. Je pourrais implémenter les services que dans le 2eme sprint.
Pas de blocage

### 📆 3ème *daily meeting*

#### 🧑‍💻 Matias
J'ai fini la mise en place de Firebase et j'ai presque fini l'implementation avec l'aide de Rémi. Aujourd'hui je vais finir l'implementation actualiser des issues et je vais commencer a faire une présentation de notre travail dans le README de l'organisation pour faire un truc propre.
Pas de blocage

#### 🧑‍💻 Rémi
J'ai fini l'implémentation des routes et j'aide Matias pour l'implementation de Firebase. Aujourd'hui je vais m'occuper de la finir les implémentation et commencer Flutter ou la mise en place des users.
Pas de blocage

#### 🧑‍💻 Thomas
J'ai presque fini la mise en place des templates, je fais fasse a un problème avec mon environnelent angular qui ne se met pas a jour. Je vais essayer de le régler aujourd'hui.
Pas de blocage

### 📆 4ème *daily meeting*

#### 🧑‍💻 Matias
J'ai fini l'implementation de Firebase et j'ai commencé a faire la présentation du projet. J'ai regarder comment mettre en place les user et j'ai commencer a les mettre en place avec Remi. 
Parallelement je vais pofiner présentation.
Pas de blocage

#### 🧑‍💻 Rémi
J'ai fini l'implementation des routes et j'ai commencé a mettre en place les users avec Matias. Aujourd'hui je vais finir les users et commencer Flutter.
Pas de blocage

#### 🧑‍💻 Thomas
J'ai fini la mise en place des templates. J'ai fini de régler mon problème d'environnement. Aujourd'hui j'implemente le back dans angular.
