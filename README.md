

- Setup Docker com mysql
- Timezone ajustado para o Brasil

### Passo a passo
Clone Repositório
```sh
git clone -b main https://github.com/claudiomecenas/setup-docker-laravel-11-BR.git app-laravel
```
```sh
cd app-laravel
```

Crie o Arquivo .env
```sh
cp .env.example .env
```

Edite o .env para usar Redis
```sh
SESSION_DRIVER=redis
QUEUE_CONNECTION=redis  
CACHE_STORE=redis  
REDIS_HOST=redis  
```

Suba os containers do projeto
```sh
docker compose up -d
```

Acesse o container app
```sh
docker compose exec app bash
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
[http://localhost:8989](http://localhost:8989)
