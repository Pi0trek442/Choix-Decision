# 🎯 Sélecteur & Comparateur d'Options Intelligents

Une application web légère, moderne et sans dépendance externe, conçue pour faciliter la prise de décision. Que ce soit pour choisir un plat, classer des priorités ou départager des idées, l'outil propose plusieurs méthodes de comparaison adaptées à chaque besoin.

## 🚀 Fonctionnalités

- **Saisie simple** : Entrez vos options séparées par des virgules.
- **Interface responsive & moderne** : Design épuré avec animations fluides.
- **Multiples algorithmes de choix** : Du classement exhaustif au tirage aléatoire immédiat.
- **Sécurité cryptographique** : Génération d'aléa basée sur l'API Web Crypto.

---

## 🧠 Nuances des algorithmes de tri disponibles

Chaque méthode répond à une contrainte spécifique (précision, vitesse ou neutralité). Voici comment elles fonctionnent :

### 1. Tous les duels (Round-Robin)
- **Principe** : Compare chaque élément individuellement contre tous les autres éléments de la liste.
- **Complexité** : $\frac{n(n - 1)}{2}$ duels.
- **Cas d'usage** : Idéal pour les petites listes (< 6 éléments). C'est la méthode la plus exhaustive et précise pour obtenir un classement complet avec comptage de points.

### 2. Tri Fusion (Merge Sort)
- **Principe** : Algorithme de tri dichotomique (« diviser pour régner »). Il découpe la liste en sous-groupes et demande des arbitrages uniquement lorsque c'est nécessaire.
- **Complexité** : $O(n \log n)$ comparaisons.
- **Cas d'usage** : Optimal pour les listes moyennes à longues (6 à 20+ éléments). Il réduit considérablement le nombre de duels requis par rapport au Round-Robin en déduisant la logique des choix précédents.

### 3. Arbre d'élimination (Tinder-like / Bracket)
- **Principe** : Fonctionne sous forme de tournoi à élimination directe. Les éléments s'affrontent 2 par 2 : le perdant est immédiatement éliminé, le gagnant passe au tour suivant.
- **Complexité** : $n - 1$ duels.
- **Cas d'usage** : Parfait pour isoler uniquement le **Grand Vainqueur (Top 1)** le plus rapidement possible, sans perdre de temps à classer les éléments secondaires.

### 4. Tirage Random (Vrai Hasard)
- **Principe** : Sélectionne immédiatement un élément au hasard dans la liste.
- **Garantie mathématique** : Contrairement au `Math.random()` classique (pseudo-aléatoire), cette option exploite `window.crypto.getRandomValues()`. Cela garantit un tirage basé sur l'entropie matérielle du système, parfaitement uniforme et impartial.

---

## 🛠️ Utilisation

Ouvrez simplement le fichier `index.html` dans n'importe quel navigateur web moderne. Aucun serveur ni installation de paquet n'est requis.
