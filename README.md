<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

## Proje kurulum

##### Projeyi indirme
```
git clone https://github.com/alisanalacam/laravel-passport-deneme.git
cd laravel-passport-deneme
```

##### Projeyi çalıştırma
```
cp .env.example .env
docker-compose up -d
```

##### DB Kullanıcı oluşturma
```
docker-compose exec db bash
mysql -u root -p
GRANT ALL ON laravel.* TO 'laraveluser'@'%' IDENTIFIED BY 'your_laravel_db_password';
FLUSH PRIVILEGES;
EXIT;
exit
```

##### .env dosyasını düzenleme
```
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=laraveluser
DB_PASSWORD=your_laravel_db_password
```


##### Yapılandırma
```
docker-compose exec app php artisan key:generate
docker-compose exec app composer require laravel/passport
docker-compose exec app php artisan passport:install
docker-compose exec app php artisan migrate
```

