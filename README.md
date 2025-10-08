# Change Xampp Php Version
How to change xampp php version to 8.4.

## Download php

Download https://downloads.php.net/~windows/releases/archives/php-8.4.13-Win32-vs17-x64.zip and unzip (https://www.php.net/downloads.php).

## Simple way

Just overwrite files in **/xampp/php** directory.

## Second way

Unzip to **php** directory on disk **C**.

### Change xampp settings

Go to **https-xampp.conf** and change all paths from **/xampp/php** to **/php**.

### Windows 10 environment variables

Run command, press **ALT + R** and type **sysdm.cpl** and click OK. See in advanced tab environment variables and add in **Path**. 

```sh
# Change C:/xampp/php to C:/php or remove from environment variables and add new line:

C:/php
```


### Create php.ini

Copy from **php.ini-development** and add in **php.ini** file path to extensions directory (if you want to place php in different location).

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

### Check in cmd

```sh
php -v
php -m
```

### Add in xampp
C:\xampp\htdocs\index.php

```
<?php
  phpinfo();
  die();
?>
```


### Check php version in browser

http://localhost

## VsCode settings

```json
{
  "php.validate.executablePath": "C:/php/php.exe"
}
```
