# WP CLI Useful Commands

## Guides

Install: https://github.com/wp-cli/wp-cli#installing
Commands: https://github.com/wp-cli/entity-command  

## Wordpress

### Install plugin

```
php wp-cli.phar plugin install akismet --activate
```

### List plugin

```
php wp-cli.phar plugin list
```

### Install theme

```
php wp-cli.phar theme install twentytwenty --activate
```

### List theme

```
php wp-cli.phar theme list
```

### Optimizing Site Images

```
wp image-optimize mu-plugins
wp image-optimize plugins
wp image-optimize themes
wp image-optimize wp-admin
wp image-optimize wp-includes
```

```
wp media regenerate --yes
```

```
wp image-optimize batch --limit=500
wp image-optimize batch --limit=1000
wp image-optimize batch --limit=2500
wp image-optimize batch --limit=5000
```
```
wp image-optimize attachment 123
wp image-optimize restore 123
wp media regenerate 123
```

https://www.liquidweb.com/kb/image-optimizer-package-wp-cli/  

## Woocommerce

### Update Database

```
php wp-cli.phar wc update
```

### Delete Trashed Products

```
php wp-cli.phar post delete --force $(php wp-cli.phar post list --post_status=trash --post_type='product' --posts_per_page=1000 --format=ids)
```

