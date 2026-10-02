FROM php:8.2-fpm

# Instalar dependências do sistema e extensões PHP
RUN apt-get update && apt-get install -y \
    git \
    curl \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    unzip \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Instalar o Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Definir diretório de trabalho
WORKDIR /var/www

# Ajustar permissões (opcional, mas útil)
RUN chown -R www-data:www-data /var/www

EXPOSE 9000
CMD ["php-fpm"]