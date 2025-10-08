# Xampp php 8.4
How to change xampp php version.

## Download php

Download https://downloads.php.net/~windows/releases/archives/php-8.4.13-Win32-vs17-x64.zip and unzip.

## Overweite xampp php

Simple method, just overwrite files in **/xampp/php**. Long method unzip to **php** directory on disk **C**

## Change Xampp settings

Go to **https-xampp.conf** and change all paths from **/xampp/php** to **/php** or **/your/php/location**.

## Env variables

Add env variables path in windows.

```sh
C:/php
```

## Create php.ini

Copy from **php.ini-development** and add in php.ini file path to extensions directory (if you want to place php in different location).

```sh
[PHP]

# Php extension directory
extension_dir="./ext"

# Unhash extensions

extension=bz2
extension=curl
extension=ftp
extension=fileinfo
extension=gd
extension=gettext
extension=intl
extension=mbstring
extension=exif
extension=openssl
extension=pdo_mysql
extension=pdo_sqlite
extension=sockets
extension=sqlite3
extension=zip
zend_extension=opcache
```
