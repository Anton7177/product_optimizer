# Product_optimizer
Продуктовый оптимизатор - это сервис оптимизации списка продуктов под список рецептов.
#

## Как это работает:
**1. Пользователь копирует url понравившегося рецепта блюда с сайта ["Меню недели"](https://menunedeli.ru/)**
<img src="https://raw.githubusercontent.com/nikolay-py/product_optimizer/main/pictures/1_%D0%9F%D0%BE%D0%BB%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5_url.PNG" alt="Получение url" width="700"/>

**2. Вставляет url в специальное окно нашего сайта. Нажимаем "Получить рецепт"**
<img src="https://raw.githubusercontent.com/nikolay-py/product_optimizer/main/pictures/2_%D0%92%D1%81%D1%82%D0%B0%D0%B2%D0%BA%D0%B0_url.PNG" alt="Вставка_url" width="700"/>

**3. Автоматически поучили ингридиенты, и теперь нажимаем "Получить цены"**
<img src="https://raw.githubusercontent.com/nikolay-py/product_optimizer/main/pictures/3_%D0%A0%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82_%D0%BF%D0%B0%D1%80%D1%81%D0%B8%D0%BD%D0%B3%D0%B0_%D1%80%D0%B5%D1%86%D0%B5%D0%BF%D1%82%D0%B0.PNG" alt="Результат_парсинга_рецепта" width="500"/>

**4. Получили список продуктов к покупке, с указнием цены**
<img src="https://raw.githubusercontent.com/nikolay-py/product_optimizer/main/pictures/4_%D0%A0%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82_%D0%BF%D0%B0%D1%80%D1%81%D0%B8%D0%BD%D0%B3%D0%B0_%D1%82%D0%BE%D0%B2%D0%B0%D1%80%D0%BE%D0%B2.PNG" alt="Результат_парсинга_товаров" width="500"/>


**5. С помощью выпадающего списка имеем возможностью выбрать/уточнить товар.**
<img src="https://raw.githubusercontent.com/nikolay-py/product_optimizer/main/pictures/5_%D0%92%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D1%8C_%D1%83%D1%82%D0%BE%D1%87%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F_%D1%82%D0%BE%D0%B2%D0%B0%D1%80%D0%B0.PNG" alt="Возможность_уточнения_товара" width="700"/>

## Установка

1. Клонируйте репозиторий, установите виртуальное окружение
```
git clone https://github.com/nikolay-py/product_optimizer.git
pip install pipenv
```
2. Перейдите в созданную папку product_optimizer, создайте виртуальное окружение
```
pipenv shell
```
3. Установите зависимости
```
pipenv install
```

4. Создайте файл **.env** и создайте в нем переменные:
```
FLASK_APP=app
FLASK_ENV=development
DB_URL = 'sqlite:///goods.db' # общая база данных будет создана в корне проекта
```
## Первый запуск для создания базы данных
Запустите приложение
```
flask run
```
Дождитесь пока программа выполнит все действия,
после чего нажмите **Ctrl+C**

## Наполнение базы данных
Из корня проекта запустите парсер:
```
python3 run_parsers.py
```
Дождитесь, пока спарсятся данные по товарам.

**Цены на товары парсятся с сайта [ОКЕЙ-доставка](https://www.okeydostavka.ru/s)**


## Запуск программы
```
flask run
```

Приложение будет доступно через браузер по адресу

http://127.0.0.1:5000/
