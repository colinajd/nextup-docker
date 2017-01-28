# Docker config for zlshames/nextup
  My Docker setup for this project
### Installation Instuctions
  1. Install Docker Native [Link Here](https://www.docker.com/products/overview#/install_the_platform)
  2. Clone/add submodule to the main project repo
  3. Run this inside the docker folder `docker-compose build`
  4. Once the build is finished run `docker-compose up -d`
  5. When containers have started run `docker-compose exec --user docker workspace bash`
  6. Install all dependencies - `composer install && npm install`
  7. Copy .env.example to env then add the db credentials
  
  ```
    DB_CONNECTION=pgsql
    DB_HOST=10.0.75.2
    DB_PORT=5432
    DB_DATABASE=nextup
    DB_USERNAME=homestead
    DB_PASSWORD=secret
   ```
  8. Finally run `php aritsan key:generate && php artisan migrate`
