# APE Les Écureuils — version de présentation

Site statique français, responsive, sans dépendance ni compilation. Aucun nom de domaine nécessaire pour la prévisualisation GitHub Pages.

## Prévisualiser

Exécuter `python3 -m http.server 8000` dans ce dossier, puis ouvrir http://localhost:8000. Ouvrir directement index.html permet aussi de voir le site, mais le chargement JSON nécessite un serveur HTTP.

## Déployer sur GitHub Pages

Déposer tous les fichiers de ce dossier à la racine du dépôt, y compris `.nojekyll`. Dans Settings → Pages, sélectionner « Deploy from a branch », `main`, `/ (root)`, puis enregistrer. Vérifier le workflow Pages et le lien affiché par GitHub. Aucun CNAME n’est fourni : le domaine sera choisi après validation.

## Modifier les actualités

Le site lit `actualites.json`. Structure :

```json
{"items":[{"title":"Titre validé", "date":"2026-10-01", "body":"Texte approuvé", "published":true}]}
```

Les textes sont rendus comme du texte, jamais comme du HTML. Une entrée publiée apparaît sur la page. `published:false` masque l’entrée du site mais ne protège pas son contenu : le JSON et un dépôt public restent accessibles. Ne jamais y mettre de données confidentielles. La carte d’adhésion se modifie dans `index.html` à chaque rentrée. La configuration `.pages.yml` peut permettre une édition avec Pages CMS après installation et autorisation par le propriétaire ; aucune application CMS n’a été installée dans cette livraison.

## Avant validation du dirigeant

- Confirmer les textes, le prix et le lien d’adhésion.
- Fournir le logo original et approuver l’illustration proposée.
- Confirmer le bureau, l’adresse e-mail à publier et l’URL Facebook exacte.
- Fournir les événements, bilans et documents autorisés à la publication.
- Compléter et valider les mentions légales avec les données exactes du responsable et de l’hébergement.
- Choisir le domaine après validation ; configurer le domaine et HTTPS ensuite.
- Retirer `noindex,nofollow` des deux fichiers HTML et remplacer `Disallow: /` dans robots.txt uniquement au lancement officiel.

La préversion n’est pas privée : noindex est une consigne aux moteurs de recherche, pas un contrôle d’accès. Aucun formulaire non fonctionnel, faux événement, faux résultat chiffré, compte Google ou service de messagerie n’a été ajouté.

## Sources vérifiées le 29 septembre 2026

- Brief : https://chatgpt.com/share/6abb5768-c524-83eb-b15e-28a43a1a388e
- Association, missions et adresse : https://www.helloasso.com/associations/ape-les-ecureuils-a-hargarten
- Adhésion 5 €, période 01/09/2026–31/08/2027 : https://www.helloasso.com/associations/ape-les-ecureuils-a-hargarten/adhesions/adhesion-annuelle-2

L’illustration SVG est originale et décorative, non une représentation des locaux de l’école. Le logo public a été récupéré sur HelloAsso et intégré à la page (version 140 px). Demander l’original haute résolution au bureau. Les images sont intégrées au HTML pour faciliter le déploiement ; les sources sont conservées dans assets/.
