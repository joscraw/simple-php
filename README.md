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


------------------------------------------------------------------------------------------------------------------------------
INSTRUCTIONS/DOCUMENTATION
------------------------------------------------------------------------------------------------------------------------------

Inside this repository you will be able to drill down to the custom PHP build that works for you. 
-simple-php
  - CentOs
    - php7.2.0
      - 1
        - .rpm 
        - enabled-extensions.md
        - README.md

1. Find your distribution. (CentOs, Ubuntu, etc)
2. Select the PHP version you need
3. search through the list of builds for the PHP build that works best for you. First build starting with number 1. 
4. Inside each build you will see a file called enabled-extensions.md. This file shows you which modules are enabled for both the PHP CLI and the php CGI. 
5. There is also a README.md file which gives pacakge specific instructions on installing that given package inside the build folder. 






If we are missing a certain PHP build feel free to submit and Issue with the PHP version you are requesting, the extensions you need, and the distro you need it for. We will get to it as soon as possible. 

If you have compiled a PHP package and feel that it should be included in our REPO, feel free to send a pull request and we will review, test, and merge it in!



Happy-Coding! 
