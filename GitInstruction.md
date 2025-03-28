![Git-logotip](Git-logotip.png)
# Работа с Git

## 1. Проверка наличия установленного Git

В терминале выполнить команду `git --version`. Если Git установлен появится сообщение с информацией о версии программы, иначе будет сообщение об ошибке.

## 2. Установка Git
Загружаем последнюю версию программы с [сайта](https://git-scm.com/downloads). Устанавливаем с настройками по умолчанию.

## 3. Настройка Git
После установки необходимо «представиться» системе контроля версий. Это нужно сделать всего один раз, и git запомнит вас. Для этого нужно ввести в терминале 2 команды:
• git config --global user.name «Ваше имя английскими буквами»
• git config --global user.email ваша почта@example.com

## 4. Инициализация репозитория
Команда `git init` - указываем папку, в которой git начнет отслеживать изменения. В папке создается скрытая папка .git

## 5. Запись изменений в репозиторий

Команда `git status` - показывает текущее состояние git, есть ли изменения, которые нужно закоммитить (сохранить).

Команда `git add` - добавляет (подгатавливает) содержимое каталога в индекс для последующего коммита. Данная команда дается после добавления файла + название файла, писать название файла можно не до конца, нажимаем клавишу Tab.

Команда `git commit -m "message"`- сохраняет все внесенные данные с указанием, что сделанно с помощью git add.

## 6. Просмотр историй коммитов
Команда `git log` - это журнал изменений. данная команда необхадима, чтобы увидеть количество сохранений (коммитов).

## 7. Перемещение между сохранениями (коммитами)
Команда `git checkout` - это переключение между версиями, т.е переход от одного коммита к другому. Копируем 4 символа коммита с журнала git log.

Команда `git checkout master` - вернуться к актуальному состоянию и продолжить работу.

Команда `git diff` - показывает разницу между текущим файлом и сохраненным (закоммиченным) файлом.

## 8. Игнорирование файлов
Для того, чтобы исключить из отслеживания в репозитории определённые файлы или папки, необходимо создать файл `.gitignore` и записать в него их названия или шаблоны, соответствующие таким файлам или папкам.

## 9. Создание веток в Git
По умолчанию имя основной ветки в Git `master`.

Создать ветку можно командой:
```bash
git branch имя новой ветки
```
## 10. Слияние веток
Для того, чтобы слить любую ветку с основной, необходимо в основной ветке master либо main применить команду:
```bash
git merge имя ветки
```

## 11. Разрешение конфликтов
При работе в двух ветках одновременно может возникнуть ситуация, когда в одной и другой ветке по-разному изменили блок текста. Если затем слить данные ветки , Git сообщит о конфликте и предложит выбрать какие же изменения записать.

## 12. История коммитов в ввиде дерева

***Git log --graph*** - данная команда позволяет отобразить коммиты в виде дерева.

***Git log --graph --oneline*** - команда для просмотра короткой истори коммитов.

## 13. Удаление веток

***git branch -d имя ветки*** - команда позволяет удалить ветку, которую слили с основной.

***git branch -D имя ветки*** - команда позволяет принудительно удалить ветку.

# Работа с удаленными репозиториями в GitHub

**git clone** - данная команда позволяет копировать внешний репозиторий на локальный репозиторий (свой ПК). Она также пытается слить все ветки на локальном компьютере и в удаленном репозитории.

**git pull** - данная команда позволяет скачать даленный репозиторий и автоматически сделать *merge* с нашей версией.

**git push** - данная команда позволяет отправить свою версию репозитория (локальную) во внешний репозиторий.

~~~bash
При первом её использовании необхадима авторизация на внешнем репозитории.
~~~

## Совместная работа репозитория Git b GitHub

1. Создать аккаунт на GitHub.com 
2. Создать локальный репозиторий
3. "Подружить" локальный и удаленный репозитории (GitHub при создании нового репозитория подскажет, как это сделать)
4. Отправить (push) ваш локальный репозиторий в удаленный на GitHub, при этом возможно вам будет необходимо авторизоваться на удаленном репозитории
5. Произвести изменения "с другого компьютера"
6. Выкачать (pull) актуальное состояние из удаленного репозитория.

7. **pull request** - команда для предложения изменений, запрос на вливание изменений в репозиторий.

## Как сделать pull request?

1. Делаем fork (отвлетвление) репозитория
2. Делаем `git clone` своей версии репозитория
3. Создаем новую ветку и в неё вносим изменения
4. Фиксируем изменения (делаем коммиты)
5. Отправляем свою версию в свой GitHub
6. На сайте GitHub нажимаем кнопку pull request 
