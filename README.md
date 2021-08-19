# Домашняя задание

### Обязательная часть

Измененная схема базы данных музыкального сервиса

![db image](db.jpg)

###  Необязательная часть

Спроектировать отношение (или схему из нескольких отношений) "Сотрудник". У каждого сотрудника есть следующие параметры:

Имя
Отдел
Начальник (ссылка на начальника)
Примечание: начальник - тоже сотрудник. Отдел можно хранить строкой, можно идентификатором (не принципиально).

```
CREATE DATABASE test WITH OWNER netology; 

CREATE TABLE department (
id serial primary key,
department varchar(80) not null,
manager varchar(80) not null
);

CREATE TABLE employee (
id serial primary key,
name varchar(80) not null,
department_id integer not null references department(id)
);
```

