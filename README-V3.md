# Destinations GPS — V3

V3 avec recherche Google Places / Google Maps, favoris locaux et lancement Google Maps ou Waze.

## 1. Google Maps Platform

Dans Google Cloud :

1. Créer ou sélectionner un projet.
2. Activer la facturation pour un usage standard en production.
3. Activer **Maps JavaScript API**.
4. Activer **Places API (New)**.
5. Créer une clé API.
6. Restreindre la clé aux **Sites Web (HTTP referrers)**.
7. Autoriser au minimum :
   - `https://mgresset.github.io/*`
   - ou plus restrictif si votre navigateur/referrer le permet : `https://mgresset.github.io/destinations-gps/*`
8. Dans les restrictions d'API, n'autoriser que **Maps JavaScript API** et **Places API (New)**.

## 2. Ajouter la clé dans VS Code

Ouvrir `index.html`, chercher :

```js
const GOOGLE_MAPS_API_KEY = 'PASTE_YOUR_GOOGLE_MAPS_API_KEY_HERE';
```

Remplacer uniquement la valeur entre apostrophes par votre clé.

## 3. Publier depuis VS Code

Après avoir cloné le dépôt GitHub :

```bash
git add index.html
git commit -m "V3 recherche Google Places"
git push
```

GitHub Pages republiera automatiquement la branche configurée.

## Fonctionnalités V3

- Recherche de lieux et adresses dans Google Places.
- Résultats Google Maps intégrés dans l'interface.
- Recherche simultanée dans les favoris.
- Sélection d'un lieu puis `Itinéraire` ou `+ Favori`.
- Le bouton `+` permet aussi de rechercher une adresse dans Google Maps avant l'enregistrement.
- Sauvegarde locale des favoris.
- Coordonnées GPS conservées lorsqu'un lieu Google Places est sélectionné.
- Lancement Google Maps ou Waze.
- Migration automatique des favoris V2.
