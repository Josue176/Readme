# Application de Liste de Tâches

Ceci est une simple application de liste de tâches construite avec React pour le frontend et NestJS pour le backend. Elle permet aux utilisateurs de créer, lire, mettre à jour et supprimer des tâches.

## Table des Matières

- [Fonctionnalités](#fonctionnalités)
- [Technologies Utilisées](#technologies-utilisées)
- [Prérequis](#prérequis)
- [Installation](#installation)
  - [Frontend](#frontend)
  - [Backend](#backend)
- [Exécution de l'Application](#exécution-de-lapplication)
  - [Frontend](#frontend-1)
  - [Backend](#backend-1)
- [Points d'Accès API](#points-daccès-api)
- [Structure des Dossiers](#structure-des-dossiers)
- [Tests](#tests)
- [Déploiement](#déploiement)
- [Contribution](#contribution)
- [Licence](#licence)

## Fonctionnalités

- Créer de nouvelles tâches avec un titre et une description optionnelle.
- Afficher une liste de toutes les tâches.
- Marquer les tâches comme terminées.
- Modifier les tâches existantes.
- Supprimer des tâches.
- Interface utilisateur simple et intuitive.

## Technologies Utilisées

**Frontend (React) :**

- [React](https://react.dev/) - Bibliothèque JavaScript pour la construction d'interfaces utilisateur.
- [React Router](https://reactrouter.com/) - Pour la gestion de la navigation de l'application (si applicable).
- [Axios](https://axios-http.com/) - Client HTTP basé sur les Promises pour effectuer des requêtes API.
- [Bibliothèque de Gestion d'État](https://redux.js.org/) ou [Context API](https://react.dev/learn/passing-data-deeply-with-context) - (Spécifiez si vous en avez utilisé une).
- [Bibliothèque/Framework de Style](https://styled-components.com/) ou [CSS Modules](https://github.com/css-modules/css-modules) ou [CSS natif] - (Spécifiez comment vous avez stylisé votre application).

**Backend (NestJS) :**

- [NestJS](https://nestjs.com/) - Framework Node.js progressif pour construire des applications serveur efficaces et évolutives.
- [TypeScript](https://www.typescriptlang.org/) - Sur-ensemble de JavaScript qui ajoute le typage statique.
- [TypeORM](https://typeorm.io/) ou [Mongoose](https://mongoosejs.com/) - ORM/ODM pour l'interaction avec la base de données (Spécifiez lequel vous avez utilisé).
- [Base de Données](https://www.postgresql.org/) ou [MongoDB](https://www.mongodb.com/) ou [autre] - (Spécifiez la base de données que vous avez utilisée).
- [Class-validator](https://github.com/typestack/class-validator) et [class-transformer](https://github.com/typestack/class-transformer) - Pour la validation et la transformation des données de requête.

## Prérequis

Avant de commencer, assurez-vous d'avoir les éléments suivants installés :

- [Node.js](https://nodejs.org/) (version >= 18 recommandée)
- [npm](https://www.npmjs.com/) (version >= 9 recommandé) ou [yarn](https://yarnpkg.com/) (version >= 1.22 recommandé)
- [Git](https://git-scm.com/)

## Installation

Clonez le dépôt :

```bash
git clone <l'URL-de-votre-dépôt>
cd <le-nom-de-votre-dépôt>


Frontend
Naviguez vers le répertoire frontend :

Bash


cd frontend


Installez les dépendances avec npm :

Bash


npm install


ou avec yarn :

Bash


yarn install


Backend
Naviguez vers le répertoire backend :

Bash


cd backend


Installez les dépendances avec npm :

Bash


npm install


ou avec yarn :

Bash


yarn install


Exécution de l'Application
Frontend
Naviguez vers le répertoire frontend :

Bash


cd frontend


Démarrez le serveur de développement :

Bash


npm start


ou

Bash


yarn start


Ceci démarrera généralement l'application React sur http://localhost:3000.
Backend
Naviguez vers le répertoire backend :

Bash


cd backend


Démarrez le serveur de développement :

Bash


npm run start:dev


ou

Bash


yarn start


Ceci démarrera généralement l'application NestJS sur http://localhost:3001.
Points d'Accès API
Voici une liste des points d'accès API exposés par le backend :
GET /api/todos : Récupérer toutes les tâches.
GET /api/todos/:id : Récupérer une tâche spécifique par son ID.
POST /api/todos : Créer une nouvelle tâche. Le corps de la requête doit être en JSON avec title (chaîne de caractères) et description optionnelle (chaîne de caractères).
PATCH /api/todos/:id : Mettre à jour une tâche existante. Le corps de la requête doit être en JSON avec les champs à mettre à jour (par exemple, title, description, completed).
DELETE /api/todos/:id : Supprimer une tâche par son ID.
Structure des Dossiers



le-nom-de-votre-dépôt/
├── backend/
│   ├── src/
│   │   ├── app.controller.ts
│   │   ├── app.module.ts
│   │   ├── app.service.ts
│   │   ├── todos/
│   │   │   ├── dto/
│   │   │   │   ├── create-todo.dto.ts
│   │   │   │   └── update-todo.dto.ts
│   │   │   ├── entities/
│   │   │   │   └── todo.entity.ts (ou todo.schema.ts si vous utilisez Mongoose)
│   │   │   ├── todos.controller.ts
│   │   │   ├── todos.module.ts
│   │   │   └── todos.service.ts
│   │   ├── main.ts
│   │   └── ... (autres fichiers backend)
│   ├── test/
│   │   └── ... (fichiers de test backend)
│   ├── nest-cli.json
│   ├── package.json
│   ├── README.md
│   ├── tsconfig.build.json
│   └── tsconfig.json
├── frontend/
│   ├── public/
│   │   └── ... (assets publics)
│   ├── src/
│   │   ├── App.js (ou App.tsx)
│   │   ├── components/
│   │   │   ├── TodoItem.js (ou TodoItem.tsx)
│   │   │   ├── TodoList.js (ou TodoList.tsx)
│   │   │   ├── ... (autres composants frontend)
│   │   ├── hooks/
│   │   │   └── ... (hooks personnalisés si vous en avez)
│   │   ├── pages/
│   │   │   └── ... (pages de l'application si vous utilisez React Router)
│   │   ├── App.css (ou autres fichiers de style)
│   │   ├── index.js (ou index.tsx)
│   │   └── ... (autres fichiers frontend)
│   ├── package.json
│   ├── README.md
│   └── ... (autres fichiers de configuration frontend)
├── .gitignore
├── LICENSE
└── README.md (ce fichier)


Tests
Backend
Naviguez vers le répertoire backend :

Bash


cd backend


Exécutez les tests unitaires :

Bash


npm run test


ou

Bash


yarn test


Exécutez les tests end-to-end :

Bash


npm run test:e2e


ou

Bash


yarn test:e2e


Frontend
Naviguez vers le répertoire frontend :

Bash


cd frontend


Exécutez les tests (en utilisant Jest et React Testing Library par défaut) :

Bash


npm test


ou

Bash


yarn test


Déploiement
Fournissez des détails sur la manière de déployer votre application. Cela pourrait inclure :
Instructions pour construire les bundles frontend et backend prêts pour la production.
Informations sur les plateformes d'hébergement (par exemple, Netlify, Vercel pour le frontend ; Heroku, DigitalOcean pour le backend).
Détails de configuration pour les variables d'environnement en production.
Contribution
Si vous souhaitez contribuer à ce projet, veuillez suivre ces directives :
Forkez le dépôt.
Créez une nouvelle branche pour votre fonctionnalité ou correction de bug (git checkout -b fonctionnalité/nom-de-votre-fonctionnalité).
Effectuez vos modifications et commitez-les (git commit -m 'Ajouter une fonctionnalité').
Poussez vers la branche (git push origin fonctionnalité/nom-de-votre-fonctionnalité).
Ouvrez une pull request.
Veuillez vous assurer que votre code respecte les normes de codage du projet et inclut des tests appropriés.
Licence
[Spécifiez votre licence ici, par exemple, Licence MIT]



Licence MIT

Copyright (c) [Année] [Votre Nom]

La permission est accordée, gratuitement, à toute personne obtenant une copie
de ce logiciel et des fichiers de documentation associés (le "Logiciel"), de traiter
le Logiciel sans restriction, y compris, sans limitation, les droits
d'utiliser, de copier, de modifier, de fusionner, de publier, de distribuer, de sous-licencier, et/ou de vendre
des copies du Logiciel, et de permettre aux personnes auxquelles le Logiciel est
fourni de le faire, sous les conditions suivantes :

La notice de copyright ci-dessus et la présente notice de permission doivent être incluses dans toutes
les copies ou parties substantielles du Logiciel.

LE LOGICIEL EST FOURNI "TEL QUEL", SANS GARANTIE D'AUCUNE SORTE, EXPRESSE OU
IMPLICITE, Y COMPRIS, MAIS SANS S'Y LIMITER, LES GARANTIES DE COMMERCIALISATION,
D'ADÉQUATION À UN USAGE PARTICULIER ET DE NON-CONTREFAÇON. EN AUCUN CAS, LES
AUTEURS OU TITULAIRES DU COPYRIGHT NE SERONT RESPONSABLES DE TOUTE RÉCLAMATION, DOMMAGE OU AUTRE
RESPONSABILITÉ, QU'ELLE DÉCOULE D'UN CONTRAT, D'UN DÉLIT OU AUTRE, DÉCOULANT DE,
DE OU EN RELATION AVEC LE LOGICIEL OU SON UTILISATION OU D'AUTRES TRANSACTIONS DANS LE
LOGICIEL.


N'oubliez pas de remplacer les espaces entre crochets (par exemple, <l'URL-de-votre-dépôt>, [Année] [Votre Nom], etc.) avec les informations spécifiques à votre projet. N'hésitez pas si vous avez d'autres questions !
Sources
1. https://github.com/YassineOularbi/STUDENT-MANAGEMENT-SPRINGBOOT-ANGULAR
2. https://github.com/aee-enssat/aee-connectors soumis à licence (MIT)
3. https://www.lokad.com/fr/calculer-l-effectif-du-centre-d-appel-avec-excel/
4. https://www.idrlabs.com/fr/test-politique-des-8-valeurs/test.php
5. https://enscape3d.com/fr/mentions-legales/
6. https://www.harmonie-mutuelle.fr/mentions-legales
