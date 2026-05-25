# Домашнее задание "Система сбора логов Elastic Stack" - `Фомичев Анатолий`

## Ссылка на Д3 - https://github.com/netology-code/mnt-homeworks/blob/MNT-video/10-monitoring-04-elk/README.md

## Ссылка на репозиторий - https://github.com/SLzDevOps/Netology-Monitoring-3

### Скриншоты - https://github.com/SLzDevOps/Netology-Monitoring-3/tree/main/screenshots

# Домашнее задание "ELK Stack"

## Выполненные задачи

### 1. Запущен ELK стек в Docker:
- Elasticsearch (hot и warm ноды)
- Logstash (прием JSON по TCP)
- Kibana
- Filebeat (сбор логов Docker)

### 2. Конфигурация компонентов:
- Logstash настроен на прием JSON сообщений по TCP порту 5000
- Filebeat настроен на отправку логов Docker контейнеров в Logstash

### 3. Результаты работы:
- Все 5 контейнеров успешно запущены и работают
- Данные собираются и индексируются в Elasticsearch
- Kibana отображает логи через созданный index pattern

## Файлы в репозитории:
- `docker-compose.yml` - манифест Docker Compose
- `logstash.conf` - конфигурация Logstash
- `filebeat.yml` - конфигурация Filebeat
- `screenshots/` - скриншоты выполнения задания

## Проверка работы:

### Просмотр логов в Kibana:
1. Открыть http://localhost:5601
2. Перейти в Discover
3. Выбрать data view `docker-logs-*`

### Отправка тестового JSON:
```bash
echo '{"app":"test","message":"Hello ELK"}' | nc -N localhost 5000


![alt text](https://github.com/SLzDevOps/Netology-Monitoring-3/blob/main/screenshots/Screenshot_875.png).
![alt text](https://github.com/SLzDevOps/Netology-Monitoring-3/blob/main/screenshots/Screenshot_876.png).
![alt text](https://github.com/SLzDevOps/Netology-Monitoring-3/blob/main/screenshots/Screenshot_877.png).
![alt text](https://github.com/SLzDevOps/Netology-Monitoring-3/blob/main/screenshots/Screenshot_878.png).
![alt text](https://github.com/SLzDevOps/Netology-Monitoring-3/blob/main/screenshots/Screenshot_879.png).


