# Autoload

Cette classe une fois rajoutée dans votre projet php s'occupera d'inclure les fichiers dont vous avez besoin.

Vous n'aurez plus besoin de rajouter les includes au début de chaque fichier, mais il est recommandé d'utiliser des namespace pour éviter les collisions de nom de classe (surtout si vous utilisez des librairies).

## Utilisation
Dans votre `index.php`
```php
require_once 'autoloader.php'; // Il faut inclure le fichier de la classe
Autoloader::setPathTop(__DIR__); // Définit le haut de votre arborescence là ou est situé le index.php
spl_autoload_register('Autoloader::load'); // Enregistre la méthode load de la classe pour inclure les fichiers automatiquement
```
