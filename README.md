# Домашнее задание к занятию «Базы данных» Шаяхметов Ринат

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

---
### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

### *Ответ*

<details>

*1. Сотрудники*
   - Идентификатор, первичный ключ, SERIAL,
   - Фамилия, Имя, Отчество, VARCHAR(100),
   - Дата приема на работу DATA,
   - Оклад DECIMAL 10, 2, 
   - должность_id, внешний ключ, INTEGER,
   - подразделение_id, внешний ключ, INTEGER
   - код_структурного_поразделения_id, INTEGER,
   - филиал_id, внешний ключ, INTEGER


*2. Должность*
   - Идентификатор, первичный ключ, SERIAL,
   - Должность, VARCHAR(100)
 
*3. Тип подразделения*
   - Идентификатор, первичный ключ, SERIAL,
   - Тип подразделения (полное название), VARCHAR(100)
 
*4. Код структурного поразделения*
   - Идентификатор, первичный ключ, SERIAL,
   - Полное наименование структурного подразделения, VARCHAR(100)
   - должности_id, INTEGER

*5. Филиалы_адреса*
   - идентификатор, первичный ключ, SERIAL, 
   - область_id, внешний ключ, INTEGER
   - город_id, внешний ключ, INTEGER
   - адрес филиала, VARCHAR(350)

*6. Проект*
   - Идентификатор, первичный ключ, SERIAL,
   - Наазвание проекта, VARCHAR(100)
   - Идентификатор_сотрудника_id, INTEGER

*7. Области* 
   - идентификатор, первичный ключ, SERIAL
   - имя района, VARCHAR(50)

*8. Города*
   - идентификатор, первичный ключ, SERIAL
   - имя города, VARCHAR(50)

</details>

---

<details>

## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.


### Задание 2*

Перечислите, какие, на ваш взгляд, в этой денормализованной таблице встречаются функциональные зависимости и какие правила вывода нужно применить, чтобы нормализовать данные.

</details>
