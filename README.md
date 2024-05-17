# 12_01 Стасенко Григорий Домашнее задание к занятию «Базы данных» 12_01

## Задание 1
Опишите не менее семи таблиц, из которых состоит база данных:

какие данные хранятся в этих таблицах;
какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Приведите решение к следующему виду:

Сотрудники (

-идентификатор, первичный ключ, serial,
-фамилия varchar(50),
-...
-идентификатор структурного подразделения, внешний ключ, integer).

````

Сотрудники (
-идентификатор, первичный ключ, serial,
-фамилия varchar(50),
-внешний ключ, integer)

Оклад (
-первичный ключ, serial
-Оклад, numeric(2)
-внешний ключ, integer)

Должность (
-идентификатор, первичный ключ, serial,
-Должность, varchar(33)
-внешний ключ, integer))

Подразделение (
-идентификатор, первичный ключ, serial,
-Тип подразделения, varchar(11)
-Структурное подразделение, varchar(50)
-внешний ключ, integer)

Дата найма (
-первичный ключ, serial,
-Дата найма
-внешний ключ, integer)

Адреса филиалов (
-первичный ключ, serial
-Адрес филиала, varchar(65)
-внешний ключ, integer)

Проекты(
-первичный ключ, serial,
-Название проекта varchar(50)
-внешний ключ integer)

````

---
## Задание 2*
Перечислите, какие, на ваш взгляд, в этой денормализованной таблице встречаются функциональные зависимости и какие правила вывода нужно применить, чтобы нормализовать данные.

````
Таблица Должность зависит от таблицы Структурное подразделение, а Дата найма от ФИО Сотрудников.
-ФИО сотрудников разбить на разные столбцы
-Идентификатор Оклада перевести в тип money
-Дата найма перевести в формат date 'DMY'
````
