# docker_shop
dockerをインストール. 
https://www.docker.com/products/docker-desktop/. 
dockerを立ち上げる  
  
docker_shopをshop_backendと同じディレクトリに置く(例:workdir内に置く). 
$ls
workdir$shop_backend docker_shop. 
  
docker_shopを立ち上げる  
$docker-compose up -d -build. 
  
dbコンテナ内に入る. 
$docker exec -it docker_shop_db_1 bash. 
  
mysqlを起動する. 
$mysql -u root -p  
Enter password:(passwordはroot)

shopデータベースを作成する. 
mysql> show databases;  
+--------------------+. 
| Database           |. 
+--------------------+. 
| default            |. 
| information_schema |. 
| mysql              |. 
| performance_schema |. 
| sys                |. 
+--------------------+. 
6 rows in set (0.00 sec). 
  
mysql> create database shop;  
  
mysql> show databases;  
+--------------------+. 
| Database           |. 
+--------------------+. 
| default            |. 
| information_schema |. 
| mysql              |. 
| performance_schema |. 
| shop               |. 
| sys                |. 
+--------------------+. 
6 rows in set (0.01 sec). 
  
docker側の作業は以上です. 
