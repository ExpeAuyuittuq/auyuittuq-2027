# Expédition ᐊᐅᔪᐃᑦᑐᖅ · Auyuittuq 2027

Site de présentation de notre traversée à ski et pulka du col Akshayuk, dans le parc national Auyuittuq (Nunavut), en avril 2027. Il sert surtout à trouver des partenaires pour nous équiper.

- **Site :** https://expe-auyuittuq.ca
- **Équipe :** 7 amis, 4 de Montréal et 3 du Nunavut
- **Itinéraire :** Qikiqtarjuaq → Pangnirtung, 100 km à ski, 8 jours de voyage dont 5 à ski, jusqu'à −40 °C
- **Contact :** dorianecara2@gmail.com

## Contenu du dépôt

```
index.html      le site complet (textes FR/EN, styles et animations)
404.html        la page affichée quand une adresse n'existe pas
*.jpg           les photos
*.png           les dessins du carnet et les mots écrits à la main
*.svg           les illustrations et le favicon
maroni.woff     la police des titres
CNAME           le nom de domaine (ne pas supprimer, sinon le domaine se débranche)
robots.txt      \
sitemap.xml     /  pour les moteurs de recherche
README.md       ce fichier
```

Le site est un simple fichier HTML, sans base de données ni étape de compilation. Les autres polices viennent de Google Fonts.

## Mettre le site à jour

1. Ouvrir le dépôt sur GitHub.
2. Cliquer sur **Add file → Upload files**.
3. Glisser le nouveau `index.html`, ainsi que les nouvelles images s'il y en a. Les fichiers qui portent le même nom sont remplacés.
4. Cliquer sur **Commit changes**.

GitHub Pages republie le site automatiquement, en une à deux minutes. Si le changement n'apparaît pas, recharger la page en vidant le cache (Cmd/Ctrl + Maj + R).

Attention : en glissant un fichier qui existe déjà, vérifier qu'il porte bien le même nom. Un `index_1.html` ou un `photo_1.jpg` (nom donné par l'ordinateur à un doublon) crée un deuxième fichier au lieu de remplacer le premier.

### Modifier un texte rapidement

Ouvrir `index.html` sur GitHub et cliquer sur le crayon ✏️ pour l'éditer. Chaque texte existe en deux versions, une en français et une en anglais :

```html
<span class="fr">Texte en français</span><span class="en">English text</span>
```

Penser à modifier les deux, puis cliquer sur **Commit changes**.

Dans les textes français, `&nbsp;` est une espace insécable : elle empêche un « : », un « ? » ou une unité (km, °C) de se retrouver seul au début d'une ligne. La garder devant ces signes.

### Changer une photo

Remplacer le fichier par une nouvelle image **portant exactement le même nom**, par exemple `team-victor.jpg`. Format recommandé : JPEG d'environ 1600 px de large au maximum, et moins de 400 Ko si possible.

### Changer le statut d'un article de la liste de matériel

Dans le tableau, chaque ligne se termine par une étiquette :

```html
<span class="pill need">…</span>   recherché
<span class="pill part">…</span>   en partie
<span class="pill ok">…</span>     on l'a
```

Pour changer un statut, copier l'étiquette complète d'une ligne qui a déjà le bon statut (de `<span class="pill …">` jusqu'au `</span></span>` final). La phrase « 3 articles sur 12 trouvés » et la barre de progression se recalculent toutes seules.

### Ajouter une page au carnet d'Antho

1. Téléverser le dessin en PNG à fond transparent (trait noir), par exemple `carnet-windy.png`, environ 795 × 1120 px.
2. Dans `index.html`, chercher `data-sketch` et ajouter une ligne sur le même modèle, dans l'ordre des pages :

```html
<canvas data-sketch="carnet-windy.png" width="795" height="1120" role="img" aria-label="Croquis d'Antho : …" data-en="Sketch by Antho: …"></canvas>
```

Les flèches et le compteur de pages apparaissent d'eux-mêmes dès qu'il y a plus de deux dessins. Penser à ajuster la phrase d'introduction du carnet, qui nomme les dessins présents.

### Envoyer un lien directement en anglais

Le site s'ouvre en français, ou en anglais si le navigateur du visiteur est en anglais. Pour forcer une langue dans un lien :

- https://expe-auyuittuq.ca/?lang=en
- https://expe-auyuittuq.ca/?lang=fr

## Hébergement

- **GitHub :** stocke les fichiers et garde l'historique de toutes les modifications.
- **GitHub Pages :** met le site en ligne à chaque modification de la branche `main` (réglage dans Settings → Pages).
- **Domaine :** `expe-auyuittuq.ca`, enregistré chez Spaceship. Les DNS pointent vers GitHub Pages, et le fichier `CNAME` du dépôt fait le lien.

## Crédits

- Photos : Antho, Doriane et l'équipe
- Dessins du carnet : Antho, col Akshayuk
- Écriture des étiquettes : Doriane
