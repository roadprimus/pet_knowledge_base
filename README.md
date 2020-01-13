# pet_knowledge_base


Краткое описание приложения

Это приложение для моего обучения созданию приложений python/django и их тестирования. Приложение для хранения домашней базы знаний.
Возможности:
1. Создание заметок;
2. Создание заметок на основе статей из интернета;
3. Поиск новых статей на выбранных ресурсах, получение этих статей, сохранение их в заметки;
4. Поиск по сохранённым статьям, по названию и хэш-тегам;
5. Получение сведений о прогнозе погоды с openweathermap.org (это немного не про базу знаний, но хочу добавить для тренировки работы с периодическими задачами).

Основные объекты:
1. Заметка:
   - CRUD (create, read, update, delete);
   - поиск по наименованию;
   - создание заметки на основе статьи из интернета;
   - поиск новых статей на выбранных ресурсах (для начала только с habr.com);
2. веб-ресурс:
   - CRUD;
3. Хэш-тег:
   - CRUD;
   - поиск по наименованию;
4. Погода:
   - CRUD;
   - Получение информации по REST API.


Планируемая пирамида тестирования

1. Модульные (unittest/pytest) 21:
    - Заметка:
        - 4 CRUD;
        - 2 поиск по наименованию:
          - поиск статей по части наименования;
          - полученные статьи должны быть упоядочены по алфавиту;
        - 1 создание заметки на осное статьи из интернета;
    - веб-ресурс:
        - 4 CRUD;
    - Хэш-тег:
        - 4 CRUD;
        - 2 поиск по наименованию:
          - поиск статей по части наименования;
          - полученные хэш-теги упорядочены по алфавиту.
    - Погода:
        - 4 CRUD.
2. Интеграционные 4:
    - 1 получение новых статей с habr.com;
    - 1 получение данных о погоде с openweathermap.org;
    - 1 проверка доступа пирложения к БД;
    - 1 проверка доступа к файловой системе.     
3. Функциональные (selenium) 1:
    - 1 создение заметки.
