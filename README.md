## «Система мониторинга Zabbix» Вознюк Ольга

### Задание 1

*Авторизация в админке*

![alt text](./img/auth_zabbix.png)

*Использованные команды из `history`*

```
    5  wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4%2Bdebian11_all.deb
    6  sudo dpkg -i zabbix-release_6.0-4+debian11_all.deb 
    7  sudo apt update
    8  ls 
    9  sudo dpkg -i zabbix-release_6.0-4+debian11_all.deb 
   10  apt update 
   11  echo "deb http://ftp.de.debian.org/debian stretch main" >> /etc/apt/sources.list
   12  apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y php7.0-pgsql
   13  nano /etc/apt/sources.list
   14  apt update 
   15  sudo apt-get update
   16  sudo apt -y install software-properties-common
   17  sudo add-apt-repository ppa:ondrej/php
   18  sudo apt-get update
   19  sudo apt -y install php7.4
   20  apt update 
   21  sudo apt -y install php7.4
   22  sudo add-apt-repository ppa:ondrej/php
   23  hp -v
   24  php -v
   25  sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath
   26  sudo add-apt-repository ppa:sergey-dryabzhinsky/php74
   27  sudo add-apt-repository ppa:sergey-dryabzhinsky/php7-modules
   28  sudo add-apt-repository ppa:sergey-dryabzhinsky/backports
   29  sudo add-apt-repository ppa:sergey-dryabzhinsky/packages
   30  apt upgrade 
   31  apt update 
   32  sudo apt install -y apt-transport-https lsb-release ca-certificates wget 
   33  wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
   34  echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/sury-php.list
   35  sudo wget -qO - https://packages.sury.org/php/apt.gpg | sudo gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/debian-php-8.gpg --import
   36  sudo chmod 644 /etc/apt/trusted.gpg.d/debian-php-8.gpg
   37  apt update 
   38  rm /etc/apt/sources.list.d/sury-php.list 
   39  apt update 
   40  wget https://www.php.net/distributions/php-7.4.0.tar.gz
   41  ls 
   42  tar -xvzf php-7.4.0.tar.gz 
   43  ls 
   44  cd php-7.4.0/
   45  ./configure 
   46  make install
   47  apt install make 
   48  make install
   49  make install .
   50  make install .
   51  ./configure \
   52  ./configure
   53  make install
   54  apt install php libapache2-mod-php
   55  systemctl restart apache2
   56  systemctl status apache
   57  systemctl status apache2.service 
   58  php -v
   59  apt install php7.4-pgsql
   60  wget http://archive.ubuntu.com/ubuntu/pool/main/p/php7.4/php7.4-pgsql_7.4.3-4ubuntu2.23_amd64.deb
   61  ls 
   62  dpkg -i php7.4-pgsql_7.4.3-4ubuntu2.23_amd64.deb 
   63  wget http://archive.ubuntu.com/ubuntu/pool/main/p/php7.4/php7.4-common_7.4.3-4ubuntu1_amd64.deb
   64  dpkg -i php7.4-common_7.4.3-4ubuntu1_amd64.deb 
   65  apt-get install php7.4-common
   66  apt --fix-broken install
   67  apt-get install php7.4-common
   68  wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
   69   apt install zabbix-server-pgsql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts nano -y # zabbix-agent
   70  apt install libldap-2.4-2
   71  apt install libldap-common 
   72  apt search libssl
   73  apt install libssl1.1
   74  apt install libssl
   75  apt-get install libssl-dev
   76   apt install zabbix-server-pgsql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts nano -y # zabbix-agent
   77   libldap-common  --version
   78  apt-get install libldap2-dev=2.4.31-1+nmu2ubuntu8.2
   79  apt remove libldap-2.5-0 
   80  apt-get install libldap2-dev=2.4.31-1+nmu2ubuntu8.2
   81  apt-get install libldap2-dev checkinstall
   82   apt install zabbix-server-pgsql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts nano -y # zabbix-agent
   83   apt install zabbix-server-pgsql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts nano -y # zabbix-agent
   84  docker ps 
   85   apt install zabbix-server-pgsql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts
   86   apt install zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts
   87   apt install zabbix-server-pgsql
   88  cat /etc/os-release 
   89  apt remove zabbix-release
   90  curl -LO https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1%2Bdebian12_all.deb
   91  apt install curl
   92  curl -LO https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1%2Bdebian12_all.deb
   93  dpkg -i zabbix-release_6.4-1%2Bdebian12_all.deb 
   94  apt update 
   95  apt install zabbix-server-pgsql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts zabbix-agent2
   96  systemctl status zabbix-server.service 
   97  systemctl start zabbix-server.service 
   98  systemctl enable zabbix-server.service 
   99  systemctl status zabbix-server.service 
  100  sudo -u postgres createuser --pwprompt zabbix
  101  systemctl stop zabbix-server.service 
  102  systemctl status zabbix-server.service 
  103  su - postgres
  104  apt install postgresql-15
  105  sudo -u postgres createuser --pwprompt zabbix
```
 

 ### Задание 2

 *скриншот раздела Configuration > Hosts, где видно, что агенты подключены к серверу*

 ![alt text](./img/conf_servers.png)

 *скриншот лога zabbix agent*

 ![alt text](./img/zabbix_logs.png)

 *скриншот раздела Monitoring > Latest data*

 ![alt text](./img/latest_data.png)

 *Использованные команды из `history`*

```
wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian12_all.deb
--2024-07-28 12:49:54--  https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian12_all.deb
Resolving repo.zabbix.com (repo.zabbix.com)... 178.128.6.101
Connecting to repo.zabbix.com (repo.zabbix.com)|178.128.6.101|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3540 (3.5K) [application/octet-stream]
Saving to: ‘zabbix-release_6.4-1+debian12_all.deb’

zabbix-release_6.4-1+debian12_all.deb           100%[=====================================================================================================>]   3.46K  --.-KB/s    in 0s      

2024-07-28 12:49:55 (21.5 MB/s) - ‘zabbix-release_6.4-1+debian12_all.deb’ saved [3540/3540]

root@ans2:~# wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian12_all.deb^C
root@ans2:~# dpkg -i zabbix-release_6.4-1+debian12_all.deb
Selecting previously unselected package zabbix-release.
(Reading database ... 34374 files and directories currently installed.)
Preparing to unpack zabbix-release_6.4-1+debian12_all.deb ...
Unpacking zabbix-release (1:6.4-1+debian12) ...
Setting up zabbix-release (1:6.4-1+debian12) ...
root@ans2:~# apt update
Get:1 http://security.debian.org/debian-security bookworm-security InRelease [48.0 kB]
Get:2 http://deb.debian.org/debian bookworm InRelease [151 kB]                                       
Get:3 http://deb.debian.org/debian bookworm-updates InRelease [55.4 kB]            
Get:4 http://security.debian.org/debian-security bookworm-security/main Sources [105 kB]
Get:5 http://security.debian.org/debian-security bookworm-security/main amd64 Packages [169 kB]
Get:6 http://security.debian.org/debian-security bookworm-security/main Translation-en [102 kB]   
Get:7 http://deb.debian.org/debian bookworm/non-free-firmware Sources [6,456 B]                               
Get:8 http://deb.debian.org/debian bookworm/main Sources [9,485 kB]
Get:9 https://repo.zabbix.com/zabbix/6.4/debian bookworm InRelease [2,874 B]     
Get:10 https://repo.zabbix.com/zabbix/6.4/debian bookworm/main Sources [17.4 kB]
Get:11 http://deb.debian.org/debian bookworm/main amd64 Packages [8,788 kB]
Get:12 https://repo.zabbix.com/zabbix/6.4/debian bookworm/main amd64 Packages [46.8 kB]
Get:13 https://repo.zabbix.com/zabbix/6.4/debian bookworm/main all Packages [9,731 B]          
Get:14 http://deb.debian.org/debian bookworm/main Translation-en [6,109 kB]
Get:15 http://deb.debian.org/debian bookworm/non-free-firmware amd64 Packages [6,216 B]
Fetched 25.1 MB in 4s (6,195 kB/s)                      
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
42 packages can be upgraded. Run 'apt list --upgradable' to see them.
N: Repository 'http://deb.debian.org/debian bookworm InRelease' changed its 'Version' value from '12.5' to '12.6'
root@ans2:~# apt install zabbix-agent
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  libcurl3-gnutls libcurl4 libmodbus5
The following NEW packages will be installed:
  libcurl4 libmodbus5 zabbix-agent
The following packages will be upgraded:
  libcurl3-gnutls
1 upgraded, 3 newly installed, 0 to remove and 41 not upgraded.
Need to get 1,496 kB of archives.
After this operation, 2,080 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://deb.debian.org/debian bookworm/main amd64 libcurl3-gnutls amd64 7.88.1-10+deb12u6 [385 kB]
Get:2 http://deb.debian.org/debian bookworm/main amd64 libcurl4 amd64 7.88.1-10+deb12u6 [390 kB]
Get:3 http://deb.debian.org/debian bookworm/main amd64 libmodbus5 amd64 3.1.6-2.1 [31.3 kB]
Get:4 https://repo.zabbix.com/zabbix/6.4/debian bookworm/main amd64 zabbix-agent amd64 1:6.4.17-1+debian12 [690 kB]
Fetched 1,496 kB in 4s (395 kB/s)      
Reading changelogs... Done
(Reading database ... 34380 files and directories currently installed.)
Preparing to unpack .../libcurl3-gnutls_7.88.1-10+deb12u6_amd64.deb ...
Unpacking libcurl3-gnutls:amd64 (7.88.1-10+deb12u6) over (7.88.1-10+deb12u5) ...
Selecting previously unselected package libcurl4:amd64.
Preparing to unpack .../libcurl4_7.88.1-10+deb12u6_amd64.deb ...
Unpacking libcurl4:amd64 (7.88.1-10+deb12u6) ...
Selecting previously unselected package libmodbus5:amd64.
Preparing to unpack .../libmodbus5_3.1.6-2.1_amd64.deb ...
Unpacking libmodbus5:amd64 (3.1.6-2.1) ...
Selecting previously unselected package zabbix-agent.
Preparing to unpack .../zabbix-agent_1%3a6.4.17-1+debian12_amd64.deb ...
Unpacking zabbix-agent (1:6.4.17-1+debian12) ...
Setting up libmodbus5:amd64 (3.1.6-2.1) ...
Setting up libcurl3-gnutls:amd64 (7.88.1-10+deb12u6) ...
Setting up libcurl4:amd64 (7.88.1-10+deb12u6) ...
Setting up zabbix-agent (1:6.4.17-1+debian12) ...
Created symlink /etc/systemd/system/multi-user.target.wants/zabbix-agent.service → /lib/systemd/system/zabbix-agent.service.
Processing triggers for man-db (2.11.2-2) ...
Processing triggers for libc-bin (2.36-9+deb12u7) ...
root@ans2:~# systemctl restart zabbix-agent
root@ans2:~# systemctl enable zabbix-agent
Synchronizing state of zabbix-agent.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable zabbix-agent
root@ans2:~# systemctl status zabbix-agent.service 
● zabbix-agent.service - Zabbix Agent
     Loaded: loaded (/lib/systemd/system/zabbix-agent.service; enabled; preset: enabled)
     Active: active (running) since Sun 2024-07-28 12:51:47 EDT; 47s ago
   Main PID: 1149 (zabbix_agentd)
      Tasks: 6 (limit: 2307)
     Memory: 4.3M
        CPU: 25ms
     CGroup: /system.slice/zabbix-agent.service
             ├─1149 /usr/sbin/zabbix_agentd -c /etc/zabbix/zabbix_agentd.conf
             ├─1150 "/usr/sbin/zabbix_agentd: collector [idle 1 sec]"
             ├─1151 "/usr/sbin/zabbix_agentd: listener #1 [waiting for connection]"
             ├─1152 "/usr/sbin/zabbix_agentd: listener #2 [waiting for connection]"
             ├─1153 "/usr/sbin/zabbix_agentd: listener #3 [waiting for connection]"
             └─1154 "/usr/sbin/zabbix_agentd: active checks #1 [idle 1 sec]"

Jul 28 12:51:47 ans2 systemd[1]: zabbix-agent.service: Deactivated successfully.
Jul 28 12:51:47 ans2 systemd[1]: Stopped zabbix-agent.service - Zabbix Agent.
Jul 28 12:51:47 ans2 systemd[1]: Starting zabbix-agent.service - Zabbix Agent...
Jul 28 12:51:47 ans2 systemd[1]: Started zabbix-agent.service - Zabbix Agent.
root@ans2:~# ss -tlpn | grep 10050
LISTEN 0      4096         0.0.0.0:10050      0.0.0.0:*    users:(("zabbix_agentd",pid=1154,fd=4),("zabbix_agentd",pid=1153,fd=4),("zabbix_agentd",pid=1152,fd=4),("zabbix_agentd",pid=1151,fd=4),("zabbix_agentd",pid=1150,fd=4),("zabbix_agentd",pid=1149,fd=4))
LISTEN 0      4096            [::]:10050         [::]:*    users:(("zabbix_agentd",pid=1154,fd=5),("zabbix_agentd",pid=1153,fd=5),("zabbix_agentd",pid=1152,fd=5),("zabbix_agentd",pid=1151,fd=5),("zabbix_agentd",pid=1150,fd=5),("zabbix_agentd",pid=1149,fd=5))

```


## «Система мониторинга Zabbix. часть 2» Вознюк Ольга
 ### Задание 1

 ![alt text](./img/items_add.png)
 
 ### Задание 2-3

 ![alt text](./img/hosts.png)

 ### Задание 4

 ![alt text](./img/dashboard.png)


## «Кластеризация и балансировка нагрузки»
 ### Задание 1

 * конфигурационный файл haproxy

 ```
 (my-venv) user@debian:~/my-venv/bin$ cat /etc/haproxy/haproxy.cfg
global
	log /dev/log local0
	user haproxy
	group haproxy
	daemon

defaults
	log global
	option httplog
	timeout connect 5000ms
	timeout client 50000ms
	timeout server 50000ms

frontend http_front
	bind *:8081
	default_backend http_back

backend http_back
	balance roundrobin
	server server1 127.0.0.1:9000 check
	server server2 127.0.0.1:9001 check
```  
* перенаправление запросов на разные серверы при обращении к HAProxy.
![alt text](./img/haproxy.png)

### Задание 2

* конфиг `haproxy.cfg`

```
user@debian:~$ cat /etc/haproxy/haproxy.cfg
global
	log /dev/log local0
	user haproxy
	group haproxy
	daemon

defaults
	log global
	option httplog
	timeout connect 5000ms
	timeout client 50000ms
	timeout server 50000ms

frontend example
	bind *:8081
	acl ACL_example_local hdr(host) -i example.local
	use_backend web_servers if ACL_example_local

backend web_servers
	mode http
	balance roundrobin
	option httpchk
	http-check send meth GET uri /index.html
	server server1 127.0.0.1:9000 weight 2
	server server2 127.0.0.1:9001 weight 3
	server server3 127.0.0.1:9002 weight 4   
```

* пример запросов с указанием `example.local`

![alt text](./img/haproxy_with_example.local.png)

* пример запросов без указания `example.local`

![alt text](./img/haproxy_without_example.local.png)



## Резервное копирование
### Задание1

* команда rsync и результат её выполнения

![alt text](./img/rsync.png)

### Задание2
 * скрипт backup

```
user@ans2:~$ cat backup.sh 
#!/bin/bash

# Задаем переменные
SOURCE_DIR=~
BACKUP_DIR=/tmp/backup
LOG_FILE=/tmp/backup/backup.log
DATE=$(date '+%Y-%m-%d %H:%M:%S')

# Создаем директорию для резервных копий, если она не существует
mkdir -p $BACKUP_DIR

# Выполняем резервное копирование с rsync
if rsync -av --exclude='.*' --checksum $SOURCE_DIR/ $BACKUP_DIR/ >> $LOG_FILE 2>&1; then
    echo "$DATE: Backup successful" >> $LOG_FILE
else
    echo "$DATE: Backup failed" >> $LOG_FILE
fi
```
* файл crontab

```
user@ans2:~$ crontab -l
# Edit this file to introduce tasks to be run by cron.
# 
# Each task to run has to be defined through a single line
# indicating with different fields when the task will be run
# and what command to run for the task
# 
# To define the time you can provide concrete values for
# minute (m), hour (h), day of month (dom), month (mon),
# and day of week (dow) or use '*' in these fields (for 'any').
# 
# Notice that tasks will be started based on the cron's system
# daemon's notion of time and timezones.
# 
# Output of the crontab jobs (including errors) is sent through
# email to the user the crontab file belongs to (unless redirected).
# 
# For example, you can run a backup of all your user accounts
# at 5 a.m every week with:
# 0 5 * * 1 tar -zcf /var/backups/home.tgz /home/
# 
# For more information see the manual pages of crontab(5) and cron(8)
# 
# m h  dom mon dow   command
54 10 * * * /bin/bash ~/backup.sh
```
* результат работы утилиты

![alt text](./img/crontab.png)

## Отказоустойчивость в облаке
### Задание 1

* Terraform playbook

```
# Объявление переменных для конфиденциальных параметров

variable "folder_id" {
  type = string
}

variable "vm_user" {
  type = string
}

variable "ssh_key" {
  type      = string
  sensitive = true
}

# Настройка провайдера

terraform {
  required_providers {
    yandex = {
      source = "yandex-cloud/yandex"
      version = ">= 0.47.0"
    }
  }
}

provider "yandex" {
  zone = "ru-central1-a"
  token     = "secret_token"
  folder_id = var.folder_id

}

# Создание сервисного аккаунта и назначение ему ролей

resource "yandex_iam_service_account" "for-autoscale" {
  name = "for-autoscale"
}

resource "yandex_resourcemanager_folder_iam_member" "vm-autoscale-sa-role-compute" {
  folder_id = var.folder_id
  role      = "editor"
  member    = "serviceAccount:${yandex_iam_service_account.for-autoscale.id}"
}

# Создание облачной сети и подсетей

resource "yandex_vpc_network" "network-1" {
  name = "network-1"
}

resource "yandex_vpc_subnet" "vm-autoscale-subnet-a" {
  name           = "vm-autoscale-subnet-a"
  zone           = "ru-central1-a"
  v4_cidr_blocks = ["192.168.1.0/24"]
  network_id     = yandex_vpc_network.network-1.id
}

resource "yandex_vpc_subnet" "vm-autoscale-subnet-b" {
  name           = "vm-autoscale-subnet-b"
  zone           = "ru-central1-b"
  v4_cidr_blocks = ["192.168.2.0/24"]
  network_id     = yandex_vpc_network.network-1.id
}

# Создание группы безопасности

resource "yandex_vpc_security_group" "sg-1" {
  name                = "sg-autoscale"
  network_id          = yandex_vpc_network.network-1.id
  egress {
    protocol          = "ANY"
    description       = "any"
    v4_cidr_blocks    = ["0.0.0.0/0"]
  }
  ingress {
    protocol          = "TCP"
    description       = "ext-http"
    v4_cidr_blocks    = ["0.0.0.0/0"]
    port              = 80
  }
  ingress {
    protocol          = "TCP"
    description       = "healthchecks"
    predefined_target = "loadbalancer_healthchecks"
    port              = 80
  }
}

# Указание готового образа ВМ

data "yandex_compute_image" "autoscale-image" {
  family = "container-optimized-image"
}

# Создание группы ВМ

resource "yandex_compute_instance_group" "autoscale-group" {
  name                = "autoscale-vm-ig"
  folder_id           = var.folder_id
  service_account_id  = yandex_iam_service_account.for-autoscale.id
  instance_template {

    platform_id = "standard-v3"
    resources {
      memory = 2
      cores  = 2
    }
  
    boot_disk {
      mode = "READ_WRITE"
      initialize_params {
        image_id = data.yandex_compute_image.autoscale-image.id
        size     = 30
      }
    }

    network_interface {
      network_id = yandex_vpc_network.network-1.id
      subnet_ids = [
        yandex_vpc_subnet.vm-autoscale-subnet-a.id,
        yandex_vpc_subnet.vm-autoscale-subnet-b.id
      ]
      
      nat                = true
    }

    metadata = {
      user-data = templatefile("config.tpl", {
        VM_USER = var.vm_user
        SSH_KEY = var.ssh_key
      })
      docker-container-declaration = file("declaration.yaml")
    }
  }

  scale_policy {
    auto_scale {
      initial_size           = 2
      measurement_duration   = 60
      cpu_utilization_target = 40
      min_zone_size          = 1
      max_size               = 6
      warmup_duration        = 120
    }
  }

  allocation_policy {
    zones = [
      "ru-central1-a",
      "ru-central1-b"
    ]
  }

  deploy_policy {
    max_unavailable = 1
    max_expansion   = 0
  }

  load_balancer {
    target_group_name        = "auto-group-tg"
    target_group_description = "load balancer target group"
  }
}

# Создание сетевого балансировщика

resource "yandex_lb_network_load_balancer" "balancer" {
  name = "group-balancer"

  listener {
    name        = "http"
    port        = 80
    target_port = 80
  }

  attached_target_group {
    target_group_id = yandex_compute_instance_group.autoscale-group.load_balancer[0].target_group_id
    healthcheck {
      name = "tcp"
      tcp_options {
        port = 80
      }
    }
  }
}
```

* Скриншот статуса балансировщика и целевой группы

![alt text](./img/load_balancer.png) 

![alt text](./img/vm_groups.png) 

* Скриншот страницы, которая открылась при запросе IP-адреса балансировщика

![alt text](./img/ip_load_balancer.png)

## Базы данных, их типы
### Задание 1 СУБД

> Кейс
> Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.
>
> Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?
>
> 1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.
>
> 1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы?
>
> 1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.
>
> 1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?
>
> 1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.
>
> 1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это реализовать?
>
> 1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.
>
> 1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД логистов?
>
> 1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?
>
> Приведите ответ в свободной форме.
 

 > 1.1. Для бюджетирования проектов и формирования аналитических отчётов наилучшим вариантом будет использование реляционной СУБД, такой как PostgreSQL или MySQL. Эти СУБД обеспечивают строгую целостность данных благодаря поддержке транзакционности и механизмам проверки целостности. Они также прекрасно подходят для формирования комплексных отчетов с использованием SQL-запросов.

> 1.1.* Для ускорения процессов хеширования можно рассмотреть использование API, таких как OpenSSL или Bouncy Castle. Эти библиотеки предлагают быстрые и эффективные алгоритмы хеширования, которые могут значительно сократить время обработки.

> 1.2. Для лендингов и CRM целесообразно использовать NoSQL базы данных, такие как MongoDB или Firebase Firestore. Они обладают высокой гибкостью и быстро справляются с большими объемами неструктурированных данных, что идеально подходит для динамично меняющихся данных от пользователей.

> 1.2.* Да, эту задачу можно закрыть одной СУБД. Рекомендуется использовать MongoDB, которая прекрасно подойдёт как для хранения данных лендингов, так и для CRM. Она обеспечивает гибкость в хранении разнообразной информации и высокую скорость доступа.

> 1.3. Для создания базы по корпоративным нормам и обучающим материалам можно использовать ту же реляционную СУБД, что и для бюджетирования. Например, PostgreSQL может служить отличной основой для хранения как финансовых отчетов, так и структурированных данных по нормативам. Структуру таблиц можно адаптировать для хранения различных типов данных и связи между ними.

> 1.3.* Да, можно использовать уже существующую СУБД. Лучше всего это реализовать, добавив новые таблицы и отношения в той же базе данных, используемой для задач 1.1. Это позволит избежать избыточности данных и упростит администрирование.

> 1.4. Для задач логистики можно использовать графовые СУБД, такие как Neo4j, которые отлично работают со связями между объектами. Это подойдет для быстрого формирования маршрутов и управления курьерами. 

> 1.4.* Подразделение закупок можно подключить к графовой СУБД, что позволит им использовать данные о маршрутах и поставках. Если в закупках также нужны специфические данные, может потребоваться интеграция с реляционной СУБД.

> 1.5.* Да, все перечисленные задачи можно решить, используя одну СУБД, но это зависит от конкретных требований к данным. Рекомендуемая СУБД — PostgreSQL, так как она поддерживает как реляционные, так и некоторые NoSQL-принципы через расширения, что позволяет решать все поставленные задачи в рамках одной системы.
 
### Задание 2. Транзакции

> 2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. > Ориентируйтесь на шесть действий.

> 2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

**2.1. Пошаговые действия для успешного пополнения баланса счёта телефона:**

> 1. **Аутентификация пользователя:** Пользователь вводит свои учетные данные (логин и пароль) для доступа к системе. Проверяется, существует ли аккаунт и правильность введённых данных.

> 2. **Запрос на пополнение:** После успешной аутентификации пользователь выбирает опцию пополнения счёта и вводит необходимую сумму, которую он хочет внести на свой баланс.

> 3. **Проверка наличия средств:** Система проверяет, достаточно ли средств на банковском счёте или в другой платежной системе, выбранной пользователем для пополнения. Если средств недостаточно, транзакция отменяется.

> 4. **Создание транзакции:** Система генерирует уникальный идентификатор транзакции и сохраняет её состояние как ожидающее. Это необходимо для отслеживания и возможного восстановления транзакции в случае сбоя.

> 5. **Обработка платежа:** Система отправляет запрос на обработку платежа в соответствующий платежный шлюз или банк для списания средств. Платежный шлюз выполняет запрос и возвращает статус транзакции (успех или ошибка).

> 6. **Обновление баланса:** Если обработка платежа прошла успешно, система обновляет баланс пользователя, отражая новое значение. Пользователь получает уведомление о завершении транзакции и актуальном балансе.

> **2.1.* Действия при автоплатеже:**

> 1. **Аутентификация пользователя:** Как и в случае с ручным пополнением, система удостоверяется, что пользователь имеет активный аккаунт и учётные данные.

> 2. **Настройка автоплатежа:** Пользователь предварительно настраивает автоплатеж, выбирая сумму, периодичность (например, ежемесячно) и банковский счёт или платежную систему, с которой будут списываться средства.

> 3. **Запланированное выполнение:** Система отслеживает расписание автоплатежа. В назначенное время производится автоматическая генерация транзакции, без необходимости ручного вмешательства.

> 4. **Проверка наличия средств:** Перед списанием средств система проверяет наличие достаточной суммы на счёте пользователя.

> 5. **Обработка платежа:** Система отправляет запрос на автоматическую обработку платежа в платежный шлюз или банк. Получив ответ о статусе платежа, действующее состояние транзакции фиксируется.

> 6. **Обновление баланса:** После успешного списания средств со счёта, система автоматически обновляет баланс пользователя и отправляет уведомление о выполненном автоплатеже и новой сумме на счёте. 

> Такой подход позволяет пользователям удобно управлять своими расходами и поддерживать баланс, не задумываясь о периодических платежах.

### Задание 3. SQL vs NoSQL

> 3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.
> 3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

> **3.1. Пять преимуществ SQL-систем по отношению к NoSQL:**

> 1. **Структурированные данные:** SQL-системы используют жесткую схему данных, что позволяет организовывать и хранить данные в структурированном виде. Это делает их идеальными для работы с предсказуемыми и однородными данными.

> 2. **Поддержка сложных запросов:** SQL-системы используют мощный язык запросов SQL, который позволяет выполнять сложные операции, такие как соединения (JOIN), агрегации и подзапросы, что позволяет получать полезную информацию из связанных таблиц.

> 3. **Транзакционная целостность (ACID):** SQL-системы гарантируют соблюдение свойств ACID (атомарность, согласованность, изолированность и долговечность), что обеспечивает надежность транзакций и предотвращает потерю данных в случае сбоя.

> 4. **Широкая поддержка и зрелость:** SQL-системы существуют на рынке с 1970-х годов, и многие из них имеют обширную базу пользователей и документации, что облегчает обучение и решение проблем. Существуют также стандартные инструменты для администрирования баз данных.

> 5. **Сложные аналитические операции:** SQL-системы предлагают мощные средства для аналитики и отчетности, что позволяет бизнесу эффективно анализировать данные для принятия информированных решений.

> **3.1.* Преимущества NewSQL систем перед SQL и NoSQL:**

> 1. **Сочетание преимуществ SQL и масштабируемости NoSQL:** NewSQL системы предлагают преимущества традиционных SQL баз данных, такие как поддержка ACID-транзакций, и при этом обеспечивают возможность горизонтального масштабирования, подобно системам NoSQL, что позволяет обрабатывать большие объемы данных и запросов.

> 2. **Высокая производительность:** NewSQL разработки, как правило, используют оптимизации, такие как распределенные системы и параллельная обработка, что позволяет им достигать высокой производительности при больших нагрузках, что делает их конкурентоспособными в современных условиях.

> 3. **Гибкое управление схемой:** Многие NewSQL системы предлагают более гибкие схемы данных, чем традиционные SQL, и позволяют разработчикам адаптироваться к изменениям в структурах данных без разрушения существующих приложений.

> 4. **Поддержка облачных технологий:** NewSQL системы часто созданы с учетом облачной архитектуры, что позволяет легко применять облачные решения и использовать преимущества облачной инфраструктуры, такие как автоматическое резервное копирование и восстановление.

> 5. **Интеграция с современными технологиями:** NewSQL базы данных обеспечивают совместимость с современными технологиями аналитики, машинного обучения и больших данных, позволяя компаниям эффективно использовать данные в своих бизнес-решениях и иновациях.

> В результате, NewSQL представляет собой интересную альтернативу, привнося лучшие черты как из мира SQL, так и из NoSQL, адаптируясь под современные требования к данным и масштабируемости.

### Задание 4. Кластеры


> Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.
> На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

> При выборе типа системы управления базами данных (СУБД) для обработки огромного количества данных на 1000 машинах, важно учитывать несколько ключевых критериев:

> 1. Объем данных и природа запросов: Необходимо оценить, с каким объемом данных будет работать система и какие типы запросов будут исполняться. Если данные структурированы и требуют сложной аналитики, возможно, стоит рассмотреть SQL СУБД. Однако, если необходимо работать с неструктурированными или полуструктурированными данными, логично выбрать NoSQL решения.

> 2. Масштабируемость: С учетом большого количества машин, важно, чтобы СУБД могла легко масштабироваться как вертикально, так и горизонтально. Поэтому стоит обратить внимание на системы, которые поддерживают распределенное хранение данных и автоматическое масштабирование.

> 3. Производительность и отзывчивость: Ускорение обработки запросов — один из основных критериев. Важно учитывать, как система справляется с большими объемами параллельных запросов, и насколько эффективно реализованы механизмы кэширования и индексации.

> 4. Поддержка распределенных вычислений: Система должна обеспечивать эффективную обработку данных на уровне кластеров. Поддержка распределенных транзакций и обработка данных в реальном времени являются ключевыми для эффективной работы на таком большом количестве машин.

> 5. Соответствие требованиям ACID: Если требуется высокая целостность данных и надежность транзакций, это может стать важным фактором в выборе традиционных SQL СУБД, тогда как для менее критичных задач можно рассмотреть NoSQL решения.

> Модель распределенных вычислений:

> На основе вышеуказанных критериев, для обработки больших данных в таком распределенном окружении на 1000 машинах наиболее эффективно подойдут:

> 1. Apache Hadoop: Эта модель обработки данных позволяет эффективно распределять и обрабатывать данные на большом количестве узлов. Она идеально подходит для обработки больших объемов данных и выполнения сложных расчетов. Hadoop использует модель MapReduce, что делает ее высокоэффективной для обработки параллельных вычислений.

> 2. Apache Spark: Это еще одно мощное решение для обработки данных в распределенном окружении. Spark предлагает более высокую производительность по сравнению с Hadoop, поскольку он работает в памяти и использует более простой API. Это отлично подходит для интерактивной обработки данных и в реальном времени.

> 3. Dask: Эта библиотека предоставляет динамические данные и параллельные вычисления непосредственно в Python-коде, что может быть удобно для тех, кто работает с научной и аналитической обработкой данных.

> Подводя итог, выбор типа СУБД и модель распределенных вычислений должны быть основаны на природe данных, требованиях к производительности и надежности, требованиях к масштабируемости и способности системы к обработке параллельных запросов. Это позволит наиболее эффективно использовать 1000 машин для обработки больших объемов данных.



## Кеширование Redis/memcached
### Задание 1. Кеширование


> Приведите примеры проблем, которые может решить кеширование.

> Кеширование — это мощная техника, которая позволяет значительно улучшить производительность и эффективность систем, сокращая время доступа к данным и снижая нагрузку на основные источники данных. Рассмотрим несколько примеров проблем, которые кеширование может решить.

> 1. Повышение скорости доступа к данным
Когда пользователи обращаются к часто запрашиваемой информации, кеширование позволяет возвращать эти данные гораздо быстрее, чем если бы каждый раз приходилось обращаться к основному хранилищу данных. Например, в веб-приложении, где пользователи регулярно запрашивают одни и те же страницы, кеширование результатов запросов (например, HTML-кода) значительно ускоряет время загрузки страниц.

> 2. Снижение нагрузки на базу данных
При большом количестве пользователей, одновременно обращающихся к базе данных для получения одинаковых данных, может возникать значительная нагрузка, что может привести к замедлению ответов или даже сбоям. Кеширование позволяет снизить количество обращений к базе, так как данные могут храниться во временном хранилище и предоставляться оттуда, что разгружает основной источник данных.

> 3. Увеличение пропускной способности
Кеширование может увеличить общее количество запросов, которые система может обработать одновременно. Например, если данные или результаты вычислений кешируются в памяти, выполнение одного и того же запроса для разных пользователей требует минимального времени на выполнение, что может значительно повысить общую пропускную способность приложения.

> 4. Улучшение пользовательского опыта
Благодаря кешированию пользователи могут получать данные и услуги быстрее. Время отклика приложения — критически важный фактор для удовлетворенности пользователей. Быстрее загружающиеся страницы или приложения ведут к улучшению общего опыта и, как следствие, увеличению вероятности возвращения пользователей.

> 5. Оптимизация сетевого трафика
В распределенных систем, особенно в облачных и микросервисных архитектурах, кеширование может сократить объем сетевого трафика. Например, с помощью CDN (Content Delivery Network) можно кешировать статические ресурсы (изображения, видео, скрипты) ближе к пользователям, что уменьшает задержки и скорость загрузки.

> 6. Уменьшение затрат на обработку больших данных
При работе с большими данными, кеширование результатов промежуточных вычислений может значительно ускорить анализ и обработку, так как не придется повторно выполнять одни и те же громоздкие запросы.

> 7. Снижение времени простоя
Кеширование может играть важную роль в ситуациях, когда основное хранилище данных временно недоступно. Например, если база данных временно выходит из строя, кешированные данные могут продолжать предоставляться пользователям, минимизируя время простоя и снижая влияние на бизнес-процессы.

> Кеширование — это эффективный способ улучшения производительности и надежности систем. Однако важно правильно управлять кешем, чтобы избежать проблем с устаревшими данными и обеспечить их актуальность.


### Задание 2. Memcached

> Установите и запустите memcached.

* Cкриншот systemctl status memcached

![alt text](./img/memcached.png)

### Задание 3. Удаление по TTL в Memcached

> Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5.

![alt text](./img/TTL.png)



### Задание 4. Запись данных в Redis

> Запишите в Redis несколько ключей с любыми именами и значениями.

![alt text](./img/redis.png)


