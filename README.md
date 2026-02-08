# Varbase Blog Base

A recipe to provide a blog post content type, listing page, and related configuration for Varbase. Use Blog to publish blog posts by different authors in the Blog section of the site.

This recipe builds on top of the Varbase Content Base, Media Base, SEO Base, and Workflow Base recipes, extending them with blog-specific content structure, views, and SEO fields.

## Features

### Blog Content Type
- **Blog** (`blog`): A content type for blog posts with the following fields:
  - Title
  - Description (short summary text)
  - Featured Image (media reference)
  - Content (long text with format)
  - Tags (taxonomy reference with autocomplete via Tagify)
  - Blog Categories (taxonomy reference)

### SEO Fields
- **SEO Title**: Override the default HTML page title for search engines
- **SEO Description**: Description for search engines and social media
- **SEO Image**: Image for social media sharing
- **SEO Analysis**: Yoast SEO real-time content analysis
- SEO fields are grouped in a collapsible "Search Engine Optimization (SEO) Information" fieldset on the edit form

### Taxonomy Vocabularies
- **Tags**: Shared tags vocabulary for blog content
- **Blog Categories**: Blog-specific categorization

### Views
- **Blog** (`blog`): A views listing with multiple displays:
  - **All Blog Posts**: Paginated listing with Better Exposed Filters for tags and categories
  - **Latest Blog Posts**: Block showing the 3 most recent posts
  - **Related Blog Posts**: Block showing related posts based on shared tags
  - **RSS Feed**: Blog content RSS feed

### View Modes
- **Default**: Full blog post display with featured image, content, and tags
- **Card**: Compact card display with featured image and description

### Canvas Content Templates
- **Full**: Canvas template using heading, image, and text components
- **Card**: Canvas template using the card component

### URL Patterns
- **Pathauto**: Automatic URL aliases following the pattern `/blog/[node:created:html_month]/[node:title]`

### Editorial Workflow
- Blog content type is integrated with the Varbase Editorial Workflow for content moderation and scheduled publishing

## Dependencies

This recipe depends on the following Varbase base recipes:
- **varbase_content_base**: Core content structure, field storages, and content management tools
- **varbase_media_base**: Media library, image handling, and media types
- **varbase_seo_base**: Metatag, Pathauto, Yoast SEO, and SEO tools
- **varbase_workflow_base**: Editorial workflow, content moderation, and scheduler

Additional module:
- **selective_better_exposed_filters**: Enhanced exposed filter widgets for views

## Permissions

The recipe configures blog content permissions for:
- **Content Editor**: Create, edit, delete, and manage revisions of blog content

## Installation

Add the recipe using composer:
```
composer require drupal/varbase_blog_base:~1.0.0
```

Change directory to `/web` or `/docroot`

Run the Drupal recipe bash script:
```
bash core/scripts/drupal recipe recipes/varbase_blog_base
```

or

Run the Drush recipe command:
```
drush recipe ../recipes/varbase_blog_base
```

## Maintainers

- [Vardot](https://www.drupal.org/vardot)

## License

GPL-2.0-or-later
