# Sử dụng PHP 8.2 FPM
FROM php:8.2-fpm

# Cài đặt các extension PHP cần thiết cho Laravel
RUN docker-php-ext-install pdo pdo_mysql

# Cài đặt Composer
COPY --from=composer /usr/bin/composer /usr/bin/composer

# Chọn thư mục làm việc
WORKDIR /var/www

# Copy toàn bộ mã nguồn vào container
COPY . .

# Cấp quyền cho thư mục storage và bootstrap/cache
RUN chown -R www-data:www-data /var/www/storage /var/www/bootstrap/cache
