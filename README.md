# Laravel Form Builder

This package provides the standard form builder functionality used in most projects.

## Installation
#### PHP
You can install the package via composer:

```bash
composer require dcodegroup/form-builder
```

Then run the install command.

```bash
php artisan form-builder:install
```

This will publish the configuration file and the migration file.

Run the migrations

```bash
php artisan migrate
```

#### JS

Include vue components to your main vue js file eg: `app.js` with syntax:

```
require('../../public/vendor/form-builder');
```

#### SCSS

There is a new generated file under `sass\form-builder\index.scss`. You must use this file in your main scss file 

Run the npm build (dev/prod)

```bash
npm run dev
```

## Configuration

Most of configuration has been set the fair defaults. However you can review the configuration file at `config/form-builder.php` and adjust as needed

```
return [
    'path'            => env('FORM_BUILDER_PATH', 'forms'),
    'middleware'      => ['web', 'auth'],
    'layout_path'     => 'layouts.admin' // Make sure you have correct base layout name,
    'content_section' => 'content'
]
```

## Usage

The package provides an endpoints which you can use. See the full list by running
```bash
php artisan route:list --name=form
```

They are

[example.com/forms] Which is where you will form index. This is by default protected auth middleware but you can modify in the configuration. This is where you want to link to in your admin and possibly a new window