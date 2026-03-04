# Exercice JavaScript - Création dynamique de contenus Bootstrap

## Objectif

L'objectif de cet exercice est de pratiquer la création dynamique de contenus HTML en utilisant JavaScript. Vous allez générer dynamiquement trois colonnes Bootstrap (`col-12 col-md-4`) à partir d'un tableau de données, chacune contenant une image, un titre et un paragraphe.

## Instructions

1. Créez un fichier HTML nommé `index.html`.

2. Créez une structure HTML de base avec les balises `<html>`, `<head>` et `<body>`.

3. Dans le `<head>`, liez Bootstrap CSS et Google Fonts directement dans le HTML (via des balises `<link>`).

4. Dans le `<body>`, créez uniquement la structure conteneur Bootstrap :
   - Une `<div class="container">` englobante
   - À l'intérieur, une `<div class="row">` qui restera **vide côté HTML** — c'est JavaScript qui y injectera les colonnes.

5. Écrivez un script JavaScript pour créer et injecter dynamiquement les colonnes dans la `row` :
   - Déclarez un tableau `data` au format JSON contenant 3 objets, chacun avec les propriétés `image`, `title` et `text`. Voici un exemple de structure attendue (avec une seule entrée) :
     ```json
     [
       {
         "image": "https://exemple.com/photo.jpg",
         "title": "Mon titre",
         "text": "Mon paragraphe de description."
       }
     ]
     ```
   - Récupérez la `div.row` dans le DOM via `querySelector`.
   - Parcourez le tableau avec `forEach` et, pour chaque élément :
     - Créez une `<div>` colonne avec les classes `col-12 col-md-4` (responsive : pleine largeur sur mobile, 1/3 sur écran moyen et plus).
     - Créez une balise `<img>` avec les attributs `src` et `alt`.
     - Créez une balise `<h3>` avec le titre, et ajoutez-lui la classe Bootstrap `text-primary`.
     - Créez une balise `<p>` avec le texte descriptif.
     - Ajoutez ces trois éléments à la colonne avec `appendChild`.
     - Ajoutez la colonne à la `row` avec `appendChild`.

6. Ajoutez des styles CSS dans une balise `<style>` dans le `<head>` pour personnaliser l'apparence des colonnes (fond blanc, padding, bordure simulant un espacement, etc.).

7. Testez votre page dans un navigateur pour vous assurer que les trois colonnes s'affichent correctement côte à côte (sur écran md+) avec le bon style et les images.

## Données à utiliser

Voici les contenus à intégrer dans votre tableau `data` :

| # | Image | Titre | Texte |
|---|-------|-------|-------|
| 1 | `https://picsum.photos/600/400?random=101` | Exploration Urbaine | Partez à la découverte des paysages urbains et de l'architecture moderne à travers cette vue captivante. |
| 2 | `https://picsum.photos/600/400?random=102` | Nature & Détente | Un moment de calme et de fraîcheur au cœur d'une nature apaisante. Respirez profondément. |
| 3 | `https://picsum.photos/600/400?random=103` | Technologie en Mouvement | Plongez dans le futur avec cette illustration dynamique du progrès technologique. |

## Bonus

- Ajoutez une transition CSS sur les colonnes pour créer un effet de survol (`transform: translateY`) lorsque la souris passe dessus.
- Expérimentez avec différentes classes Bootstrap pour enrichir le rendu visuel.
