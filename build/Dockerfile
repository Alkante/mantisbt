FROM docker.alkante.com/alk-apache:1-php8.2
# Install php8.2-mysql
RUN apt-get update && \
    apt-get install -y php8.2-mysql
# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer && chmod 777 /var/www
# End
RUN apt-get clean && \
    rm -rf /tmp/* /var/tmp/*
