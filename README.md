# 📘 N stream – Guide complet du projet

*Un Netflix perso, open-source et auto-hébergé.*

---

## 1. Présentation du projet

**N stream** est une plateforme de streaming vidéo personnelle, conçue pour rassembler et organiser tes films et séries préférés dans une interface élégante, inspirée des grandes plateformes (Netflix, Disney+).

### Objectifs
- Centraliser des liens de lecture (Tokyvideo, etc.) dans un catalogue unifié.
- Gérer **plusieurs profils** avec des recommandations personnalisées.
- Sauvegarder **la progression de visionnage** (films et séries).
- Permettre **l’ajout collaboratif** de films via GitHub.
- Offrir une **expérience immersive** (bande-annonce au survol, mode TV, etc.).

### Technologies utilisées
- **HTML / CSS / JavaScript** (Vanilla) – pas de framework, léger et rapide.
- **LocalStorage** pour la persistance locale.
- **GitHub API** pour le partage de listes de films.
- **Telegram Bot API** pour recevoir les demandes de films.
- **Tokyvideo** comme source d’hébergement vidéo (embed).

---

## 2. Fonctionnalités principales

### 🧑‍🤝‍🧑 Profils multiples
- Chaque utilisateur a son propre avatar, son code PIN, sa liste personnelle, sa progression.
- Les profils pré‑définis (Oscar, Jules, Frank, Valérie, Félix, Invité) ont des goûts distincts, influençant les recommandations.

### 📺 Catalogue de films
- Plus de **400 films** pré‑chargés (dont des classiques, des nouveautés et des exclusivités).
- Chaque film possède : titre, année, catégorie, affiche, lien d’embed Tokyvideo.
- Filtres par **genre**, **période** et **tri** (récent, ancien, alphabétique).

### ➕ Ma liste
- Chaque profil peut ajouter ou retirer des films de sa liste personnelle.
- Accès rapide depuis la navigation.

### 🎬 Lecture et progression
- Lancement d’un film en cliquant sur sa carte.
- La progression (pourcentage visionné) est sauvegardée automatiquement.
- Reprise de la lecture là où on s’était arrêté.

### 📺 Série « Prison Break »
- Intégration complète des **3 saisons** (57 épisodes) avec suivi de progression.
- Bouton « Reprendre » pour enchaîner automatiquement les épisodes.
- Interface de sélection par saison et par épisode.

### 📅 Section « À venir »
- Liste des sorties prévues en 2026 avec affiches et dates (ex: *Toy Story 5*, *Avengers: Doomsday*).

---

## 3. Ajout et partage de films

### 📄 Fichier externe `film.txt` (GitHub)
- Le projet peut lire un fichier texte hébergé sur GitHub (`ajouts-films.txt`).
- Format attendu (une ligne par film) :  
  `Titre du film | Année | Lien d’embed | Catégorie (optionnel) | Affiche (optionnel)`
- Exemple :  
  `Le Comte de Monte-Cristo | 2024 | https://www.tokyvideo.com/fr/embed/759955 | Aventure`

### ✏️ Ajout via l’interface
- Un formulaire dans les préférences permet d’ajouter un film directement.
- Il faut fournir : titre, année, le code d’intégration Tokyvideo (ou l’URL), et un **token GitHub** (pour écrire dans le dépôt).
- Le film est ajouté au fichier `ajouts-films.txt`, et le catalogue est mis à jour automatiquement.

### 🔄 Synchronisation en temps réel
- Une API distante (optionnelle) peut synchroniser les profils, la liste et la progression entre plusieurs appareils.

---

## 4. Expérience utilisateur

### 🎨 Thèmes et animations
- Personnalisation de la couleur d’accent (bleu, violet, émeraude, rose, ambre).
- Option pour désactiver les animations fluides (réduction de mouvement).
- Bande‑annonce au survol de l’affiche (sur l’écran d’accueil).

### 📱 Interface adaptative
- Responsive : s’adapte aux mobiles, tablettes et grands écrans.
- Navigation tactile et au clavier.

### 🖥️ Mode Télévision
- Optimisé pour les télécommandes (navigation par flèches, sélection par Entrée).
- Cache automatiquement le curseur après quelques secondes.
- Support du plein écran et du verrouillage du pointeur.

---

## 5. Configuration et installation

### 🔧 Prérequis
- Un navigateur moderne (Chrome, Firefox, Edge, Safari).
- Un compte GitHub (pour les ajouts) et un bot Telegram (optionnel).

### 📦 Mise en place
1. Télécharge le code source (fichier `index.html` et ressources).
2. Ouvre le fichier dans un navigateur.
3. Choisis un profil (ou utilise le profil Invité).
4. Configure les préférences (couleur, animations, etc.).
5. (Optionnel) Lie un dépôt GitHub pour les ajouts collectifs.
6. (Optionnel) Connecte un bot Telegram pour recevoir les demandes de films.

### 🔒 Sécurité
- Les codes PIN sont stockés sous forme de hash SHA‑256.
- Le token GitHub et les identifiants Telegram sont stockés localement (dans le navigateur).

---

## 6. Conclusion et perspectives

**N stream** est un projet vivant, évolutif et centré sur l’utilisateur. Il permet de :

- Regrouper ses contenus préférés en un seul endroit.
- Partager et enrichir le catalogue en communauté.
- Profiter d’une interface moderne et réactive.

### Idées d’amélioration
- Ajout de sous‑titres et de pistes audio.
- Support d’autres sources vidéo (Vimeo, Dailymotion, etc.).
- Intégration d’un moteur de recommandation plus avancé.
- Export/import des données en JSON.

---

## 7. Remerciements

- **Tokyvideo** pour l’hébergement des vidéos.
- **GitHub** pour le partage de fichiers.
- **Telegram** pour les notifications.
- La communauté open‑source pour l’inspiration.

---

**N stream – Fait avec ❤️ par Boo et la communauté.**  
*Version 1.0 – 2026*

---
