﻿## Задание

Создать веб-приложение TO-DO лист (аналог функционала `Заметки` из [Google Keep](https://keep.google.com/)) и разместить его в интернете.

#### Командная работа
На данном проекте все студенты разделены на группы по три человека. Для каждого из участников команды частично определен перечень заданий, которые он должен выполнить. Остальные задания участники команды могут распределить самостоятельно. Участники команды могут самостоятельно решить, кто будет выполнять задание №1, №2 и №3.

#### Технические требования:
 - Возможность создания неограниченного количества заметок.
 - Заметки могут быть двух типов: 
   - карточка с названием (опционально) и текстом 
   - TO-DO список: название (опционально), перечень задач с чекбоксом для отметки того, что задача была выполнена. Выполненные задачи отображаются в самом низу списка.
 - Все запросы между клиентской и серверной частью производятся с помощью AJAX запросов.
 - Для разработки клиентской части необходимо использовать фреймворк [Bootstrap 4](https://getbootstrap.com/). Супер красивости не требуются, но дизайн должен быть аккуратным и не вызывающим отторжение.
 - HTML код должен быть написан с помощью backend-шаблонизатора [JSX](https://learn-reactjs.ru/basics/introduction-to-jsx). Поэтому дальше в задании под словосочетанием "Backend-шаблон HMTL" мы будем иметь в виду "JSX-HTML шаблон".
 - Верстка должна быть сделана только под мобильные девайсы. Верстка под широкоформатные экраны и адаптив не обязательны.
 - Сервер должен быть подключен к удаленной базе MongoDB.
 - Результат работы должен быть размещен на [Heroku](https://www.heroku.com/).
 
#### Задание для студента №1
 - Frontend:
   - Базовая архитектура приложения.
   - Backend-шаблон HTML страницы вывода всех заметок, с возможностью перехода к конкретной заметке при клике на нее. 
 - Backend:
   - Базовая архитектура приложения, подключение необходимых модулей.
   - Роут GET `/`, который будет возвращать главную HTML страницу со всеми заметками.

#### Задание для студента №2
 - Frontend:
   - Backend-шаблон HTML страницы создания заметки.
   - Отправка POST запроса на сервер с созданием заметки. После ответа сервера пользователь должен быть перенаправлен на главную страницу.
   - Backend-шаблон HTML страницы детального отображения заметки. На этой странице должна быть возможность отредактировать и удалить заметку.
   - Отправка PUT запроса на сервер с отредактированной заметкой. После ответа сервера пользователь должен быть перенаправлен на главную страницу.
   - Отправка DELETE запроса на сервер для удаления заметки. После ответа сервера пользователь должен быть перенаправлен на главную страницу.
 - Backend:
   - Роут GET `/notes`, который будет отдавать HTML страницу с формой создания заметки.
   - Роут GET `/notes/${id}`, который будет отдавать HTML страницу детального отображения заметки.
   - Роут POST `/api/notes` для создания заметки.
   - Роут PUT `/api/notes/${id}` для редактирования заметки.
   - Роут DELETE `/api/notes/${id}` для удаления заметки.
 
#### Задание для студента №3
 - Frontend:
   - Бекенд-шаблон HTML страницы создания списка.
   - Отправка POST запроса на сервер с созданием списка. После ответа сервера пользователь должен быть перенаправлен на главную страницу.
   - Backend-шаблон HTML страницы детального отображения списка. На этой странице должна быть возможность отредактировать и удалить список.
   - Отправка PUT запроса на сервер с отредактированным списком. После ответа сервера пользователь должен быть перенаправлен на главную страницу.
   - Отправка DELETE запроса на сервер для удаления списка. После ответа сервера пользователь должен быть перенаправлен на главную страницу.
 - Backend:
   - Роут GET `/lists`, который будет отдавать HTML страницу с формой создания списка.
   - Роут GET `/lists/${id}`, который будет отдавать HTML страницу детального отображения списка.
   - Роут GET `/api/lists/${id}` отображения заметки со списком.
   - Роут POST `/api/lists` для добавления нового списка задач с учетом того, что количество позиций в списке - не ограничено и заранее не известно.
   - Роут PUT `/api/lists/${id}` для редактирования списка задач.
   - Роут DELETE `/api/lists/${id}` для удаления заметки со списком.

#### Общее задание для команды:
 - Код участников команды должен находиться в одном репозитории.
 - Создать файл [README.MD](https://dan-it.gitlab.io/fe-book/teamwork/readme.html) в корне проекта. Указать в файле коротко информацию о проекте:
   - Список использованных технологий
   - Состав участников проекта
   - Какие задачи выполнял кто из участников
 - Разместить проект в интернете на сервере [Heroku](https://www.heroku.com/) (не забудьте потом добавить ссылку в резюме).
   
#### Необязательные задания продвинутой сложности (могут быть выполнены любым участником команды):
 - К заметке и элементам списка должна быть возможность прикрепить изображение (посмотреть в сторону модуля Sharp.js или аналога).
 - Создать роут и функционал в клиентской части для изменения прикрепленной картинки (замены на другую).
 - Создать роут и функционал в клиентской части для удаления картинки.
 
#### Организация рабочего процесса:
 - При выполнении данного проекта необходимо настроить рабочее окружение на GitHub таким образом, чтобы ветка `master` была защищенной, и в нее напрямую нельзя было делать ни один коммит. О том как это сделать можно почитать [здесь](https://dan-it.gitlab.io/fs-book/new-structure/final-project/setup.html).
 - Каждый раз для внесения изменений в проект необходимо будет создать новую ветку, а потом Pull Request, основанный на изменениях в ней. Детальнее про процесс можно почитать [здесь](https://dan-it.gitlab.io/fs-book/new-structure/final-project/pull_request.html).
 - На данном проекте вы будете учиться выполнять Code review кода, который написали ваши коллеги. Проект должен быть настроен таким образом, что любой Pull Request можно слить в мастер только после того, как его посмотрят и поставят свой Approve оба других участника команды. Как настроить для этого репозиторий описано [здесь](https://dan-it.gitlab.io/fs-book/new-structure/final-project/setup.html). 

#### Полезные ссылки:
 - [Работа в команде на Step проекте](https://dan-it.gitlab.io/fe-book/teamwork/step.html)

#### Удачи!