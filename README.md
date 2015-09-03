# BEdita 4 Application Skeleton - Draft

A skeleton for BEdita 4 applications.

## Installation

1. Download [Composer](http://getcomposer.org/doc/00-intro.md) or update `composer self-update`.
2. Run `git clone https://github.com/bedita/bedita4-sandbox && php composer.phar install`.

If Composer is installed globally, run
```bash
git clone https://github.com/bedita/bedita4-sandbox && composer install
```

You should then set up virtual hosts for both `apps/manage/webroot` and `apps/api/webroot`,
then navigate to the URLs `/users/` and `/users.json` respectively for demo usage.

## Configuration

Read and edit `config/app.php` and setup the 'Datasources' and any other
configuration relevant for your application.

## Structure

All BEdita frontends should be placed within the `apps/` folder.

Each app should be configured to use plugins, vendor dependencies, logs, temporary files
and configuration settings from the project folder (see `apps/manage/config/paths.php` and
`apps/manage/config/bootstrap.php` for reference).

All BEdita plugins and modules should be placed within the `plugins/BEdita/` folder.

Each frontend and each plugin can have its own dependencies, which will be installed in the
project's `vendors/` directory using Composer.
