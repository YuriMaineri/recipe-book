<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

# Como rodar a aplicação

## 1. Instalar o docker na máquina

- Como instalar o docker no [Linux](https://runnable.com/docker/install-docker-on-linux)
- Como instalar o docker no [Windows](https://docs.docker.com/get-docker/)

## 2. Subir o docker
    2.1 Dentro da pasta do projeto, basta renomear o .env, com esse comando:
> cp .env.example .env

    2.2 Depois basta subir os containers do docker

> docker-compose up -d
- Isso vai subir o **Apache** na porta 80, o **MySQL** na porta 3306 e o **phpMyAdmin** na porta 8080

- Certifique-se de ter essas portas liberadas ou basta mapear para outra porta no docker-compose.yml

### Resultado do comando
```
docker-compose up -d
  Starting mysql      ... done
  Starting apache-php ... done
  Starting pma        ... done
```
## 3. Laravel
O comando a seguir vai instalar os pacotes necessários para rodar o Laravel

> docker exec -t apache-php ./composer.phar install

Acesse a pasta www que é onde ficam os arquivos do Laravel
> cd www

Então renomeei o .env:
> cp .env.example .env

Depois gere a chave do Laravel:
> php artisan key:generate

E de permissão de escrita na pasta de logs:
> chmod -R 777 storage