# Домашнее задание к занятию «Репликация и масштабирование. Часть 2»

---

### Задание 1

Опишите основные преимущества использования масштабирования методами:

- активный master-сервер и пассивный репликационный slave-сервер; 
#### Дешевле, чем "master-сервер и несколько slave-серверов", но не обеспечивет бесперебойную работу системы, так как слейв не сразу берет на себя работу. В случае атаки, можно будет сделать откат системы.

-  master-сервер и несколько slave-серверов;
#### Обеспечивает высокую доступность к инфраструктуре и повышает скорость выборки данных.


- активный сервер со специальным механизмом репликации — distributed replicated block device (DRBD);
#### Обеспечивает высокую доступность к данным на диске.

- SAN-кластер.
#### Основным преимуществом сети SAN является то, что все согласования доступа к файлам осуществляются через Ethernet, в то время как файлы обслуживаются через чрезвычайно высокоскоростной Fibre Channel, что приводит к очень высокой производительности на клиентских рабочих станциях, даже для очень больших файлов.

*Дайте ответ в свободной форме.*

---

### Задание 2


Разработайте план для выполнения горизонтального и вертикального шаринга базы данных. База данных состоит из трёх таблиц: 

- пользователи, 
- книги, 
- магазины (столбцы произвольно). 

Опишите принципы построения системы и их разграничение или разбивку между базами данных.

*Пришлите блоксхему, где и что будет располагаться. Опишите, в каких режимах будут работать сервера.* 

## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.

---
### Задание 3*

Выполните настройку выбранных методов шардинга из задания 2.

*Пришлите конфиг Docker и SQL скрипт с командами для базы данных*.
