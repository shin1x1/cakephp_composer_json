cakephp_composer_json
=======================

1. Install CakePHP using Composer
-----------------------------------

<pre>
$ git clone https://github.com/shin1x1/cakephp_composer_json.git
$ cd cakephp_composer_json
$ curl -sS https://getcomposer.org/installer | php
$ ./composer.phar install
</pre>

2. Setup CakePHP app
-----------------------------------

<pre>
$ cp -a vendor/cakephp/cakephp/app .
</pre>

or
<pre>
$ ./vendor/cakephp/cakephp/lib/Cake/Console/cake bake project
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

3. Hello Cake!
-----------------------------------

<pre>
$ ./app/Console/cake server -p 10000
</pre>

4. Update CakePHP core
-----------------------------------

<pre>
$ ./composer.phar update
</pre>
