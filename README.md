# Web Dashboard recipe

The default dashboards of the Webship site templates, built with
[Display Builder](https://www.drupal.org/project/display_builder) on the
[Web Dashboard](https://www.drupal.org/project/webdashboard) module. No Layout Builder.

- **Webmaster**: site status, who is online, a content chart and recent content. The default dashboard of site
  administrators.
- **Editorial**: add content links, recent content, own drafts and own content. The default dashboard of
  content editors.

The **Dashboards** toolbar tab opens the dashboard with the lowest weight the user can view. Webmaster has weight
-20 and Editorial -10, so they come before other dashboards, which stay listed in the tab.

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

Build the dashboards at `/admin/structure/webdashboards`, with the **Default Dashboard** tab of each dashboard,
and set who can view them on its **Permissions** tab. To make another dashboard the default, give it a lower
weight.
