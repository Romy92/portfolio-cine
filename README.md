# Portfolio & Critiques ciné

## Publier gratuitement sur Cloudflare Pages

1. Créez un compte sur [GitHub](https://github.com) puis un nouveau dépôt, par exemple `portfolio-cine`.
2. Ajoutez tous les fichiers de ce dossier au dépôt, y compris le dossier `assets`.
3. Créez un compte sur [Cloudflare](https://dash.cloudflare.com/sign-up).
4. Dans **Workers & Pages**, choisissez **Create application** puis **Pages** et **Import an existing Git repository**.
5. Connectez GitHub, choisissez le dépôt `portfolio-cine`, puis configurez :
   - Production branch : `main`
   - Build command : `exit 0`
   - Build output directory : `.`
6. Cliquez sur **Save and Deploy**. Cloudflare affiche alors votre lien public en `*.pages.dev`.

## Choisir une adresse personnalisée

Vous pouvez utiliser l’adresse gratuite Cloudflare ou acheter un domaine auprès du registraire de votre choix, par exemple `monportfolio-cine.fr`. Dans Cloudflare Pages : ouvrez votre projet, allez dans **Custom domains**, puis **Set up a domain** et suivez les instructions DNS affichées.

## Modifier le contenu

Pour cette première version, ouvrez `index.html` dans GitHub puis cliquez sur l’icône crayon :

- `OBSESSION` : titre du film ;
- `★★★★☆` : note (une étoile pleine = `★`, une étoile vide = `☆`) ;
- `Portfolio · 2026` : catégorie et année ;
- `ceci est une critique de film` : texte de critique ;
- `assets/obsession.jpg` : affiche actuelle. Pour remplacer l’image, importez votre photo dans `assets`, puis remplacez `obsession.jpg` dans `styles.css` par le nouveau nom.

Après chaque modification enregistrée sur GitHub, Cloudflare republie le site automatiquement.

Pour une gestion sans toucher aux fichiers, la prochaine étape est d’ajouter un espace d’administration sécurisé : formulaire d’ajout de films, import d’affiches et choix de la note.

## Administration préparée

L’administration est disponible à l’adresse `/admin/` après déploiement. Elle permet de modifier le titre, la catégorie, l’année, la note par demi-étoile, le texte, la couleur et l’affiche de chaque film.

Avant sa première utilisation, remplacez dans `admin/config.yml` :

- `REMPLACER_PAR_VOTRE_COMPTE/portfolio-cine` par votre compte GitHub et le nom du dépôt ;
- `REMPLACER_PAR_VOTRE_URL_OAUTH` par l’URL du petit service OAuth GitHub qui protège la connexion d’administration.

Cette dernière URL doit être créée avec votre compte GitHub, car elle utilise vos identifiants privés. Je peux vous guider lors de cette étape sans jamais vous demander votre mot de passe ou vos clés privées.
