# docker-soplanning
## Informations
Soplanning docker files use to develop [Soplanning](http://www.soplanning.org) with:
 - Soplanning source code or specific fork
 - Imported database from production environment

The docker environment uses:
- [mysql](https://github.com/docker-library/mysql/blob/ae850f69e7414a7c28e8d364ae039fe0a0464e7a/5.5/Dockerfile) container
- [php-apache](https://github.com/docker-library/php/blob/3cb02a21164bc2bdb8b25ec48886ffcb7e195510/5.6/apache/Dockerfile) container

## How-to
To enhance ;)

 1. Edit `docker-compose.yml` file if you want to change mysql parameters
 2. Edit the `database.inc` file in soplanning source code to match with mysql
container parameters (be careful with IP/hostname !)
 3. Edit docker-compose.yml file if you want to change source code folder
 4. run `docker-compose up`
 5. go to http://localhost to log in
 6. Enjoy!

## License
The code is licensed under the "BSD 3-Clause License".
