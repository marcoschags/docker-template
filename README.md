# Criar o Projeto Laravel
docker run --rm -v $(pwd)/src:/app composer create-project laravel/laravel .

# Instalar o Livewire
docker compose run --rm app composer require livewire/livewire.

# Subir os contêineres
docker compose up -d

# Executar as migrações (o comando roda dentro do contêiner 'app')
docker compose exec app php artisan migrate