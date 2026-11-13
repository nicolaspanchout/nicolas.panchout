# Ajouter un projet au portfolio

Tu n'as jamais besoin de toucher à `index.html`. Tout se passe dans deux endroits :

- le dossier `projets/`, qui contient tes images et tes vidéos ;
- le fichier `projets.json`, qui contient la liste des projets et leurs textes.

## Organisation du dépôt

```
index.html            ← le site (ne pas modifier)
chambre.jpg           ← le rendu de la chambre
projets.json          ← la liste de tes projets
projets/
  3d/                 ← rendus Blender         → onglet 3D (poster 3D)
  photos/             ← shootings              → onglet Photo (appareil photo)
  videos/             ← reels (.mp4)           → onglet Vidéo (caméra)
  ux-ui-design/       ← maquettes d'applis/sites → onglet UX/UI (poster UX/UI)
  logos/              ← logos, identités       → onglet Identité (écran)
```

## Étape 1 : prépare tes fichiers

- **Images** : en JPG, 2000 px de large maximum, moins de 1 Mo si possible.
- **Vidéos** : en MP4, moins de 25 Mo, car GitHub refuse au-delà par le site web.
- **Noms de fichiers** : en minuscules, sans espaces ni accents, par exemple `ville-neon-01.jpg`.

## Étape 2 : envoie les fichiers sur GitHub

1. Ouvre ton dépôt, puis le dossier `projets`, puis le dossier de la catégorie (par exemple `3d`).
2. Clique sur **Add file**, puis **Upload files**, et glisse tes images.
3. Clique sur **Commit changes**.

Chaque dossier contient un petit fichier `_mets-tes-fichiers-ici.txt` : il sert juste à ce que GitHub garde le dossier même vide. Tu peux le laisser.

## Étape 3 : ajoute le projet dans `projets.json`

1. Ouvre `projets.json` sur GitHub et clique sur le crayon ✏️ (**Edit**).
2. Va dans la bonne catégorie : `"3d"`, `"photos"`, `"videos"`, `"ux-ui-design"` ou `"logos"` (les mêmes noms que les dossiers).
3. Copie un projet existant, colle-le et remplace les textes. Exemple :

```json
{
  "titre": "Ville néon",
  "tags": ["Blender", "Cycles", "2026"],
  "format": "paysage",
  "images": [
    "projets/3d/ville-neon-01.jpg",
    "projets/3d/ville-neon-02.jpg"
  ],
  "texte": "Une rue cyberpunk sous la pluie : modélisation, néons et brouillard volumétrique."
},
```

4. Clique sur **Commit changes**. Le site se met à jour en une minute environ.

## Les champs possibles

| Champ | Obligatoire | Ce que ça fait |
|---|---|---|
| `titre` | oui | Le nom du projet |
| `texte` | oui | La description |
| `tags` | non | Les petites étiquettes : `["Logo", "2026"]` |
| `format` | non | `"paysage"` (4:3) ou `"portrait"` (9:16, pour les reels) |
| `images` | non | Liste des images. La première sert de vignette, les autres se voient en cliquant dessus |
| `video` | non | Un MP4 : `"projets/videos/zeppelin.mp4"` |
| `lien` | non | Un lien externe, par exemple le reel sur Instagram |
| `texte_lien` | non | Le texte du bouton de lien : `"Voir le reel"` |
| `statut` | non | Une pastille orange, par exemple `"En cours"` |
| `stats` | non | Des chiffres : `[{"chiffre": "12k", "label": "Vues"}]` |

Un projet sans image affiche « Visuel à intégrer ».

## Les 3 erreurs classiques

1. **Une virgule** : il faut une virgule `,` entre deux projets `{ … }`, mais pas après le dernier.
2. **Les guillemets** : utilise toujours des guillemets droits `"`, jamais `«` ni `“`. Pour des guillemets dans un texte, mets `«  »`, qui ne posent pas de problème.
3. **Le chemin de l'image** : il doit être exactement le même que sur GitHub, majuscules comprises.

Si le site n'affiche plus tes projets après une modification, colle le contenu de `projets.json` sur **jsonlint.com** : le site t'indique la ligne de l'erreur.

## Changer le mail ou l'Insta

C'est en haut de `projets.json`, dans `"contact"`.
