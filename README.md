# Разработка серверной части приложений PostgreSQL 12. Базовый курс

## Docker-compose script

### Запуск

```bash
docker compose -f "docker-compose.yml" up -d --build
```

### Остановка

```bash
docker compose -f "docker-compose.yml" down
```

### Подключиться к контейнеру postgres

```bash
docker exec -it postgres-dev1-postgres-1 /bin/bash
```

### Запуск psql

[Локальная установка psql](./psql-setup.md)

```bash
# Локально:
psql -h localhost -U postgres

# В контейнере:
psql -U postgres
```

## Практика

### Базовый инструментарий

#### 1. Конфигурация

Установите в postgresql.conf для параметра work_mem значение 8 Мбайт.

Обновите конфигурацию и проверьте, что изменения вступили в силу.

#### 2. Исполнение файлов sql

Запишите в файл ddl.sql команду CREATE TABLE на создание любой таблицы.

Запишите в файл populate.sql команды на вставку строк в эту таблицу.

Войдите в psql, выполните оба скрипта и проверьте, что таблица создалась и в ней появились записи.

#### 3. Просмотр логов

Найдите в журнале сервера строки за сегодняшний день.

[Посмотреть ответы](./src/dev1_01_tools_overview/answers.md)
