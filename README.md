# Bootstrap Base

This base theme for Drupal  Bootstrap Sass

This base theme provides the following:
- Template overrides implementing Bootstrap UI components and utilities.
- Libraries to provide standard Bootstrap CSS/JS.
- Separate libraries containing Drupal-specific CSS/JS.
- Bootstrap Sass sub-theme starterkit
- Drush support.

The starterkit provides Bootstrap Sass and an empty `variables.scss` file so you can immediately override the standard `bootstrap.css`. It also provides a basic Gulp setup to watch and build your Sass.

## Getting started

Installation:
```sh
composer require bradtreloar/bootstrap_base
drush en -y bootstrap_base
```

Sub theme using starterkit:
```sh
SUBTHEME="subtheme_name"

# Create sub theme from startkit.
drush --include="themes/contrib/bootstrap_base" bootstrap_base:create $SUBTHEME

# Enable sub theme.
drush en $SUBTHEME -y

# Set sub theme as site default theme.
drush config-set system.theme default $SUBTHEME -y
```

Building Sass in starterkit:
```sh
# Change to sub theme directory.
cd themes/custom/subtheme_name

# Install node module using Yarn
yarn

# Build CSS from Sass.
yarn build

# Watch Sass files and rebuild CSS on change.
yarn watch
```

