FROM php:5.6-apache

# update debian packages
RUN apt-get update

# Install PDO MySQL driver
RUN docker-php-ext-install mysql mysqli pdo pdo_mysql

# Install LDAP driver
RUN apt-get install -y libldap-dev
RUN docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu/
RUN docker-php-ext-install ldap

## Workaround for write permission on write to MacOS X volumes
## See https://github.com/boot2docker/boot2docker/pull/534
#RUN usermod -u 1000 www-data

# Enable Apache mod_rewrite
RUN a2enmod rewrite
