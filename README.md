# Drupal project builder

## Apache VHOST
```sh
    <VirtualHost *:80>
        ServerName drupal-build.dev
        ServerAlias *.itelis-hospiway-d7.dev
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/drupal-build/src
    
        DirectoryIndex index.html index.php
    
        <Directory /var/www/drupal-build/src>
          Options FollowSymlinks
          AllowOverride All
        </Directory>
    
        # Database configuration
        SetEnv SAMPLE_SITE_URI "SAMPLE_SITE_URI"
        SetEnv SAMPLE_DATABASE_NAME "SAMPLE_DATABASE_NAME"
        SetEnv SAMPLE_DATABASE_LOGIN "SAMPLE_DATABASE_LOGIN"
        SetEnv SAMPLE_DATABASE_PASS "SAMPLE_DATABASE_PASS"
        SetEnv SAMPLE_DATABASE_HOST "SAMPLE_DATABASE_HOST"
        SetEnv SAMPLE_DATABASE_PORT ""
        ...
        ...
    </VirtualHost>
```