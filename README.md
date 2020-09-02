# WP CLI Useful Commands

## Guides


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
php wp-cli.phar post delete $(wp post list --post_status=trash --post_type='product' --format=ids)
```

