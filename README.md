# SOVA IDE

## Описание

SOVA IDE предназначен для подготовки сценариев и правил формирования ответов, записанных на специализированном языке Dialog Language (DL). 

## Быстрый старт

Для запуска SOVA IDE в стандартном режиме необходимо выполнить следующую последовательность действий:

Выгрузка необходимых исходников:
```bash
git clone github.com/sovaai/sova_ide &&
cd sova_ide &&
./install.sh
```

Сборка докер образов:
```bash
docker-compose build
```

Запуск контейнеров:
```bash
docker-compose up -d
```
После этого необходимо дождаться, когда запустятся все сервисы и будут созданы базы данных.

Интерфейс IDE будет доступен на http://localhost:3000, а тестовый Widget на http://localhost.

Создание бота по умолчанию для работы тестового виджета:
```bash
./scripts/command.sh bot:create --profile test
```
Вместо test нужно указать профиль бота, созданный в IDE.

## Импорт шаблонов в созданный профиль
Для импорта шаблонов из файла в созданный профиль нужно использовать следующую команду:
```bash
./scripts/import_templates.sh test file
```
Где test - имя созданного в IDE профиля, а file - путь к файлу с шаблонами.

## Импорт словарей в созданный профиль
Для импорта словарей из файлов в созданный профиль нужно использовать следующую команду:
```bash
./scripts/import_dicts.sh test dicts
```
Где test - имя созданного в IDE профиля, а dicts - путь к директории со словарями.
