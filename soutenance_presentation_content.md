#  Contenu Détaillé de la Présentation Orale (15 minutes)

## Slide 1 : Titre

**Titre :** Soutenance d'Intégration HTML/CSS - Projet Booki **Sous-titre :** Page d'accueil et Responsive Design

## Slide 2 : Contexte du Projet

**Titre :** Rappel du Contexte et des Objectifs

- **Quoi :** Intégration de la page d'accueil du site Booki.

- **Pourquoi :** Permettre aux usagers de trouver des hébergements et des activités dans la ville de leur choix.

- **Pour Qui :** Les utilisateurs finaux de la plateforme Booki.

- **Objectif de cette version :** Valider l'interface utilisateur et la structure technique avant le développement des fonctionnalités (recherche non fonctionnelle, filtres non fonctionnels).

- **Livrables :** Fichiers `index.html` et `css/style.css` intégrant les maquettes desktop, tablette et mobile.

## Slide 3 : Spécifications Techniques Clés

**Titre :** Respect des Contraintes Techniques

- **Approche :** **Desktop First** (intégration prioritaire pour les écrans d'ordinateurs).

- **Mise en page :** Utilisation exclusive de **Flexbox** pour la structure et l'alignement des éléments.

- **Responsive Design :** Mise en œuvre des **Media Queries** pour les breakpoints :
  - `> 1024px` : Desktop
  - `<= 1024px` : Tablette
  - `< 768px` : Mobile

- **Largeur :** Contenu centré avec une largeur maximale de **1440px**.

- **Restrictions :** **Aucun framework** (Bootstrap, Tailwind) ni préprocesseur (Sass) utilisé. Code HTML sans propriétés CSS.

## Slide 4 : Rendu Visuel - Version Desktop

**Titre :** Intégration de la Maquette Desktop

- **Point clé :** La structure principale en deux colonnes (Hébergements à gauche, Populaires à droite) est réalisée via Flexbox.

- **Détails :** Respect de la charte graphique (couleurs, police Raleway, icônes Font Awesome).

- **Démonstration :** Afficher la version Desktop (largeur > 1024px).

## Slide 5 : Rendu Visuel - Versions Tablette et Mobile

**Titre :** Adaptation Responsive (Tablette et Mobile)

- **Tablette (****`<= 1024px`****) :**
  - Passage de la structure principale en **une seule colonne** (Hébergements puis Populaires).
  - Les cartes "Populaires" passent en affichage horizontal pour optimiser l'espace.

- **Mobile (****`< 768px`****) :**
  - Réorganisation de l'en-tête (navigation verticale).
  - Le bloc "Populaires" est placé **avant** le bloc "Hébergements" (inversion de l'ordre Flexbox).
  - Le bouton de recherche affiche uniquement l'icône loupe pour gagner de la place.

- **Démonstration :** Afficher les versions Tablette et Mobile.

## Slide 6 : Présentation du Code - HTML Sémantique

**Titre :** Structure HTML et Sémantique

- **Choix Sémantiques :** Utilisation des balises recommandées :
  - `header` et `nav` pour l'en-tête et la navigation.
  - `main` pour le contenu principal.
  - `section` pour les blocs majeurs (`search-section`, `hebergements`, `populaires`, `activites`).
  - `article` pour les cartes d'hébergement et d'activité.
  - `footer` pour le pied de page.

- **Accessibilité :** Utilisation de l'attribut `alt` pour toutes les images et de `aria-hidden="true"` pour les icônes décoratives.

## Slide 7 : Présentation du Code - CSS et Flexbox

**Titre :** Organisation du Style CSS

- **Flexbox :** Utilisation intensive pour la mise en page (en-tête, filtres, cartes, structure principale).

- **Variables CSS :** Définition des couleurs principales (`--main-color`, `--main-bg-color`, etc.) pour une maintenance facilitée.

- **Media Queries :** Structure claire des requêtes pour gérer les changements de mise en page aux breakpoints 1024px et 768px.

## Slide 8 : Points Complexes et Solutions

**Titre :** Défis d'Intégration et Solutions

- **Défi 1 :** Gestion de la structure principale (Hébergements/Populaires) en deux colonnes sur Desktop et une colonne sur Mobile/Tablette.
  - **Solution :** Utilisation de `display: flex` sur le conteneur parent (`.hebergements-and-populaires`) et de `flex-direction: column` dans la Media Query Tablette/Mobile.

- **Défi 2 :** Inversion de l'ordre des sections "Hébergements" et "Populaires" sur Mobile.
  - **Solution :** Utilisation de `flex-direction: column-reverse` dans la Media Query Mobile.

- **Défi 3 :** Adaptation du bouton de recherche.
  - **Solution :** Utilisation de `display: none` et `display: inline` sur les classes `.search-button-text` et `.search-icon` dans la Media Query Mobile.

## Slide 9 : Bilan du Projet

**Titre :** Bilan et Prochaines Étapes

- **Succès :** Toutes les spécifications techniques et fonctionnelles de l'interface ont été respectées. Le code est propre, sémantique et valide W3C.

- **Maintenabilité :** L'utilisation de Flexbox et des variables CSS assure une bonne maintenabilité et évolutivité du code.

- **Prochaines Étapes :**
  - Intégration des fonctionnalités JavaScript (recherche, filtres).
  - Développement des autres pages du site.
  - Tests d'accessibilité approfondis.

---

*Fin de la présentation de 15 minutes.*

