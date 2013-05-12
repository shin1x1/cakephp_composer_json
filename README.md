cakephp_composer_js
===================

1. Install CakePHP using Composer
-----------------------------------

<pre>
$ git clone git@github.com:shin1x1/cakephp_composer_js.git
$ curl -sS https://getcomposer.org/installer | php
$ ./composer.phar install
</pre>

2. Setup CakePHP app
-----------------------------------

<pre>
$ cp -a vendor/cakephp/cakephp/app .
</pre>

Edit include_path

<pre>
$ vim app/webroot/index.php
define('CAKE_CORE_INCLUDE_PATH', ROOT.DS.'vendor'.DS.'cakephp'.DS.'cakephp'.DS.'lib');

$ vim app/webroot/test.php
define('CAKE_CORE_INCLUDE_PATH', ROOT.DS.'vendor'.DS.'cakephp'.DS.'cakephp'.DS.'lib');

$ vim app/Console/cake.php
ini_set('include_path', $root.$ds.'vendor'.$ds.'cakephp'.$ds.'cakephp'.$ds.'lib'.PATH_SEPARATOR . ini_get('include_path'));
</pre>

3. Update CakePHP
-----------------------------------

<pre>
$ php composer.phar update
</pre>
