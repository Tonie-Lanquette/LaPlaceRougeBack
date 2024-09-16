# Application La Place Rouge BACKEND

## Installation

1. `git clone https://github.com/Tonie-Lanquette/LaPlaceRougeBack/`

2. `cd LaPlaceRougeBack`

3. `composer install`
   
5. Modifier dans le fichier .env les informations pour migrer la BDD.

6. `doctrine:migration:migrate`

7. `symfony server:start`

## Mise en ligne

### Sur le serveur Simplon

1. Créer un dossier PROD

3. Modifier le fichier nelmio_cors.yaml et y mettre l'url du site front dans les CORS.

4. Modifier le fichier.env et y mettre les informations de BDD selon l'apprenant.

5. `composer dump-env prod qui créer le dossier .env.local.php`

6. mettre dans le dossier PROD ces fichiers/dossiers :
* assets
* bin
* config
* migrations
* public
* src
* templates
* .env.local.php
* composer.json
* composer.lock
* importmap.php
* symfony.lock

6. `composer install --no-dev --optimize-autoloader`

7. `symfony console cache:clear
symfony console cache:warmup --env=prod`

8. Créer le fichier nginx.conf qui fait office de .htaccess pour le serveur et modifier les informations selon l'apprenant.

9. Installer l'application FileZilla pour televerser les fichiers sur le serveur.

10. Se connecter sur le serveur simplon via FileZilla en utilisant ses identifiants.

11. Déployer l'application sur FileZilla dans le fichier "www".


