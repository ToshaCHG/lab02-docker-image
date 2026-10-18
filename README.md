# Lab 02: Production Docker Image

Мини-сервис на Flask для лабораторной работы.

## Сборка

docker build --build-arg LAB_LOGIN=... --build-arg LAB_TOKEN=... -t login/image-lab:prefix .

## Запуск

docker run -d --rm --read-only -e ROCKET_SIZE=Big -p 8080:8000 login/image-lab:prefix

## Проверка

curl http://localhost:8080/health
curl http://localhost:8080/
curl http://localhost:8080/proof