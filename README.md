By default Ubuntu 16.04 (Xenial) now comes with php 7.0

You can install php 5.6 in parallel and switch between them using the following instructions:

add-apt-repository ppa:ondrej/php
apt update
apt install php5.6 libapache2-mod-php5.6 php5.6-curl php5.6-gd php5.6-mbstring php5.6-mcrypt php5.6-mysql php5.6-xml php5.6-xmlrpc
a2dismod php7.0
a2enmod php5.6
systemctl restart apache2

    See www.lornajane.net/…6-on-ubuntu for another how-to
    An update in 2017 included the following notice:

NOTICE: Not enabling PHP 5.6 FPM by default.
NOTICE: To enable PHP 5.6 FPM in Apache2 do:
NOTICE: a2enmod proxy_fcgi setenvif
NOTICE: a2enconf php5.6-fpm
NOTICE: You are seeing this message because you have apache2 package installed.
