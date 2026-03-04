# Exercice JavaScript - Création dynamique de contenus Bootstrap

## Objectif

L'objectif de cet exercice est de pratiquer la création dynamique de contenus HTML en utilisant JavaScript. Vous allez générer dynamiquement trois colonnes Bootstrap (`col-12 col-md-4`) à partir d'un tableau de données, chacune contenant une image, un titre, un paragraphe et un lien hypertexte.

![Final](https://sebastien-devos.fr/img/codegt/dynamic-bootstrap.png)

## Instructions

1. Créez un fichier HTML nommé `index.html`.

2. Créez une structure HTML de base avec les balises `<html>`, `<head>` et `<body>`.

3. Dans le `<head>`, liez Bootstrap CSS et Google Fonts directement dans le HTML (via des balises `<link>`).

4. Dans le `<body>`, créez uniquement la structure conteneur Bootstrap :
   - Une `<div class="container">` englobante
   - À l'intérieur, une `<div class="row">` qui restera **vide côté HTML** — c'est JavaScript qui y injectera les colonnes.

5. Écrivez un script JavaScript dans un fichier `main.js` pour créer et injecter dynamiquement les colonnes dans la `row` :
   
   - Déclarez un tableau `data` au format JSON contenant 3 objets, chacun avec les propriétés `image`, `title`, `text` et `link`.
  
   ```js
     const data = [
      {
        /* Objet 1 */
      },
      {
        /* Objet 2 */
      },
      {
        /* Objet 3 */
      }
    ];
   ```
     
   - Voici un exemple de structure attendue (avec une seule entrée) :
     
     ```json
     [
       {
         "image": "https://exemple.com/photo.jpg",
         "title": "Mon titre",
         "text": "Mon paragraphe de description.",
         "link": "https://exemple.com"
       }
     ]
     ```
     
   - Récupérez la `div.row` dans le DOM via `querySelector`.
     
   - Parcourez le tableau avec `forEach` et, pour chaque élément :
     - Créez une `<div>` colonne avec les classes `col-12 col-md-4`.
     - Créez une balise `<img>` avec les attributs `src` et `alt`.
     - Créez une balise `<h3>` avec le titre, et ajoutez-lui la classe Bootstrap `text-primary`.
     - Créez une balise `<p>` avec le texte descriptif.
     - Créez une balise `<a>` avec l'attribut `href` pointant vers l'URL de la propriété `link`, un texte de lien explicite, et l'attribut `target="_blank"` pour l'ouvrir dans un nouvel onglet.
     - Ajoutez ces quatre éléments à la colonne avec `appendChild`.
     - Ajoutez la colonne à la `row` avec `appendChild`.

7. Ajoutez des styles CSS dans une fichier `style.css` pour personnaliser l'apparence des colonnes (fond blanc, padding, bordure simulant un espacement, etc.).

8. Testez votre page dans un navigateur pour vous assurer que les trois colonnes s'affichent correctement côte à côte (sur écran md+) avec le bon style et les images.

## Données à utiliser

Voici les contenus à intégrer dans votre tableau `data` :

| # | Image | Titre | Texte | Lien |
|---|-------|-------|-------|------|
| 1 | `https://picsum.photos/600/400?random=101` | Exploration Urbaine | Partez à la découverte des paysages urbains et de l'architecture moderne à travers cette vue captivante. | `https://www.nyc.gov` |
| 2 | `https://picsum.photos/600/400?random=102` | Nature & Détente | Un moment de calme et de fraîcheur au cœur d'une nature apaisante. Respirez profondément. | `https://www.ffrandonnee.fr` |
| 3 | `https://picsum.photos/600/400?random=103` | Technologie en Mouvement | Plongez dans le futur avec cette illustration dynamique du progrès technologique. | `https://www.anthropic.com` |

## Bonus

- Ajoutez une transition CSS sur les colonnes pour créer un effet de survol (`transform: translateY`) lorsque la souris passe dessus.
- Expérimentez avec différentes classes Bootstrap pour enrichir le rendu visuel.
