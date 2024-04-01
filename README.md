# ANPR (Raspberry part)

## Апдейт от 15.11.22

Данный проект представляет собой модуль кода, который отвечает за получение кадров с IP - камер, предварительную обработку этих кадров и отправку их на сервер для дальнейшей обработки.

В качестве вычислителя используется Raspberry Pi 4 Model B (4 GB RAM). [Развернутая инструкция по настройке Raspberry.](./docs/PREPARING.md)

Папка для логов находится по пути ```~Documents/Narnia_v2/logs```


```
Crontab
* * * * * /usr/bin/flock -n ~/Documents/Narnia_v2/lock_cam_hub.lock /usr/bin/python3 ~/Documents/Narnia_v2/cam_hub.py >> ~/Documents/Narnia_v2/logs/crontab.log 2>&1
# * * * * * /usr/bin/flock -n ~/Documents/Narnia_v2/watchdog/lock_watchdog.lock /usr/bin/python3 ~/Documents/watchdog/watchdog.py
```
Скрипт "watchdog.py" не доступен на данный момент.

install turbojpeg

```shell 
sudo apt-get update -y 
sudo apt-get install -y libturbojpeg 
```

