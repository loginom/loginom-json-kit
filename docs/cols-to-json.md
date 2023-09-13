# Столбцы в JSON

[Назад к списку компонентов](../README.md)

## Назначение

Компонент преобразовывает столбцы таблицы в массив формата JSON. Результат обработки по каждому столбцу записывается в отдельную строку.

## Входные порты

| Название                | Тип        |
|:------------------------|:-----------|
| Входной источник данных | Таблица    |
| Переменные              | Переменные |

### Структура таблицы "Входной источник данных"

Структура таблицы не определена, в порте включена автосинхронизация.

### Переменные в порте "Переменные"

| № | Метка         | Тип                                 | Значение |
|:--|:--------------|:------------------------------------|:---------|
| 1 | Ключ          | ![](./img/logical.svg) Логический   | true     |

**Ключ** принимает значения:

* **true** (по умолчанию) — использует имя столбца как ключ для массива;
* **false** — массив возвращается без ключа.

## Выходные порты

| Название                | Тип         |
|:------------------------|:------------|
| Выходной набор данных   | Таблица    |

### Структура таблицы "Выходной набор данных"

| Метка         | Тип                                       | Описание                                                |
|:--------------|:------------------------------------------|:--------------------------------------------------------|
| Строка JSON   | ![](./img/string.svg) Строковый           | Результат преобразования набора данных в строку JSON    |