1. Upload the .rpm package inside this folder to a location on your server. i.e. /tmp
2. Run $ sudo rpm -i *.rpm where *.rpm is the full name of the package.
3. You might be notified that you are missing dependencies. A list of dependencies needed for this package will be 
presented to you. Use $ sudo yum install to install each missing dependency. 
4. You are all set up and good to go! Your php files will be located at /usr/local/php7.2.0
5. You can see your php version: $ /usr/local/php7.2.0/bin/php -v


If you want your PHP executables to be globally available (php, pear, pecl, phpize, php-config, etc).
1. $ sudo -s 
2. $ echo "export PATH=/usr/local/php7.2.0/bin:${PATH}" >> ~/.bash_profile
3. $ source ~/.bash_profile
4. You can now see your php version like so: $ php -v

If configuring for Apache CGI:
1. $ sudo -s
2. $ echo -e "<FilesMatch \\.php$>\nSetHandler application/x-httpd-php\n</FilesMatch>" > /etc/httpd/conf.d/php.conf
3. $ echo "PHPIniDir \"/usr/local/php7.2.0/lib/apache\"" >> /etc/httpd/conf/httpd.conf



------------------------------------------------------------------------------------------------------------------------------
The following extensions are enabled with this php build
------------------------------------------------------------------------------------------------------------------------------

PHP CLI enabled modules:

bcmath Core ctype curl date dom fileinfo filter hash iconv json libxml mbstring mysqli mysqlnd openssl pcre PDO pdo_mysql pdo_sqlite Phar posix pthreads Reflection session SimpleXML soap SPL sqlite3 standard tokenizer xdebug xml xmlreader xmlwriter zip zlib Xdebug

PHP CGI enabled modules (Usually for Apache, Nginx, etc):

Core date libxml openssl pcre sqlite3 zlib bcmath ctype curl dom fileinfo filter hash iconv json mbstring SPL session standard PDO mysqlnd pdo_sqlite Phar posix Reflection pdo_mysql SimpleXML soap mysqli tokenizer xml xmlreader xmlwriter zip apache2handler xdebug
