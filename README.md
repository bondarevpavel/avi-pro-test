# Тестовое задание стажера в юнит AvitoPRO

### Необходимо реализовать сервис на Go для генерации случайных значений.

Сервис реализует JSON API работающее по HTTP. Каждой генерации присваивать уникальный id, по которому можно получить результат генерации методом retrieve.

Реализовать методы
* POST /api/generate/ - генерация случайного значения и его идентификатора
* GET /api/retrieve/ - получение значения по id, которое вернулось в методе generate

Задача может быть решена со следующими усложнениями
* возможность задать входные параметры для метода /api/generate/
  - type - тип возвращаемого случайного значения (строка, число, guid, цифробуквенное, из заданных значений)
  - длина возвращаемого значения
* возможность идемпотентных запросов, например несколько запросов с одним requestId (query-параметр или заголовок) вернут то же самое число
* сервис поставляется как Docker образ, опубликованный в публичном репозитории
* написать Unit тесты
* как поменяется архитектура, если вместе простой задачи (генерация случайного значения) будет сложная (занимает минуты)
