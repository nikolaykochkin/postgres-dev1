# Установка psql

## Проверка установки

```bash
psql --version
```

## Windows

[Установщик](https://www.postgresql.org/download/windows)

В компонентах выбрать только **Command Line Tools**

## Linux

```bash
sudo apt-get update
sudo apt-get install postgresql-client
```

## MacOS

```bash
brew doctor
brew update
brew install libpq

# Опционально
brew link --force libpq
```