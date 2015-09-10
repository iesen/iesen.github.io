---
layout: post
title:  "Docker komutlarını sudo gerektirmeden çalıştırma"
date:   2015-09-10 18:33:55
published: false
---
  
Docker komutlarını sudo gerektirmeden çalıştırma
Docker isminde bir group yaratılır.
$ sudo groupadd docker 
Mevcut user docker grubuna eklenir
$ sudo gpasswd -a ${USER} docker
Docker daemon restart edilir.
$ sudo service docker restart
SSH dan logout olunup tekrar login olunduğunda docker komutlarını sudo ile çalıştırmaya gerek kalmaz.