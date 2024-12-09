# COMPILER-WRAPPER

## Обертка онлайн-компилятора

Магистратура ЮФУ Таганрог.

Программа: Цифровые технологии разработки систем умного города.

Данный репозиторий представляет собой лаборатороные работы по предмету "Программное и аппаратное обеспечение ИС и АС"

Сервис представляет собой API, который принимает на вход программный код, возвращает пользователю результат его выполнения, а также шифрует и хранит выполненный пользователями код.

Компиляция кода производится с помощью публичного API https://github.com/Jaagrav/CodeX-API.

Можно сказать что это расширение функционала API выполняющего код.

## Используемые технологии:

- Go
- Chi
- PostgreSql
- Prometheus
- Grafana

## Документация:

// TODO

## Установка

1. Скачать файлы проекта на ПК
2. Для установки зависимостей в терминале директории проекта прописать команду:

```
go mod download
```
3. Переименуйте файл .env_sample в .env и вставьте ссылку на компилятор
4. Для запуска проекта прописать:

```
go run ./.../compiler-wrapper
```

## Использование

#### После запуска, сервис располагается по адресам:

API: http://127.0.0.1:8082/ или http://localhost:8082/

## Как читать код

### Проект разделен на несколько частей:

    .
    ├── cmd                     # Папка с main
    ├── config                  # Папка с конфигом
    ├── internal                # Папка с основным функционалом
    │   ├── config              # Обработка конфига
    │   ├── http-server         # Функционал
    │   │   ├── handlers        # Обработчики
    │   │   ├── middleware      # Промежутчное ПО
    │   ├── lib                 # Помощники
    │   │   ├── api             # Помощники API
    │   │   └── logger          # Расширения для логгера
    └── ...