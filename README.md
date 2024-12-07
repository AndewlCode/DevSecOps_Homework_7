# DevSecOps_Homework_7

## Часть 1
При помощи Trivy был просканирован образ nginx:latest. Лог сканирования во вложенной папке logs: [trivy_nginx_latest.txt](logs/trivy_nginx_latest.txt)

В результате сканирования обнаружено 2 критические уязвимости.
Критическими уязвимостями являются:
- CVE-2023-6879 в пакете libaom3 [https://avd.aquasec.com/nvd/cve-2023-6879](https://avd.aquasec.com/nvd/cve-2023-6879)
- CVE-2023-45853 в пакете zlib1g [https://avd.aquasec.com/nvd/cve-2023-45853](https://avd.aquasec.com/nvd/cve-2023-45853)

## Часть 2

Для тестирования был запущен Docker - контейнер при помощи команды:

```
docker run nginx
```

В запущенном Docker были выполнены команды:
```
docker exec -it c6bfe82feeb4 sh
```

и 

```
docker exec -it c6bfe82feeb4 curl
```

Команды выполнялись в интерактивном режиме чтобы не прерывать работу контейнера.

Информация о запуске контейнера и команд записана в логе [falco.txt](logs/falco_nginx.txt)