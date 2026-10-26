
# Домашнее задание «1.2. Тестирование API, CI» — задача № 3

![Java CI with Gradle](https://github.com/alekseinedelyaev-dev/AQA-Postman-Echo/actions/workflows/gradle.yml/badge.svg)

## Описание

Автоматизированное тестирование API учебного сервиса Postman Echo с использованием REST Assured и JUnit 5.

## Задача

Отправить POST-запрос на `https://postman-echo.com/post` с текстом `some data` и проверить, что сервер возвращает отправленное значение.

## Используемые технологии

- Java 17
- Gradle
- REST Assured
- JUnit 5
- GitHub Actions

## Проверки

1. HTTP-статус ответа — 200.
2. Значение поля `data` в JSON-ответе совпадает с отправленным текстом `some data`.

Для проверки ответа используется JSONPath.

## Запуск тестов

Windows:

```powershell
.\gradlew.bat clean test
```

Linux:

```bash
./gradlew clean test
```

## Непрерывная интеграция

В GitHub Actions настроен автоматический запуск тестов.

В истории сборок представлены:

- Успешная сборка с корректной проверкой.
- Намеренно неуспешная сборка с неправильным ожидаемым значением.
- Успешная сборка после восстановления теста.
