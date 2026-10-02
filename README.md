# Criar o Projeto Laravel
docker run --rm -v $(pwd)/src:/app composer create-project laravel/laravel .

# Instalar o Livewire
docker compose run --rm app composer require livewire/livewire