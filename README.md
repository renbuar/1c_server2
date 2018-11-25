# 1c_server2

2 сервер

$ cd cd ~/

$ git clone https://github.com/renbuar/1c_server2.git

$ cd ~/1c_server2/8.3.14-1373

$ cp ~/test/1c-enterprise83-common_8.3.14-1373_amd64.deb ~/1c_server2/8.3.14-1373

$ cp ~/test/1c-enterprise83-server_8.3.14-1373_amd64.deb ~/1c_server2/8.3.14-1373

$ cp ~/test/haspd_7.60-eter1ubuntu_amd64.deb ~/1c_server2/8.3.14-1373

$ cp ~/test/haspd-modules_7.60-eter1ubuntu_amd64.deb ~/1c_server2/8.3.14-1373

$ docker build --tag 1c-server2 .

$ docker volume create --name 1c-server2

Запуск тестовый

$ docker run -ti -h u1604 --name 1c-server-2 --rm --privileged -p 2540:2540 -p 2541:2541 -p 2560-2591:2560-2591 -p 475:475 -p2947:2947 -v 1c-server2:/home/usr1cv8 1c-server2:latest

Запуск разовый

$ docker run -d -h u1604 --name 1c-server-2 --rm --privileged -p 2540:2540 -p 2541:2541 -p 2560-1591:2560-1591 -p 475:475 -p1947:1947 -v 1c-server2:/home/usr1cv8 1c-server2:latest

 

Без проброса портов ml:

 

Запуск тестовый

$ docker run -ti -h u1604 --name 1c-server-2 --rm --privileged -p 2540:2540 -p 2541:2541 -p 2560-2591:2560-2591 -v 1c-server2:/home/usr1cv8 1c-server2:latest

Запуск разовый

$ docker run -d -h u1604 --name 1c-server-2 --rm --privileged -p 2540:2540 -p 2541:2541 -p 2560-1591:2560-1591 -v 1c-server2:/home/usr1cv8 1c-server2:latest

 
