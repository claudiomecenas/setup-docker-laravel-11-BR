
# Setup Docker Laravel 11 com PHP 8.3
[By prof. Carlos Ferreira - Especializa TI](https://github.com/especializati/setup-docker-laravel)

- Setup Ajustado para uso do mysql
- Timezone ajustado para o Brasil

### Passo a passo
Clone Repositório
```sh
git clone -b setup-docker-laravel-11-BR https://github.com/claudiomecenas/setup-docker-laravel-11-BR.git app-laravel
```
```sh
cd app-laravel
```

Crie o Arquivo .env
```sh
cp .env.example .env
```

Suba os containers do projeto
```sh
docker-compose up -d
```

Acesse o container app
```sh
docker-compose exec app bash
```


Instale as dependências do projeto
```sh
composer install
```

Gere a key do projeto Laravel
```sh
php artisan key:generate
```

Rodar as migrations
```sh
php artisan migrate
```

Acesse o projeto
[http://localhost:8000](http://localhost:8000)
