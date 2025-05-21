# 🎓 Projet Universitaire – Application de Quiz Interactif en JavaScript

## Description Générale

Ce projet a été réalisé dans le cadre du module **Programmation Web II : JavaScript** à la **Faculté des Sciences Semlalia - Université Cadi Ayyad**. Il s'inscrit dans une démarche pédagogique visant à renforcer les compétences des étudiants en conception d'interfaces interactives, en manipulation du DOM, et en gestion des événements utilisateur à travers JavaScript moderne (ES6+), HTML5 et CSS3.

---

## Encadrement Pédagogique

* **Enseignant :** Pr. Abdelmoula Abouhilal
* **Année universitaire :** 2024 – 2025
* **Filière :** MIP
* **Module :** Programmation Web II

---

## Équipe de Développement : Groupe ASADAT

| Nom complet         | Numéro d'apogée   | Rôle / Contribution principale                  |
| ------------------- | ----------------- | ----------------------------------------------- |
| BAHAIDA Salma       | 2226601           | Structure HTML du quiz (index.html) : balisage, |
|                     |                   | accessibilité,organisation du contenu           |
| EL HASOUBI Soukaina | 2130126           | Feuille de style (styles.css) : mise en page,   |
|                     |                   | couleurs, responsive design                     |
| ELMOUHIB Ikram      | 2125072           | Fichier des questions (questions.js) : rédaction|
|                     |                   | des questions, réponses, explications           |
| TARAKA Fatimeezahra | 2330910           | Logique JavaScript (script.js) : fonctionnement |
|                     |                   | du quiz, interactions, minuterie                |

---

## Objectifs Pédagogiques

* Maîtriser la manipulation dynamique du DOM avec JavaScript ES6+.
* Structurer un projet web selon les bonnes pratiques (séparation HTML/CSS/JS).
* Améliorer l'UX via timers, transitions, et animations CSS.
* Travailler en équipe avec gestion collaborative (Git/GitHub).
* Documenter proprement un projet logiciel à vocation académique.

---

## Objectifs du Projet

Créer une application de quiz interactif permettant aux utilisateurs de tester leurs connaissances en JavaScript, avec les fonctionnalités suivantes :

* Interface conviviale avec HTML/CSS/JS.
* Chargement dynamique des questions depuis un fichier questions.js.
* Prise en charge du score en temps réel.
* Minuteur par question (ex: 20 secondes).
* Rétroaction visuelle sur les réponses (bonnes/mauvaises).
* Affichage du résultat final avec un système d'explication dépliable (accordion).
* Stockage du prénom utilisateur pour personnalisation.
* Architecture modulaire ES6+.

---

## Fonctionnalités Principales

Interface utilisateur

   * Accueil personnalisé avec prénom
   * Progression question par question
   * Affichage dynamique des questions et choix
   * Minuteur intégré à chaque question (non inclus dans le code transmis, mais prévu)
   * Système de score instantané
   * Résultat final avec explications accessibles

Questions et Réponses

   * Questions définies dans un tableau JSON exporté via questions.js
   * Chaque question contient :
        L'intitulé
        Un tableau de réponses possibles
        L'indice de la bonne réponse
        Une explication

Styles

   * Design futuriste néon avec animations CSS
   * Responsive mobile avec media queries


---

## Technologies Utilisées

| Technologie                   | Usage                                         |
| ----------------------------- | --------------------------------------------- |
| **HTML5**                     | Structure sémantique de l'application         |
| **CSS3**                      | Mise en page, transitions, animations         |
| **JavaScript ES6+**           | Logique de quiz, gestion du DOM               |
| **Flexbox / Grid CSS**        | Logique de quiz, gestion du DOM               |
| **Git & GitHub**              | Versioning, collaboration                     |
| **localStorage**              | prénom utilisateur                            |
| **Aucune dépendance externe** | Application 100% native, légère et performante|

---

## Structure du Projet

```
📁 /quiz-interactif/
├── index.html        → Structure de l’application (HTML5 sémantique)
├── style.css         → Design responsive et animations (CSS3)
├── script.js         → Logique du quiz (ES6+, DOM, timers)
├── questions.js      → Base de données locale des questions
├── README.md         → Documentation du projet
└── sounds/           → Dossier des sons intégrés
    ├── welcome.mp3     (son d'accueil)
    ├── correct.mp3     (son court de bonne réponse)
    ├── wrong.mp3       (son court de mauvaise réponse)
    └── end.mp3         (son de fin motivant)
```


---

## Détails techniques

➔ Gestion du temps
   * Implémentée avec setInterval() et clearInterval()
   * Blocage automatique du clic utilisateur après 15s
   * Affichage dynamique du compteur sur l’interface

➔ Manipulation du DOM
   * Sélection des éléments via querySelector() / querySelectorAll()
   * Ajout/suppression de classes CSS pour le feedback utilisateur
   * Création dynamique des balises HTML pour les options et explications

➔ Architecture modulaire
   * questions.js contient un tableau d’objets (question, options, bonne réponse, explication)
   * script.js orchestre la logique du quiz, la gestion du timer, du score, et du DOM

➔ Accessibilité
   * Contrastes de couleurs respectés (WCAG AA)
   * Structure HTML logique (titres, listes, boutons)
   * Navigation clavier fonctionnelle (tabulation, focus visible)
   * Rôles ARIA aux éléments interactifs (si applicable)

---



##  Instructions d’Utilisation

1. **Cloner le projet**

```bash
git clone https://github.com/soukaina-elhasoubi/quiz-interactif
cd quiz-interactif
```

2. **Lancer dans le navigateur**

Ouvrir simplement le fichier `index.html` avec un navigateur moderne (Chrome, Firefox, Edge).

---

## Ajout de Questions (personnalisation facile)

Dans `questions.js`, les questions sont définies sous forme d'un tableau d'objets :

```js
const questions = [
  {
    question: "Que fait la méthode JavaScript 'Array.prototype.map()' ?",
    answers: [
      "Elle transforme chaque élément du tableau en fonction d'une fonction",
      "Elle trie le tableau",
      "Elle filtre les éléments selon une condition",
      "Elle ajoute un élément à la fin du tableau",
    ],
    correct: 0,
    explanation: "La méthode 'map()' crée un nouveau tableau avec les résultats de l'appel d'une fonction sur chaque élément du tableau original.",
  },
  // autres questions...
];
```

---

## Améliorations Possibles

* Sauvegarde du score et du temps dans localStorage
* Ajout de badges de performance ou niveaux de difficulté
* Export du résultat final en format PDF
* Intégration de support audio pour chaque question (accessibilité accrue)
* Version multilingue (fr, en, ar)
* Mode "duel" ou "challenge" entre deux utilisateurs (via WebSocket/Firebase)
* Intégration d’un tableau de classement (leaderboard)

---

## Bonnes Pratiques Respectées

* Utilisation de `const` et `let`, pas de `var`
* Code commenté, clair, fonctions nommées explicitement
* Accessibilité (navigation clavier, ARIA tags)
* Responsive Design via Flexbox/Grid + media queries
* Validation W3C HTML/CSS

---

## Inspirations pédagogiques

Le projet s’appuie sur des approches d’apprentissage par l’expérience et le renforcement par l’erreur expliquée. Le système d’accordéon présentant les explications favorise la réflexion métacognitive et la mémorisation à long terme.

---

## Ressources Pédagogiques

* [MDN Web Docs (JavaScript)](https://developer.mozilla.org/fr/docs/Web/JavaScript)
* [CSS Tricks - Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [GitHub Education Pack](https://education.github.com/pack)
* [W3C Validator](https://validator.w3.org/)

---

## Licence

Ce projet est à usage **strictement académique**. Toute reproduction ou réutilisation dans un autre contexte doit mentionner les auteurs et l'établissement d'origine.

---

## Remerciements

Nous exprimons notre sincère gratitude à **Pr. Abdelmoula Abouhilal** pour sa pédagogie, son suivi constant et son engagement envers la réussite des étudiants.

---



## Groupe ASADAT
---