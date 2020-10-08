# Wordpress CLI Useful Commands

## Guides

Install: https://github.com/wp-cli/wp-cli#installing  
Commands: https://github.com/wp-cli/entity-command  
Woocommerce: https://github.com/woocommerce/woocommerce/wiki/WC-CLI-Overview  

## Update WP Cli

```
php wp-cli.phar cli update
```

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

### Yoast Index

```
php wp-cli.phar yoast index
```

### Optimizing Site Images

```
php wp-cli.phar image-optimize mu-plugins
php wp-cli.phar image-optimize plugins
php wp-cli.phar image-optimize themes
php wp-cli.phar image-optimize wp-admin
php wp-cli.phar image-optimize wp-includes
```

```
php wp-cli.phar media regenerate --yes
```

```
php wp-cli.phar image-optimize batch --limit=500
php wp-cli.phar image-optimize batch --limit=1000
php wp-cli.phar image-optimize batch --limit=2500
php wp-cli.phar image-optimize batch --limit=5000
```
```
php wp-cli.phar image-optimize attachment 123
php wp-cli.phar image-optimize restore 123
php wp-cli.phar media regenerate 123
```

https://www.liquidweb.com/kb/image-optimizer-package-wp-cli/  

## Woocommerce

### Update Database

```
php wp-cli.phar wc update
```

### List Products in Status

```
php wp-cli.phar wc product list --status=trash --user=admin_username --per_page=100 --format=ids
```

### List Products in Category

```
php wp-cli.phar wc product list --category=category_id --user=admin_username --per_page=100 --format=ids
```

### List Products in Category in Status

```
php wp-cli.phar wc product list --status=status --category=category_id --user=admin_username --per_page=100 --format=ids
```


### List Orders after Date

```
php wp-cli.phar wc shop_order list --after="2020-10-07T23:59:59" --user=admin_username --per_page=100 --format=ids
```

### List Orders before Date

```
php wp-cli.phar wc shop_order list --before="2020-10-07T23:59:59" --user=admin_username --per_page=100 --format=ids
```

### List Orders between Date

```
php wp-cli.phar wc shop_order list --after="2020-10-01T00:00:00" --before="2020-10-31T23:59:59" --user=admin_username --per_page=100 --format=ids
```

### Export Orders after Date

```
php wp-cli.phar wc shop_order list --after="2020-10-01T00:00:00" --user=username --format=csv > orders_2020_10.csv
```

### Count Products in Category

```
php wp-cli.phar wc product list --category=category_id --user=admin_username --format=count
```

### Delete Products in Category

```
php wp-cli.phar post delete --force $(php wp-cli.phar wc product list --category=category_id --per_page=100 --format=ids)
```

### Delete Products in Status draft

```
php wp-cli.phar post delete --force $(php wp-cli.phar wc product list --status=draft --user=admin_username --per_page=100 --format=ids)
```

### Delete Products in Status trash

```
php wp-cli.phar post delete --force $(php wp-cli.phar wc product list --status=trash --user=admin_username --per_page=100 --format=ids)
```


## Scheduler

https://actionscheduler.org/wp-cli/  

### Scheduler Run

```
php wp-cli.phar action-scheduler run
```

