# Poakpong Starter Pack

This is a personal Starter Pack for initializing new Drupal projects. It helps save time by installing essential modules and applying frequently used configurations.

## What's Included

### Modules

#### Admin & Developer Tools
- admin_toolbar
- admin_toolbar_search
- admin_toolbar_tools
- asset_injector
- coffee
- upgrade_status

#### Content Editing & CKEditor
- ckeditor5_paste_filter
- ckeditor5_plugin_pack
- ckeditor5_plugin_pack_bookmark
- ckeditor5_plugin_pack_find_and_replace
- ckeditor5_plugin_pack_fullscreen
- ckeditor5_plugin_pack_templates
- imce
- maxlength
- node_edit_protection

#### Site Structure & Helpers
- body_node_id_class
- menu_link_attributes
- page_specific_class
- trash

#### User & Access
- admin_login_path
- login_emailusername
- rename_admin_paths

#### SEO & Path
- google_analytics
- metatag
- metatag_open_graph
- metatag_twitter_cards
- pathauto
- redirect
- scheduler
- token

#### Views Tools
- views_bulk_edit
- views_bulk_operations

#### Marketing / API
- mailjet_api

### Default Configuration
- User Registration: Administrators only
- Regional Settings: Timezone set to Asia/Bangkok
- System: File Sanitization enabled
- IMCE: Admin and Content editor profiles

## Installation Guide

### Prerequisites
Before running this recipe, please ensure that:
1. You have a **standard Drupal site installed**.
2. You have placed the `poakpong_starter_pack` folder inside the `recipes` directory of your Drupal project (e.g., at `your-project-root/drupal/recipes/poakpong_starter_pack`).

### Steps

#### 1. Download the Recipe
Go to your Drupal project root and download the recipe into your existing `recipes` folder:

```bash
cd recipes
git clone https://github.com/poakpong/poakpong_starter_pack.git
cd ..
```

(Note: The `cd ..` command returns you to the project root for the next steps.)

#### 2. Add the Recipe to the project

Run the following commands at the project root to register and require the recipe:

```bash
composer config repositories.poakpong_starter_pack path recipes/poakpong_starter_pack
composer require poakpong/poakpong_starter_pack
drush cache:rebuild
```

#### 2. Run the Recipe

Navigate to the web directory to apply the recipe:

```bash
cd web
php core/scripts/drupal recipe ../recipes/poakpong_starter_pack
```

#### 3. Export Config and Clear Cache

Go back to the project root to export the new configurations:

```bash
cd ..
drush config:export -y
drush cache:rebuild
```