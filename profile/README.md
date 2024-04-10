# 💻 Projet web

## 🧑‍💻 Membres de l'équipe
- Matias Taillade
- Rémi Mandart
- Thomas Bonin

## 📋 Présentation du projet
Création de 2 applications de To do list commune. Une tournée vers le web en **Angular** et une tournée multi plateforme (principalement mobile) avec **Flutter**.

Les données et que la gestion des users sont gérées par **Firebase** en passant par un **midleware** en **Python** pour ne pas dupiquer la logique metier.

Les 3 repositories sont accessibles par l'organisation ou ici:
- [<img src="https://github.com/todoux/.github/assets/94057745/b0c91bad-560d-4f43-94b4-b66af1cd7a17" alt="drawing" width="15"/> Back-end Python](https://github.com/todoux/back-end)
- [<img src="https://github.com/todoux/.github/assets/94057745/afc62395-32e6-4acd-bb60-706c9b515a71" alt="drawing" width="20"/> Angular](https://github.com/todoux/angular-app)
- [<img src="https://github.com/todoux/.github/assets/94057745/3ee8e42a-d247-4428-82af-af853aeb9190" alt="drawing" width="18"/> Flutter](https://github.com/todoux/flutter-app)

Lien du projet [<img src="https://github.com/todoux/.github/assets/94057745/c56b79d8-e0c2-4bee-8aa1-0c5efb855ebb" alt="drawing" width="18"/> Firebase](https://console.firebase.google.com/u/1/project/toudoux-46f4b/overview).


## 📜 Organisation

Le développement, c'est fait en **agilité**. Nous avons prévu 3 **sprint** pour le développement de ce qui est attendu. 
Les tâches de chaque sprint se retrouvent dans le [Board](https://github.com/orgs/todoux/projects/1).  
Cela nous a permis de faire le suivi du projet et aussi de s'adapter.
Chaque jour de travail nous avons fait un petit :sparkles:*daily meeting*:sparkles:. Les résumés de chacun se trouvent ici. !!!TODO!!!

## 🔍 Détails des repositories

### <img src="https://github.com/todoux/.github/assets/94057745/b0c91bad-560d-4f43-94b4-b66af1cd7a17" alt="drawing" width="15"/> Back-end Python

Cette application est un middleware en **Python** qui utilise le framework **BlackSheep** avec une architecture en **DDD** (Domain Driven Design). Elle fait les liens entre **Firebase** (qui nous permet le stockage des données/users) et nos **applications**.  
Elle permet de faire toutes les **implémentations** métier: ajout, modification et suppression des todo, task... Mais aussi la gestion des users. Grâce à cela nous ne dupliquons pas cette logique sur Angular et Flutter (gain de temps et limitation d'erreurs).

Le projet a été **conteneurisé** avec **Docker**: [Dockerfile](https://github.com/todoux/back-end/blob/prod/Dockerfile) et [Makefile](https://github.com/todoux/back-end/blob/prod/Makefile). 
Nous avons aussi ajouté un [CI](https://github.com/todoux/back-end/actions/workflows/ci.yml) avec un lint. 
La mise a jours des dépendances est automatisée par **Dependabot**.
