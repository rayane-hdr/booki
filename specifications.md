# Spécifications Techniques et Fonctionnelles - Projet Booki

Ce document résume les spécifications extraites de la Note de Synthèse (PDF) et des maquettes Figma, servant de guide pour l'intégration HTML/CSS.

## 1. Spécifications Fonctionnelles

| Fonction | Description |
| :--- | :--- |
| **Recherche** | Champ de saisie éditable, englobé dans un formulaire. La fonctionnalité n'est pas à implémenter (première version d'interface). |
| **Liens d'en-tête** | Les textes "Hébergements" et "Activités" sont des liens menant respectivement vers la section "Hébergements à Marseille" et "Activités à Marseille". Utiliser `href="#"`. |
| **Cartes** | Chaque carte d'hébergement ou d'activité doit être cliquable dans son intégralité. Utiliser `href="#"`. |
| **Filtres** | Les filtres (Budget, Ambiance, etc.) doivent changer de couleur au survol de la souris. La fonctionnalité n'est pas à implémenter. |

## 2. Spécifications Techniques

### 2.1. Design et Mise en Page

| Thème | Spécification |
| :--- | :--- |
| **Breakpoints** | Desktop: > 1024 px. Tablette: >= 768 px. Mobile: < 768 px. |
| **Largeur Max** | 1440 px. Au-delà, une marge blanche doit apparaître sur les côtés. |
| **Largeur Min** | 320 px. |
| **Approche** | **Desktop First** (intégration pour les ordinateurs en premier). Utilisation de Media Queries. |
| **Mise en page** | Recommandation d'utiliser **Flexbox**. |
| **Couleurs** | Bleu: `#0065FC` (variable CSS `--main-color`). Bleu clair: `#DEEBFF` (variable CSS `--filter-bg-color`). Gris de fond: `#F2F2F2` (variable CSS `--main-bg-color`). |
| **Police** | Raleway (importée via Google Fonts). |
| **Icônes** | Bibliothèque **Font Awesome**. |

### 2.2. Validité et Restrictions du Code

| Restriction | Description |
| :--- | :--- |
| **Balises** | Utiliser des balises sémantiques : `header`, `nav`, `h1-h2-h3`, `main`, `section`, `article`, `footer`. |
| **Validité** | Le code doit être valide aux validateurs W3C HTML et CSS. |
| **HTML/CSS** | Le code HTML ne doit pas contenir de propriété CSS. |
| **Duplication** | Ne pas dupliquer le code HTML lors du passage au responsive (sauf pour le mot "Rechercher" et l'icône de la loupe dans le formulaire). |
| **Classes CSS** | Privilégier l'utilisation des classes CSS pour cibler un élément. Ne pas dupliquer les classes CSS inutilement. |
| **Frameworks** | **Aucun framework CSS** (Bootstrap, Tailwind CSS) ou préprocesseur (Sass, Less) ne doit être utilisé. |
| **Langages** | **Aucun autre langage** (comme JavaScript) ne doit être utilisé. |
| **Compatibilité** | Compatible avec les dernières versions de Google Chrome et Mozilla Firefox. |

## 3. Analyse des Maquettes Figma

Les maquettes montrent la structure suivante pour la page d'accueil :
1.  **En-tête (`header`)** : Logo Booki et navigation (`nav`) avec liens "Hébergements" et "Activités".
2.  **Section principale (`main`)** :
    *   Titre principal (`h1`) et sous-titre.
    *   Formulaire de recherche.
    *   Filtres de recherche.
    *   Section **Hébergements à Marseille** (`section`):
        *   Contient la liste des hébergements les plus populaires.
        *   Affichage des cartes d'hébergement.
        *   Lien "Afficher plus".
    *   Section **Les plus populaires** (`section`):
        *   Contient une sélection d'hébergements populaires (colonne latérale).
        *   Affichage des cartes d'hébergement.
    *   Section **Activités à Marseille** (`section`):
        *   Contient la liste des activités.
        *   Affichage des cartes d'activité.
3.  **Pied de page (`footer`)** : Informations de contact et légales.

L'intégration doit se concentrer sur la mise en page de ces sections, en utilisant Flexbox pour organiser les éléments, notamment la section principale qui semble diviser le contenu en deux colonnes (Hébergements et Populaires).

---
*Note: Les images fournies dans le dépôt cloné (`booki-project/images`) seront utilisées pour l'intégration.*
