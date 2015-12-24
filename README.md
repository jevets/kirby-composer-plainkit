# [Kirby's][getkirby] Plain Kit with Composer

A port of [Kirby][getkirby]'s [Plain Kit][plainkit] to work with [Composer][composer].

## Why?

Composer is the excellent package/dependency manager for PHP.

This project helps you quickly spin up a Kirby site, installing [kirby][kirby], [toolkit][toolkit], and the [panel][panel] with composer.

## Directory Structure

This project uses a [customized folder setup](http://getkirby.com/docs/advanced/customized-folder-setup).

```bash
project/
    .gitignore
    composer.json
    package.json
    public/
        .htaccess
        index.php
        site.php
        content/
        assets/
            avatars/
        thumbs/
        # Composer installs these:
        kirby/
            toolkit/
        panel/
    site/
        accounts/
        blueprints/
        cache/
        config/
        controllers/
        models/
        snippets/
        templates/
```

Feel free to change the directory structure, but make sure to:

- adjust your `installer-paths` in `composer.json`
- adjust your paths in `.gitignore`
- adjust your path to `site/` in `public/site.php`
- adjust your path in the `serve` script in `package.json`

## Installation

Make sure you have [composer][composer] installed.

```bash
git clone https://github.com/jevets/kirby-composer-plainkit my-site
cd my-site
composer install
```

## Local Webserver

Install Node.js and `npm`.

I've included a simple server script in `package.json`.

`npm run serve`

If you've changed the directory structure, make sure to update the `serve` script in `package.json`.

```json
"scripts": {
    "serve": "php -S localhost:9000 -t path/to/my/document/root/"
}
```

## 

[plainkit]: https://github.com/getkirby/plainkit
[kirby]: https://github.com/getkirby/kirby
[toolkit]: https://github.com/getkirby/toolkit
[panel]: https://github.com/getkirby/panel
[getkirby]: http://getkirby.com
[composer]: http://getcomposer.org