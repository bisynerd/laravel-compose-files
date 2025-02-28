docker exec -it adaa_laravel_app php artisan migrate
docker exec -it adaa_laravel_app php artisan serve
docker run --rm -v $(pwd)/admin.adaa-learning-api:/var/www -w /var/www composer require laravel/sanctum
docker run --rm -v $(pwd)/admin.adaa-learning-api:/var/www -w /var/www composer dump-autoload
docker compose run --rm composer
docker exec -it adaa_laravel_app php artisan make:controller AuthController
docker exec -it adaa_laravel_app php artisan l5-swagger:generate
docker exec -it adaa_laravel_app php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
docker run --rm -v $(pwd)/admin.adaa-learning-api:/var/www -w /var/www composer:2.6 update
docker compose run --rm composer update