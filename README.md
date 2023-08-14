# Virtual_Internship
Sprints 1-3

Проект "Pereval"

Данное приложение создано для Федерации спортивного туризма России, которая ведет базу данных горных перевалов, пополняемую туристами. Это API-решение для мобильного приложения, которое туристы могут использовать для предоставления данных о горных перевалах и отправки их в ФСТР, как только у них появится доступ в Интернет.
Когда туристы достигают горного перевала, они могут сделать фото и использовать мобильное приложение для передачи данных. Как только турист нажимает «Отправить», мобильное приложение вызывает метод submitData, который принимает данные в формате JSON.


Методы:

Метод GET /submitdata/ - возвращает список всех горных перевалов
Метод POST /submitdata/ - отправляет данные о перевале на сервер
Метод GET /submitdata/{id} - для получения одной записи по id. Параметры запроса: id - уникальный идентификатор записи (перевала).
Метод PATCH /submitdata/{id} - для редактирования существующей записи, если она в статусе "new". Параметры запроса: id - уникальный идентификатор записи (перевала). JSON-объект с полями, которые необходимо отредактировать.
Метод GET /submitdata/?user__email=<email> - для получения списка данных обо всех объектах, которые пользователь с почтой отправил на сервер. Параметры запроса: user__email - адрес электронной почты пользователя.


Установка и запуск:

1) Сохранить репозиторий проекта.
2) Установить все зависимости из файла requirements.txt.
3) Выполнить миграции для создания базы данных.
4) Запустить сервер с помощью команды "python manage.py runserver".
5) Приложение станет доступно по адресу "http://localhost:8000".


Документацию API можно просмотреть с помощью Swagger по ссылке "http://localhost:8000/swagger/".
