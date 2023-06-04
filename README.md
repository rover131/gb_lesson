# Инструкция для работы с Git и справочные материалы по Markdown

## __Что такое Git?__

Git — это распределенная система управления версиями, то есть локальный клон проекта.
Разработчики фиксируют свою работу локально, а затем синхронизируют свою копию репозитория с копией на сервере. 

## __Идентификация пользователя__

При установке Git первым делом следует указать имя пользователя и адрес электронной почты. Это важно, так как данную информацию Git будет включать
в каждую фиксируемую вами версию, и она обязательно включается во все создаваемые вами коммиты (зафиксированные данные):

> git config --global user.name "<ваше имя>"

> git config --global user.email <ваше email>

## __Настройка репозитория Git__

Репозиторий Git или репозиторий — это папка, в которую Git отслеживает изменения. На компьютере может быть любое количество репозиториев, каждое из которых хранится в собственной папке. Каждый репозиторий Git в системе является независимым, поэтому изменения, сохраненные в одном репозитории Git, не влияют на содержимое другого.

## __Создание репозитория Git__

Существует два варианта создания репозитория Git. Его можно создать из кода в папке на компьютере или клонировать из существующего репозитория. 

### __Создание репозитория из существующего кода__

Чтобы создать репозиторий из существующей папки на компьютере: в командной строке перейдите в корневую папку, содержащую код, и выполните следующую команду:

> git init

Затем добавьте все файлы в папку в первую фиксацию с помощью следующих команд:

> git add --all

и 

> git commit -m "<описание внесенных изменений>" 

для фиксации изменений в папке.

### __Создание репозитория из удаленного репозитория__

Чтобы скопировать содержимое существующего репозитория в папку на компьютере: в командной строке перейдите в папку для хранения клонированного репозитория, а затем выполните следующую команду:

> git clone <ссылка на репозиторий с сайта https://github.com/>

### __Проверка состояния файлов__

Основным инструментом определения состояния файлов является команда:

> git status 

### __Просмотр индексированных и неиндексированных изменений__

Если команда **git status** дает недостаточно подробный, с вашей точки зрения,
результат, например если вы хотите не только получить список отредактированных
файлов, но и узнать, что именно изменилось, воспользуйтесь командой:

> git diff 

Данная команда без дополнительных параметров позволяет посмотреть, что было
изменено, но пока не проиндексировано.

### __Слежение за новыми файлами__

Чтобы начать слежение за новым файлом, воспользуйтесь командой: 

> git add

### __Фиксация изменений__

Для фиксации изменений воспользуйтесь командой:

> git commit -m <описание внесенных изменений>

### __Игнорирование файлов__

Бывает так, что некоторый класс файлов вы не хотите ни автоматически добавлять в репозиторий, ни видеть в списке неотслеживаемых. В подобных случаях создается файл **.gitignore** со списком соответствующих паттернов. 

### __Просмотр истории версий__

Для просмотра проделанной работы после сохранения нескольких версий файлов или клонирования уже имеющего содержимое репозитория воспользуйтесь командой:

> git log

или командой:

> git log --graph 

## __Ветвления__

### __Создание и удаление веток__

Команда: 

> git branch <имя ветки>

позволяет создавать ветки, а команда: 

> git branch -d <имя ветки>

их удалять. 

Запущенная без аргументов, она выводит на экран список имеющихся веток.

### __Смена веток__

Переход между ветками осуществляется с помощью команды:

> git checkout <имя ветки>

### __Слияние веток__

Для того, чтобы осуществить слияние веток, достаточно перейти в ветку, которую нужно слить и воспользоваться командой: 

> git merge <имя текущей ветки>

## __Отправка данных__ 

Команда: 

 > git pull 
 
 используется для извлечения и загрузки содержимого из удаленного репозитория и немедленного обновления локального репозитория этим содержимым. Команда **git pull** на самом деле представляет собой комбинацию двух других команд: **git fetch** и **git merge**.

  > git pull request 
 
это предложение изменения кода в чужом репозитории. Вы делаете форк чужого репозитория (который иногда и сам может быть форком) → производите изменения в своём форке → посредством **pull request** предлагаете изменения владельцам репозитория, чей форк вы сделали. 

Команда: 

 > git fetch
 
 используется для извлечения и загрузки содержимого из удаленного репозитория, но при этом не вносит изменения в локальный репозитория.

 Чтобы поделиться содержимым своей ветки с окружающими, ее нужно отправить на удаленный сервер командой:

 > git push <удаленный репозиторий> <имя ветки>

## __Что такое Markdown?__

**Markdown** — это облегченный язык разметки с синтаксисом форматирования обычного текста. Для записи Markdown можно использовать любой текстовый редактор.

## __Блок цитирования__

Блоки цитирования создаются с помощью символа **>**:

> Пример блока цитирования

## __Полужирное и курсивное начертания__

Чтобы задать для текста полужирное начертание, заключите его в двойные звездочки (**):

> Пример **полужирного текста**

Чтобы задать для текста курсивное начертание, заключите его в одинарные звездочки (*):

> Пример *курсивного начертания*

Чтобы задать для текста полужирное и курсивное начертание, заключите его в тройные звездочки (***):

> Пример одновременного ***полужирного и курсивного начертания***

## __Заголовки__

Платформа Docs поддерживает шесть уровней заголовков Markdown:

> #This is a first level heading (H1)<br>
> ##This is a second level heading (H2)<br>
> ...<br>
> ######This is a sixth level heading (H6)

* Между последним символом # и содержимым заголовка должен присутствовать пробел.
* В одном файле Markdown должен быть один и только один заголовок H1.
* Заголовок H1 указывается в файле в первую очередь, сразу после блока метаданных YML.
* Заголовки H2 автоматически отображаются в правом меню навигации опубликованного файла. Заголовки более низкого уровня не отображаются, поэтому для удобства перехода по содержимому рекомендуется использовать заголовки H2.
* Использовать заголовки HTML, такие как < h1 >, не рекомендуется, и в некоторых случаях из-за них могут возникать предупреждения при сборке.

## __Изображения__

Для изображений по умолчанию поддерживаются следующие типы файлов:

* .jpg
* .png

Базовый синтаксис Markdown для внедрения изображения: ![<краткое описание изображения>] (<ссылка на изображение>)

> Пример изображения:<br>![<краткое описание изображения>](https://img.exist.ru/img.jpg?Key=21198&Size=150x100&MethodType=5)
## __Ссылки__

Фраза для ссылки должна быть понятной. Иными словами, это должен быть полноценный текст или название страницы, на которую указывает ссылка.

> Пример ссылки: [<фраза для ссылки>](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md)

## __Списки (нумерованные, маркированные, контрольные)__

### __Нумерованный список__

Чтобы создать нумерованный список, можно использовать все единицы. При публикации числа отображаются в возрастающем порядке в виде последовательного списка. Для повышения удобства чтения исходного кода списки можно вводить с приращением вручную.

> 1. элемент 1
> 1. элемент 2
> 1. элемент 3
> 1. элемент 4
> 1. элемент 5

### __Маркированный список__

Для создания маркированного списка используйте - или *, за которым следует пробел в начале каждой строки:

> * элемент 1
> * элемент 2
> * элемент 3
> - элемент 4
> - элемент 5

## __Таблицы__

Использование вертикальных линий и строк является самым простым способом создания таблиц в Markdown. Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки.

> | Столбец 1 | Столбец 2 | Столбец 3|
> |-----------|-----------|------------|
> |ячейка 1|ячейка 3|ячейка 5|
> |ячейка 2|ячейка 4|ячейка 6|

Можно выровнять столбцы с помощью двоеточий (:):

> | Столбец 1 | Столбец 2 | Столбец 3|
> |:-----------|-----------:|:------------:|
> |1| 2| 3|
> |4| 5| 6|
> |7| 8| 9|
> |10| 11| 12|
