# Islandora Workbench Integration

## Introduction

Drupal 8 Module required by [Islandora Workbench](https://github.com/mjordan/islandora_workbench). Enables the following Views:

* Terms in vocabulary
* Term from URI

Also enables the following REST resources:

* Field
* Field Storage
* Entity Form Display
* User
* URL alias

## Usage

There is no user interface to this module. It only installs configuration that is required by Islandora Workbench.

## Requirements

* [Islandora 8](https://github.com/Islandora-CLAW/islandora)

## Installation

1. Clone this Github repo into your Islandora's `drupal/web/modules/contrib` directory.
1. Enable the module either under the "Admin > Extend" menu or by running `drush en -y islandora_workbench_integration`.

## Configuration

By default, all vocabularies are registered in the views. To prevent vocabularies from being updated by Workbench, remove them from the "Termis in vocabulary" View using its "Taxonomy term: Vocabulary" filter.

## Permissions

By default, only users with the "Administer vocabularies and terms" permission can access the "Terms in vocabulary" and "Term from URI" Views. You should not relax the permission on this View since they return large amounts of data, which can have an impact on your site's performance if the View is queried by anonymous users.

## Current maintainer

* [Mark Jordan](https://github.com/mjordan)

## License

[GPLv2](http://www.gnu.org/licenses/gpl-2.0.txt)
