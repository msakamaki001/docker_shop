# docker_shop
# dockerをインストール. 
https://www.docker.com/products/docker-desktop/. 
# dockerを立ち上げる  
  
# docker_shopをshop_backendと同じディレクトリに置く(例:workdir内に置く).  
workdir$shop_backend docker_shop. 
  
# docker_shopディレクトリ内に入りdockerを立ち上げる. 
$docker-compose up -d --build. 
  
# dbコンテナ内に入る. 
$docker exec -it docker_shop_db_1 bash. 
  
# mysqlを起動する. 
$mysql -u root -p. 
Enter password:(passwordはroot)

# shopデータベースを作成する. 
mysql> create database shop;  
  
# phpコンテナ内に入る
$docker exec -it docker_shop_php_1 bash

# shop_backendディレクトリに入る
$cd /var/www/shop_backend

# composer起動
$composer install

# マイグレーションとシーダー実行
$php artisan migrate:fresh --seed

# シンボリックリンク作成
php artisan storage:link

localhostでアクセスする

作業は以上です. 
