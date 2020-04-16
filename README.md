<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

# Como rodar a aplicação

## Instalar o docker na máquina

- Como instalar o docker no [Linux](https://runnable.com/docker/install-docker-on-linux)
- Como instalar o docker no [Windows](https://docs.docker.com/get-docker/)

**Após ter o docker instalado para rodar os seguintes comandos dentro da pasta do projeto**

- $ docker-compose up -d
> Isso vai subir o **Apache** na porta 80, o **MySQL** na porta 3306 e o **phpMyAdmin** na porta 8080

> Certifique-se de ter essas portas liberadas ou basta mapear para outra porta no docker-compose.yml

### Resultado do comando
```
    docker-compose up -d
       Starting mysql      ... done
       Starting apache-php ... done
       Starting pma        ... done
```
#### Instalação dos pacotes via composer para rodar o Laravel
- $ docker exec -t apache-php ./composer.phar install