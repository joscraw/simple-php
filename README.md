# simple-php
Simple-php is a repository that contains custom PHP builds with extensions that don't come installed by default. 


Installing PHP is easy. Depending on your distro, normally you would do: $ sudo apt-get install php or $ sudo yum install php. This is usually sufficient in most circumstances, but what if you need Pthreads, Xdebug, or any other extension that does not come installed by default? Well now things become quite difficult. Most people are left scratching their heads with the same questions. Should I use PEAR, PECL, phpize? After an hour or 2 spent on google, you realize that either 

1. PECL or PEAR needs to be updated on your system
2. Try using composer to install the extension. (You're like WHAT???)
3. Git clone the repository and then hopefully you know a little bit of C because now you need to run make, make test, make install, and more often then not, prior to that, you will need to configure the library with various options and flags to create a makefile and blah blah blah. 

Simple-php is an initiative to make your life easier. We custom compile PHP from source using extensions that normally don't come installed by default. All you have to do is search through are REPO and find the PHP version that you need with the extensions you need.


Currently we are only creating builds for the following distributions:

Debian based systems, including Ubuntu (APT package manager)
Fedora 21 and below, and CentOS. (YUM package manager)
