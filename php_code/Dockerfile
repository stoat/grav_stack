FROM php:8.3-fpm
RUN apt-get update && apt-get install -y --no-install-recommends \
        libz-dev \
        libpq-dev \
        libssl-dev \
        libzip-dev \
        libxml2-dev \
        libxml2 \
        libgd-dev libfreetype6-dev libjpeg62-turbo-dev libpng-dev libjpeg-dev jpegoptim libwebp-dev optipng pngquant gifsicle \
        libmcrypt-dev \
        libcurl4-openssl-dev \
        libonig-dev \
        curl \
        unzip \
        zip \
        ca-certificates curl gnupg \
        sendmail \
        sendmail-bin \
        mailutils \
	&& docker-php-ext-configure zip \
	&& docker-php-ext-install zip \
	&& docker-php-ext-configure gd \
          --with-freetype=/usr/include/ \
          --with-jpeg=/usr/lib/x86_64-linux-gnu \
          --with-webp=/usr/lib/x86_64-linux-gnu \
	&& docker-php-ext-install \
        	gd \
        	exif \
        	xml \
        	curl \
        	opcache \
        	intl \
        	pdo_mysql \
        	pdo \
        	pcntl \
        	zip \
        	intl \
        	mysqli \
        	mbstring \
    	&& docker-php-ext-enable mysqli gd \	
	&& apt-get clean -y \
	&& rm -rf /var/lib/apt/lists/*
