# MEKA PRINT — site internet

Site vitrine one-page pour MEKA PRINT (Léo, jeune maker à Saint-Malo) :
impression 3D, prises de vues par drone, réparation d'objets et hivernage
de moulinet.

Tout est contenu dans **un seul fichier** : [`index.html`](./index.html).
Pas de build, pas de dépendances à installer : ouvrez le fichier dans un
navigateur, ou mettez-le en ligne tel quel.

## Ce que contient le site

- Une page d'accueil avec une pièce 3D animée en CSS/SVG.
- Une section **Prestations** avec les 4 services, leurs tarifs de départ
  et une illustration dessinée pour chacun (impression 3D, drone,
  réparation, moulinet), pas de photo à fournir.
- Un **atelier 3D interactif** (impression 3D en direct avec Three.js) :
  on règle les cotes d'une pièce, on choisit une couleur de filament, on
  lance l'impression et on voit le volume/la masse se calculer.
- Une section **À propos** avec le texte de présentation de Léo.
- Une section **Comment ça marche** (méthode en 4 étapes, cliquable).
- Un **formulaire de contact** qui prépare un message prêt à copier ou à
  envoyer par email (mailto), plus les liens Instagram/Facebook/YouTube.
- Un pied de page avec une silhouette animée des remparts de Saint-Malo.

Le site s'adapte au mobile, respecte le mode sombre du système et coupe
les animations si l'utilisateur a demandé « réduire les animations »
dans son système.

## Mettre à jour les coordonnées

Les coordonnées sont regroupées tout en haut du bloc `<script>`, à la fin
du fichier :

```js
var CONTACT = {
  email: "mekaprint.bzh@gmail.com",
  instagram: "https://www.instagram.com/mekaprint.bzh",
  facebook: "https://www.facebook.com/mekaprint",
  youtube: "https://www.youtube.com/@mekaprint"
};
```

Modifiez ces valeurs directement dans `index.html` pour changer l'email
ou les liens des réseaux sociaux.

## Publier le site avec GitHub Pages (gratuit)

1. Créez un dépôt sur GitHub, par exemple `meka-print`.
2. Ajoutez ce dossier au dépôt (voir la section suivante pour les
   commandes) et poussez-le sur GitHub.
3. Dans le dépôt GitHub : **Settings → Pages**.
4. Sous *Build and deployment*, choisissez **Deploy from a branch**,
   branche `main`, dossier `/ (root)`, puis **Save**.
5. Après une minute ou deux, le site est en ligne à l'adresse
   `https://<votre-nom-utilisateur>.github.io/meka-print/`.

Pour un nom de domaine personnalisé (par ex. `mekaprint.fr`), ajoutez-le
dans la même page Settings → Pages, puis configurez chez votre
registrar un enregistrement CNAME pointant vers
`<votre-nom-utilisateur>.github.io`.

## Commandes Git pour publier ce dossier

Depuis ce dossier (celui qui contient `index.html`) :

```bash
git init
git add .
git commit -m "Site MEKA PRINT"
git branch -M main
git remote add origin https://github.com/<votre-nom-utilisateur>/meka-print.git
git push -u origin main
```

Remplacez `<votre-nom-utilisateur>` par votre nom d'utilisateur GitHub.
Si le dépôt distant existe déjà avec des fichiers (par ex. un README créé
depuis l'interface GitHub), faites `git pull origin main --allow-unrelated-histories`
avant le `push`.

## Modifier le site ensuite

Le fichier est un simple HTML avec CSS et JavaScript intégrés, sans
build : ouvrez `index.html` dans n'importe quel éditeur de texte, modifiez,
enregistrez, et raffraîchissez la page dans le navigateur pour voir le
résultat.
