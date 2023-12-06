# 4.8Spark

Задание
На вход доступен следующий фрейм данных:

id

timestamp

1

1562007679

1

1

1

2

2

2

1562007710

1562007720

1562007750

1564682430

1564682450

1564682480

id — уникальный идентификатор пользователя

timestamp — время действия на сайте, совершенное данным пользователем

Для каждого id рассчитайте усредненную длину сессии в рамках суток. Усредненная длина сессии рассчитывается как разница между первым и последним действием, произведенным на сайте.

Подсказка: воспользуйтесь возможностями оконных функций в Spark.

Вам доступны следующие фреймы данных:

Таблица с информацией о среднедневном спросе на каждый товар для каждой локации

product

location

demand

1

1

01

02

100

110

2

2

3

3

01

02

01

02

120

90

70

80

product — уникальный идентификатор продукта

location — уникальный идентификатор локации

demand — значение среднедневного спроса на конкретный товар в конкретной локации в единицах товара



Таблица с информацией о складских запасах на уровне месяца:

product

location

stock

1

1

2

01

02

01

1000

400

300

2

02

250

product — уникальный идентификатор продукта

stock — уровень запасов в единицах товара на уровне месяца



В качестве примера рассмотрим июнь 2023 года. Вам необходимо сформировать витрину данных, в которой для каждой пары товар-локация на уровне каждой технической недели* будет рассчитано прогнозируемое значение количества проданных товаров (с учетом среднедневного спроса) и количество остатков товара на складе. 

Техническая неделя — это календарная неделя или часть календарной недели, которая «укладывается» в один календарный месяц. Например, в августе 2023 года вам доступны следующие технические недели: 

01.08—06.08

07.08—13.08

14.08—20.08

21.08—27.08

28.08—31.08
