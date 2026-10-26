# Mettre le site en ligne sur lagauchere.ca (GitHub Pages, gratuit)

Le site est un simple dossier de fichiers, **tous au même niveau, sans sous-dossier** (`index.html`, `CNAME`, les photos `.jpg`/`.webp` et les vidéos `.mp4`).
GitHub Pages l’héberge gratuitement et l’affiche sous **votre** nom de domaine, sans « github.io » dans l’adresse.

> **Votre domaine :** `lagauchere.ca` (sans accent), acheté chez Namecheap. C’est ce nom qui est dans le fichier `CNAME`.
> Si vous téléversez à nouveau tout le site, gardez ce fichier `CNAME` tel quel, sinon le domaine se débranche.

## Étape 1 — Créer un compte et un dépôt GitHub
1. Créez un compte gratuit sur https://github.com.
2. Cliquez **New repository** → nom : `lagauchere-site` → **Public** → **Create repository**.
3. Cliquez **uploading an existing file**, glissez-y **tous les fichiers** du dossier → **Commit changes**.

## Étape 2 — Activer GitHub Pages
1. Dans le dépôt : **Settings** → **Pages**.
2. **Source** : *Deploy from a branch* → branche `main`, dossier `/ (root)` → **Save**.
3. Dans **Custom domain**, écrivez `lagauchere.ca` → **Save**.

## Étape 3 — Configurer le domaine chez votre registraire
(là où vous avez acheté le domaine : GoDaddy, Namecheap, Webnames, etc.)
Dans la zone **DNS** de `lagauchere.ca`, ajoutez :

| Type  | Nom / Hôte | Valeur                    |
|-------|------------|---------------------------|
| A     | @          | 185.199.108.153           |
| A     | @          | 185.199.109.153           |
| A     | @          | 185.199.110.153           |
| A     | @          | 185.199.111.153           |
| CNAME | www        | VOTRE-NOM-GITHUB.github.io |

Supprimez les anciens enregistrements A ou CNAME « @ » / « www » (page de parking du registraire).

## Étape 4 — Activer le cadenas (HTTPS)
Après 15 min à 24 h, retournez dans **Settings → Pages** et cochez **Enforce HTTPS**.
Le site est alors accessible sur **https://lagauchere.ca**.

## Vos photos et vidéos
Tous les fichiers sont à côté de `index.html`, sans dossier :
- accueil : `hero.jpg` — menu : `boeuf-soya.jpg`, `poulet.jpg`, `crevettes.jpg` — boisson : `jus-baobab.jpg`
- traiteur : `evenement.mp4` (+ `evenement-poster.jpg`), `buffet-1.mp4` à `buffet-3.mp4` (+ `buffet-1.jpg` à `buffet-3.jpg`)
- galerie : `galerie-1.jpg` à `galerie-3.jpg`, `boissons.jpg`
- logo : `logo-rond.webp`, `logo-complet.webp`, `favicon.png`, `apple-touch-icon.png`

## Modifier le site vous-même (sans rien installer)
Tout se fait sur github.com, depuis un ordinateur ou un téléphone. Chaque modification
apparaît sur lagauchere.ca environ 1 minute après.

### Changer un prix, un texte ou un numéro
1. Ouvrez votre dépôt `lagauchere-site` sur github.com et cliquez sur `index.html`.
2. Cliquez sur l’icône **crayon** (Edit this file) en haut à droite.
3. Faites **Ctrl+F** (ou Cmd+F sur Mac) et cherchez le symbole **✏️** : il marque les endroits à modifier
   (prix des gaufres, formules La Complice et La Royale, prix du jus de bouye, coordonnées, vidéo).
4. Changez seulement le texte visible. Exemple : `18&nbsp;$` devient `19&nbsp;$`
   (gardez `&nbsp;`, c’est l’espace avant le signe $).
5. Cliquez **Commit changes…** puis encore **Commit changes**. C’est enregistré.

> Si vous faites une erreur : dans le dépôt, cliquez sur **History** (historique), ouvrez la version
> précédente et restaurez-la, ou demandez-moi de corriger.

### Remplacer une photo
1. Ouvrez votre dépôt sur github.com.
2. **Add file → Upload files**, glissez la nouvelle photo **avec exactement le même nom**
   (par exemple `poulet.jpg`). Elle remplace l’ancienne.
3. **Commit changes**.

Astuce : envoyez-moi vos nouvelles photos d’abord, je les retouche et les recadre au bon format.

### Ajouter la vidéo de l’événement (section Traiteur)
1. Envoyez-moi d’abord la vidéo : je la compresse pour qu’elle charge vite sur téléphone
   (GitHub refuse les fichiers de plus de 25 Mo envoyés depuis le site web).
2. Dans le dépôt : **Add file → Upload files** → déposez le fichier nommé exactement
   `evenement.mp4` → **Commit changes**. Il remplace l’ancienne vidéo.
Tant qu’il n’y a pas de vidéo, une photo s’affiche à sa place.

### Pour un changement plus important
(nouvelle section, nouveau produit, nouvelle page) : demandez-le-moi en décrivant ce que vous voulez,
je vous renvoie le fichier `index.html` mis à jour à téléverser.
