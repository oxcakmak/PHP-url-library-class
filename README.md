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
