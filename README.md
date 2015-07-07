# .htaccess

#### Enabling `mod_rewrite`
```
<IfModule mod_rewrite.c>
    RewriteEngine On
</IfModule>
```
#### Redirect domain.com to www.domain.com
```
RewriteCond %{HTTP_HOST} !^www\.
RewriteRule ^(.*)$ http://www.%{HTTP_HOST}/$1 [R=301,L]
```
