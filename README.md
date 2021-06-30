# PHP-url-library-class
PHP url library class (php url parse)<br>
include("url.php");<br>
$url = new url;<br>
$link = $url->getSegments();<br>
$username = @$link[0];

if($username){

  include("profile.php");
  
}

profile.php:
$username //pulls username from url

Scheme:
index.php -> (VARIABLES) -> profile.php

Htaccess:<br>
Options -Indexes +FollowSymLinks<br>
RewriteEngine on<br>
RewriteRule ^ajax$ ajax.php [L, NC, QSA]<br>
RewriteCond %{REQUEST_FILENAME} !-d<br>
RewriteCond %{REQUEST_FILENAME} !-f<br>
RewriteRule ^(.+)$ index.php?page=$1 [QSA,L]
