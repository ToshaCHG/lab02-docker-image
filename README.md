# Lab 02: Production Docker Image

Мини-сервис на Flask для лабораторной работы.

## Сборка

docker build --build-arg LAB_LOGIN=toshachg --build-arg LAB_TOKEN=d1b43275320ff0f6763b78aad9abc73b -t toshachg/image-lab:d1b43275 .

## Запуск

docker run -d --rm --read-only -e ROCKET_SIZE=Big -p 8080:8000 toshachg/image-lab:d1b43275

## Проверка

curl http://localhost:8080/health
curl http://localhost:8080/
curl http://localhost:8080/proof
