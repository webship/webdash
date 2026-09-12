# Web Dashboard recipe

The default dashboards of the Webship site templates, built on the
[Dashboard](https://www.drupal.org/project/dashboard) module of Drupal CMS:

- **Webmaster**: site content, recent content, site status and who is online. The default dashboard of site
  administrators.
- **Editorial**: own drafts, recently edited content and own content. The default dashboard of content editors.

A user opens the dashboard with the lowest weight they can view at `/admin/dashboard`, and lands there after
logging in. Webmaster has weight -20 and Editorial -10, so they come before other dashboards, like the Welcome
dashboard of the Drupal CMS admin UI, which stay available as tabs.

Maintained by [Webship](https://www.drupal.org/project/webship). Used by the
[Website Starter](https://www.drupal.org/project/website_starter),
[Webship Starter](https://www.drupal.org/project/webship_starter) and
[Webship Portal](https://www.drupal.org/project/webship_portal) site templates.

## Install

Site templates include it in their `recipe.yml`:

```yaml
recipes:
  - webdash
```

On an installed site:

```shell
ddev composer require drupal/webdash
ddev drush recipe ../recipes/webdash
```

## Change the dashboards

Edit the dashboards at `/admin/structure/dashboard`, and who can view them at
`/admin/structure/dashboard/{dashboard}/permissions`. To make another dashboard the default, give it a lower
weight.
