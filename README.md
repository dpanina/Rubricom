# Чат-бот "Рубрикатор комментариев"

## Предпосылки и идея
Очень много потребительских знаний находится в комментариях к продукту. 
Часто их очень много и задача по их по выявлению смысла из них - очень трудоёмка.

## Принцип работы
**Пользователь** высылает ссылку на товар боту
**Бот** онлайн парсит данные, делает кластеризацию всех комментариев и направляет пользователю:
 - Облако слов
 - Запрос - какой тональности нужны комментарии
 - Список тем
**Пользователь** вводит выбирает или вводит свое слово
**Бот** присылает 10 самых релевантных комментариев

![image (9)](https://user-images.githubusercontent.com/79212361/119344336-3383d880-bca0-11eb-8aa1-d21f367f21fd.gif)

## Парсинг
Онлайн парсинг с помощью библиотеки Scrapy (html+API)

## Препроцессинг
Удаление стандартных стоп-слов
Кастомный список стоп-слов для каждого товара
Очистка текста от лишних символов
Удаление самых редких и самых частых слов по IDF

## Кластеризация комментариев по темам
Кластеризация алгоритмом Kmeans
В каждом кластере определяется тема по tf-idf
Центроиды у каждого кластера и по расстоянию от него - сортируются комментарии

## Анализ тональности


# Структура репозитория


## Соавторы проекта
https://github.com/OlegZubkov
https://github.com/SvetlanaY

