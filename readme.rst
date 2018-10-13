###################
What is Simple CodeIgniter Multisite (SCM)
###################

SCM is a simple CodeIgniter Multisite.

Demo:

- `Default Site: http://scm.github.mhs.web.id <http://scm.github.mhs.web.id/>`_
- `Sub Site1: http://site1.scm.github.mhs.web.id <http://site1.scm.github.mhs.web.id/>`_
- `Sub Site2: http://site2.scm.github.mhs.web.id <http://site2.scm.github.mhs.web.id/>`_

Demo @ different Domain:

- `Default Site: https://scm.omahijo.net <https://scm.omahijo.net/>`_
- `Client 1 Site: http://client1.scm.omahijo.net <http://client1.scm.omahijo.net/>`_
- `Unkwown Site (no configuration found): http://unknown.scm.omahijo.net <http://unknown.scm.omahijo.net/>`_

Demo With "HTML Template":

- `USHE Main Site: https://ushe.omahijo.net <https://ushe.omahijo.net/>`_
- `CA USHE Sub Site: https://ca.ushe.omahijo.net <https://ca.ushe.omahijo.net/>`_
- `MN USHE Sub Site: https://mn.ushe.omahijo.net <https://mn.ushe.omahijo.net/>`_
- `NY USHE Sub Site: https://ny.ushe.omahijo.net <https://ny.ushe.omahijo.net/>`_


Apache Configuration Sample:

<VirtualHost *:80>

    ServerAdmin webmaster@mhs.web.id

    ServerName scm.github.mhs.web.id

    ServerAlias *.scm.github.mhs.web.id

    DocumentRoot "/var/www/html/scm.github.mhs.web.id/public_html"

    <Directory "/var/www/html/scm.github.mhs.web.id/public_html/">

        Options FollowSymLinks

        AllowOverride All

        Order allow,deny

        Allow from all

    </Directory>

</VirtualHost>


<VirtualHost *:80>

    ServerAdmin webmaster@omahijo.net

    ServerName scm.omahijo.net

    ServerAlias *.scm.omahijo.net

    DocumentRoot "/var/www/html/scm.github.mhs.web.id/public_html"

    <Directory "/var/www/html/scm.github.mhs.web.id/public_html/">

        Options FollowSymLinks

        AllowOverride All

        Order allow,deny

        Allow from all

    </Directory>

</VirtualHost>


********
Install @ PC
********

Add Hostname (/etc/hosts):



127.0.0.1   mhs.tut

127.0.0.1   site1.mhs.tut

127.0.0.1   site2.mhs.tut


127.0.0.1   ci.mhs.tut

127.0.0.1   site1.ci.mhs.tut

127.0.0.1   site2.ci.mhs.tut



Apache Configuration Sample:



<VirtualHost *:80>

    ServerAdmin webmaster@mhs.tut

    ServerName mhs.tut

    ServerAlias *.mhs.tut

    DocumentRoot "/var/www/html/ci_multi_site/public_html"

    <Directory "/var/www/html/ci_multi_site/public_html/">

        Options FollowSymLinks

        AllowOverride All

        Order allow,deny

        Allow from all

    </Directory>

</VirtualHost>



<VirtualHost *:80>

    ServerAdmin webmaster@ci.mhs.tut

    ServerName ci.mhs.tut

    ServerAlias *.ci.mhs.tut

    DocumentRoot "/var/www/html/ci_multi_site/public_html"

    <Directory "/var/www/html/ci_multi_site/public_html/">

        Options FollowSymLinks

        AllowOverride All

        Order allow,deny

        Allow from all

    </Directory>

</VirtualHost>





###################
What is CodeIgniter
###################

CodeIgniter is an Application Development Framework - a toolkit - for people
who build web sites using PHP. Its goal is to enable you to develop projects
much faster than you could if you were writing code from scratch, by providing
a rich set of libraries for commonly needed tasks, as well as a simple
interface and logical structure to access these libraries. CodeIgniter lets
you creatively focus on your project by minimizing the amount of code needed
for a given task.

*******************
Release Information
*******************

This repo contains in-development code for future releases. To download the
latest stable release please visit the `CodeIgniter Downloads
<http://www.codeigniter.com/download>`_ page.

**************************
Changelog and New Features
**************************

You can find a list of all changes for each release in the `user
guide change log <https://github.com/bcit-ci/CodeIgniter/blob/develop/user_guide_src/source/changelog.rst>`_.

*******************
Server Requirements
*******************

PHP version 5.4 or newer is recommended.

It should work on 5.2.4 as well, but we strongly advise you NOT to run
such old versions of PHP, because of potential security and performance
issues, as well as missing features.

************
Installation
************

Please see the `installation section <http://www.codeigniter.com/user_guide/installation/index.html>`_
of the CodeIgniter User Guide.

*******
License
*******

Please see the `license
agreement <https://github.com/bcit-ci/CodeIgniter/blob/develop/user_guide_src/source/license.rst>`_.

*********
Resources
*********

-  `User Guide <http://www.codeigniter.com/docs>`_
-  `Language File Translations <https://github.com/bcit-ci/codeigniter3-translations>`_
-  `Community Forums <http://forum.codeigniter.com/>`_
-  `Community Wiki <https://github.com/bcit-ci/CodeIgniter/wiki>`_
-  `Community IRC <http://www.codeigniter.com/irc>`_

Report security issues to our `Security Panel <mailto:security@codeigniter.com>`_
or via our `page on HackerOne <https://hackerone.com/codeigniter>`_, thank you.

***************
Acknowledgement
***************

The CodeIgniter team would like to thank EllisLab, all the
contributors to the CodeIgniter project and you, the CodeIgniter user.