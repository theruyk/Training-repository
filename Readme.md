# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Создание коммитов

### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах: ![Изменения](Modified.png) или их не было:![Без изменений](Nothingtocommit.png)

### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

## Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием. *git log --graph* позволит увидеть иное отображение каммитов на разных ветках. А команда *git log --oneline покажет все сделанные коммиты*

## Ветки в Git

### Создание ветки

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*

## Слияние веток

Для того чтобы дабавить ветку в текущую ветку используется команда *git merge <name branch>*

## Удаление веток
Для удаления ветки ввести команду "git branch -d 'name branch'"

## Игнорирование файлов 
Чтобы *git* игнорировал какой-то файл, нужно создать файл с именем ".gitignore" и добавить туда имя файла который нужно игнорировать. Затем воспользоваться командами "git add" и "git commit" чтобы *git* начал отслеживать ".gitignore" и сохранил изменения в нем.

## Псевдонимы
Команда *git config* позволяет легко создать псевдоним для любой из команд. Например:
git config --global alias.st status
Теперь вместо команды *git status* достаточно будет ввести *git st*

## Основы ветвления и слияния
Последовательность действий будет
следующей:
1. Выполняем некие действия на сайте.
2. Создаем ветку для новой истории, над которой тоже нужно работать.
3. В этой ветке тоже производим некие действия.
А теперь предположим, что нам позвонили и сообщили о важной проблеме, требующей срочного решения. Поступаем следующим образом:
4. Переключаемся в производственную ветку.
5. Создаем ветку для решения проблемы.
6. После тестирования выполняем слияние побочной ветки и отправляем ее
в разработку.
7. Возвращаемся к первоначальной задаче и продолжаем работу