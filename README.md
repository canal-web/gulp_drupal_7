# Gulp Drupal 7

Automatise les tâches pour le développement front-end sur drupal 7. Permet de compiler, nettoyer, préfixer et minifier les feuilles de style et les fichiers javascript. Optimise les images. Recharge le navigateur automatiquement après une modification.

## Installation

- Requis : node.js / NPM
- Requis : Gulp  `npm install gulp -g`
- Copier les fichiers __defautl.config.json__, __gulpfile.js__ et __package.json__ dans le thème de drupal (`sites/all/themes/mon_theme`)
- Renommer __default.config.json__ en __config.json__
- Lancer l'installation des packages avec `npm install`

## Utilisation

### Toutes les tâches

La commande `gulp` lance toutes les tâches CSS, JS et images. La commande `gulp watch` surveille les dossiers concernés et lance les tâches à chaque modification.

### Lancer une tâche

Pour compiler les fichiers SCSS :

`gulp sass`

Pour compiler les fichiers JS :
`gulp js`

Pour optimiser les images :
`gulp img`

### Passage en production

Pour exécuter les tâches spécifiques à la mise en production :
`gulp --env prod`

### Recharger le navigateur automatiquement

Il faut installer le module [BrowserSync](https://www.drupal.org/project/browsersync) pour Drupal au préalable et l'activer dans *apparence/paramètres*. Puis dans le fichier __config.json__, ajouter l'url du site en face de la ligne `"proxy" :`. Enfin, relancer un `gulp watch`.
