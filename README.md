# docker-php7-apache
Docker image PHP 7 and Apache


### Versioning
| Docker Tag | Git Release | Apache Version | PHP Version | Debian Version |
|-----|-------|-----|--------|--------|
| latest | Master Branch | 2.4.25 | 7.3.4 | GNU/Linux 9 |

### Links
- [https://github.com/paliari/docker-php7-apache](https://github.com/paliari/docker-php7-apache)
- [https://hub.docker.com/r/paliari/php7-apache](https://hub.docker.com/r/paliari/php7-apache)

## Quick Start
To pull from docker hub:
```
docker pull paliari/php7-apache:latest
```
### Running
To simply run the container:
```
sudo docker run -d paliari/php7-apache

sduo docker run -p 80:80 -d -e 'WEBROOT=/var/www/html/public' -e 'SET_PHP_INI_ENV=production' -e 'PHP_MEM_LIMIT=20' -e 'PHP_POST_MAX_SIZE=10' -e 'PHP_UPLOAD_MAX_FILESIZE=10' paliari/php-fpm-nginx:latest
```

### Environments custom
| Name | Type | Default | Info | 
|-----|-----|-----|-----|
| WEBROOT | string | /var/www/html | Set custom webroot |
| PHP_MEM_LIMIT | integer | 128 | Define PHP memory limit in MB |
| PHP_POST_MAX_SIZE | integer | 100 | Define PHP post max size in MB |
| PHP_UPLOAD_MAX_FILESIZE | integer | 100 | Define PHP upload max filesize in MB |
| TIMEZONE | string | UTC | Set custom timezone |
| SET_PHP_INI_ENV | enum(development, production) | | If defined, create /usr/local/etc/php/php.ini (recommended in production) |

