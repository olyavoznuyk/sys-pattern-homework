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


