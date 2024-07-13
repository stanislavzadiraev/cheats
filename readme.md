# Разное

## WSL
Подключение тома файловой системы `PATH\DISTRO\ext4.vhdx`:
```console
wsl --import-in-place DISTRO PATH\DISTRO\ext4.vhdx
```
Настройка неупоминаемого пользователя `/etc/wsl.conf`:
```console
[user]
default=NAME
```
///
```console
wsl --status # состоятние
wsl --shutdown # выключение

wsl --list --verbose # перечисление местных
wsl --list --online # перечисление удаленных

wsl --install DISTRO # установка
wsl --unregister DISTRO # удаление

wsl --distribution, -d DISTRO # запуск
wsl --terminate, -t DISTRO # остановка
```
## Git
настройка:
```console
git config --global user.name "NAME"
git config --global user.email "EMAIL"
```
---
## Docker
установка:
```console
sudo snap install docker --classic
```
подготовка:
```
sudo groupadd docker
sudo usermod --append --groups docker $USER
# точно требуется выход пользователя из истемы
# возможно требуется презагрузка системы
```
///
```console
docker system prune
docker container prune
docker volume prune
docker image prune

docker container ls
docker volume ls
docker image ls

docker compose up
docker compose down

docker compose start
docker compose restart
docker compose stop
```
 