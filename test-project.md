### Разработать SPA:
1. Стек 
- Redux
- React: 16+
- react-router-dom: 4.1.2
- redux-thunk
- webpack
- Прочие, на свой вкус
- Для ускорения процесса предлагается использовать create-react-app

2. API 
- Можно использовать API https://api.github.com/orgs/{:userName}/repos,
где userName например octokit
2.1 Параметры
- per_page=3, количество записей в ответе
- page=N текущая страница

3. Приложение имеет внитри себя 3 роута
3.1 /  - Главная страница на ней оставьте Ваше Имя и кол-во часов, 
которые заняло у вас это тестовое задание. 
3.2 /list - Эта старница на которой находятся:
- input для ввода userName, этот userName будет использоваться в запросе к апи, 
после ввода значения в input и нажатии клавиши Enter происходит запрос к апи 
и результат запроса отображается в списке
- список с карточками (1 карточка == 1 репо) (результат ответа api) , карточки бывают двух типов, на 
карточке типа 1 выводятся 2 любых поля из информации о репозитарии, на карточке
типа 2 выводятся 4 любых поля.
- над списком распологается Toggle (или группа из 2х радиобатонов), 
которыми переключаются, какой тип карточки использовать в данный момент.
- под списком распологается кнопки "показать еще", 
которая подгружает следующий порцию с данными из апи и отображает ее в этом же списке

- при клике по любой карточке на странице /list, урл меняется на /repoDetails/:repoID
и над списком репозитариев открывается модальное окно, в модальной окне, отображается 6 
любых полей из информации о репозитарии и кнопка закрыть

- при клике на кнопку закрыть, модальное окно закрывается, 
урл восстанавливается на /list 

При открытие / закрытии модального окна, список не перерендеривается, 
сохраняя свое состояние. 

В плане html/css все сделать максимально просто.
