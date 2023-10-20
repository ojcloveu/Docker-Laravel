# Use php:8.0-fpm as the base image
FROM php:8.0-fpm

# Install required extensions
RUN docker-php-ext-install pdo pdo_mysql

# Set up Composer (you may need to install it first)
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Create a directory for the Laravel application
WORKDIR /var/www/html

# Copy Laravel application files from the 'src' directory
COPY src/ ./

# Set proper permissions (adjust as needed)
RUN chown -R www-data:www-data /var/www/html/storage /var/www/html/bootstrap

USER www-data

CMD ["php-fpm"]
