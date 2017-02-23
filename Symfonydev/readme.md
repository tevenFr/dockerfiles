# Symfony dev dockerfile
A dockerfile with ubuntu:xenial + php 7.1 + mariadb + composer + symfony installer 

Caution : this container is unsafe, was made for rapidly pop a symfony dev env at screen from existing files.

## instructions
  Caution: use this container for demo purpose only.
  Run the container, mount the volume and put your symfony files into it
  
  This is the defaults database parameters you need in your parameters.yml
  ```yml
  database_host: localhost
  database_port: ~
  database_name: symfony
  database_user: root
  database_password: ~
  ```
  
  After, launch this multiples exec in container
  ```sh
$ service mysql start
$ mysql -e "CREATE DATABASE symfony"
$ chmod a+x -R .
$ composer update
$ php bin/console doctrine:schema:create
$ php bin/console server:run 0.0.0.0:8000
```

## Contributions

I would appreciate contributions for this features :
+mysql service start debugging - actualy not working with dockerfile
+yours
