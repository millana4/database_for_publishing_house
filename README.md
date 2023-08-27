# База данных для издательства

## Задача 1

Составлены модели классов SQLAlchemy по схеме:

![](readme/book_publishers_scheme.png)

Легенда: система хранит информацию об издателях (авторах), их книгах и фактах продажи. Книги могут продаваться в разных магазинах, поэтому требуется учитывать не только что за книга была продана, но и в каком магазине это было сделано, а также когда.


## Задача 2

Используя SQLAlchemy, составила запрос выборки магазинов, продающих целевого издателя.

Python-скрипт:

- подключается к БД PostgreSQL;
- импортирует необходимые модели данных;
- принимает имя или идентификатор издателя (publisher), например, через `input()`. Выводит построчно факты покупки книг этого издателя:

```
название книги | название магазина, в котором была куплена эта книга | стоимость покупки | дата покупки
```

Пример (было введено имя автора — `Пушкин`):

```
Капитанская дочка | Буквоед     | 600 | 09-11-2022
Руслан и Людмила  | Буквоед     | 500 | 08-11-2022
Капитанская дочка | Лабиринт    | 580 | 05-11-2022
Евгений Онегин    | Книжный дом | 490 | 02-11-2022
Капитанская дочка | Буквоед     | 600 | 26-10-2022
```

## Задача 3 

БД заполняется тестовыми данными.

Тестовые данные берутся из папки `fixtures`. Пример содержания в JSON-файле.

Решение: читается JSON-файл, создаются соотведствующие экземляры моделей и сохраняются в БД.

