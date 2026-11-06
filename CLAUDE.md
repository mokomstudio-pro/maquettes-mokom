# Maquettes Site Express — Mokom Studio

## Contexte
Ce dépôt contient le catalogue de maquettes de l'offre « Site Express » de Mokom Studio (Morgane, webdesigner à Bordeaux). Il est publié sur GitHub Pages à l'adresse https://maquettes.mokomstudio.fr (fichier `CNAME`). Morgane n'est pas développeuse : explique en termes simples, propose la meilleure option, ne pose une question que si c'est bloquant.

## Structure
- `index.html` : vitrine des 11 thèmes (cadres navigateur / téléphone, sélecteur Exemple A / B, liste des pages, fonctionnalités). Les thèmes sont décrits dans le tableau `THEMES` du script en bas du fichier.
- Un fichier `.html` par page de maquette. Nommage : `<client>.html` (accueil), `<client>-<page>.html` (page intérieure), `<client>-mentions-legales.html`.
- `img/` : photos Pexels libres de droits, nommées `<prefixe>-<usage>.jpg`, ≤ 1 600 px, qualité 78.
- `CNAME`, `.nojekyll` : nécessaires à GitHub Pages. Ne pas supprimer.

## Les 11 thèmes (exemple A / exemple B)
01 artisan `atelier-bardou` / `delmas-electricite` · 02 commerce `maison-oriol` / `boulangerie-lacoste` · 03 restaurant `cantine-du-port` / `marcel-burger` · 04 beauté `maison-louve` / `costa-barbier` · 05 praticien `cabinet-roux` / `anais-verdier-avocate` · 06 indépendant `lea-marchand` / `karim-benali-formateur` · 07 sport `alto-coaching` / `studio-ananda` · 08 hébergement `maison-calmel` / `camping-les-dunes` · 09 portfolio `theo-lanvin` / `nour-haddad-interieur` · 10 boutique `etale` / `terre-et-feu` · 11 carte de visite `atelier-pivoine` / `garage-martin`.

## Règles
- Chaque page est autonome : HTML + CSS dans le même fichier, polices via Google Fonts, aucune autre dépendance externe.
- Toutes les pages gardent `<meta name="robots" content="noindex, nofollow">` : ce sont des entreprises fictives, elles ne doivent jamais être indexées.
- Chaque maquette garde le bandeau `#mokom-demo` (masqué automatiquement dans un cadre).
- Les couleurs et polices d'un thème sont dans `:root` et le lien Google Fonts en haut du fichier ; une variante se fait en changeant ces valeurs et le contenu, jamais la structure.
- Chaque page doit rester lisible à 390 px de large (aucun débordement horizontal) et à 1 280 px.
- Ne pas renommer un fichier existant sans mettre à jour `index.html` (tableau `THEMES`) et les liens internes.
- Photos : uniquement libres de droits (Pexels, Unsplash) ; jamais de photo de personne réelle identifiable issue du web pour un vrai client.

## Ajouter un thème ou une variante
1. Dupliquer la page la plus proche, changer `:root`, les polices, les textes, les photos, le `<title>` (« Maquette personnalisable pour [thème] »).
2. Ajouter les photos dans `img/` (compressées).
3. Ajouter l'entrée dans `THEMES` de `index.html` (titre, fichier, url fictive, action, description, pages, fonctionnalités, alt pour l'exemple B).
4. Vérifier à 390 px et 1 280 px, puis `git add . && git commit -m "..." && git push`.

## Mise en ligne
GitHub Pages, branche `main`, racine. Après chaque `git push`, le site est à jour en 1 à 2 minutes.
