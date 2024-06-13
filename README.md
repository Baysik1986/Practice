# Работа с Git в Windows


## Для начала нужно установить пакет Git for Windows,  
включающий в себя командную строку Git Bash.
### Познакомиться с основными флагами:
- ```~
``` **корневая директория**;
- ```..
``` **директория на уровень выше**;
- ```-a
``` **все файлы**.
### Изучить команды навигации по директориям:
- ```$ pwd
``` показывает текущую директорию;
- ```$ cd ~
``` переходит в корневую директорию;
- ```$ cd имя_папки
``` или
- ```$ cd "имя папки" # если в названии папки есть пробелы
```переходит в папку в текущей директории;
- ```$ cd ..
``` переходит на уровень выше;
- ```$ cd имя_папки/имя_папки2/имя_папки3
``` переходит в папку имя_папки3;
- ```$ ls
``` показывает список обычных файлов в текущей директории;
- ```$ ls -a
``` показывает обычные и скрытые файлы, а также особые файлы ".." и ".";
- ```$ ls ~
``` показывает содержимое файлов в корневой директории;
- ```$ ls ..
``` показывает содержимое файлов в директории уровнем выше.
### Узнать команды операций с файлами и папками:
- ```$ touch my_file.txt
``` создает файл my_file.txt в текущей папке;
- ```$ mkdir my_dir
``` создает папку my_dir в текущей папке;
- ```$ mkdir -p dir1/dir-inside/dir-deeper-inside
``` создает сразу 3 папки, находящиеся одна в другой;
- ```$ touch ~/my_file.txt
``` или ```$ ../touch my_file.txt
``` создает файл в корневой или на уровень выше папке соответственно, аналогично с созданием папок;
- ```$ cp index.html src/
``` копирует файл index.html в папку src;
- ```$ cp index.html style.css script.js src/
``` копирует файлы index.html, style.css, script.js в папку src;
- ```$ mv index.html ./src
``` перемещает файл index.html из текущей папки в папку src;
- ```$ mv ../index.html style.css ~/script.js src/
``` перемещает файл index.html из папки уровнем выше, файл style.css из текущей папки, файл script.js из корневой папки в папку src;
- ```$ cat my_file.txt
``` выводит содержание файла my_file.txt;
- ```$ rm my_file.txt
``` удаляет файл my_file.txt;
- ```$ rmdir my_dir
``` удаляет папку my_dir, если эта папка пустая;
- ```$ rm -r my_dir
``` удаляет папку my_dir, со всем её содержимым.
### Познакомиться с функциями командной строки:
- **флаг** ```&&
``` **между командами позволяет выполнять их подряд, а не по очереди**;
- **стрелки "вверх" и "вниз" позволяют выбрать команду из набранных ранее**;
- **клавиша "tab" после введенных первых символов имени запускает автопоиск**.
## Теперь необходимо настроить Git.
### Внести данные в конфигурацию Git:
- ```$ git config --global user.name "User name"
``` имя пишется в латиницей и в кавычках;
- ```$ git config --global user.email username@email.com
``` необходимо вводить свой реальный почтовый ящик.
### Инициализировать репозиторий:
- **Необходимо перейти в папку, которая будет репозитарием**;
- ```$ git init
``` создает репозиторий;
- ```$ git status
``` показывает текущее состояние папки.
### Если нужно "разгитить" папку, ввести следующую команду:
- ```$ rm -rf .git
``` удаляет папку репозитория;
### Добавить файлы в репозиторий:
- ```$ git add my_file.txt
``` добавляет файл my_file.txt;
- ```$ git add --all
``` добавляет все файлы из папки;
- ```$ git add .
``` добавляет всю текущую папку.
### Взаимодействовать с коммитами к файлам:
- ```$ git commit -m 'Мой первый коммит'
``` создает коммит и сохраняет текущую версию файлов в репозитории;
- ```$ git log
``` показывает историю коммитов.
# Ну и наконец работа с GitHub.


- _Пройти регистрацию на сайте_ [GitHub](github.com "ГитХаб");
- _Создать удалённый репозиторий_;
- _Сгенерировать SSH-ключ_:
	1. ```$ ls -la .ssh/
``` проверяет наличие ключа, ввести в корневой папке;
	2. ```$ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```;
	3. ```$ ls -a ~/.ssh
``` проверяет сгенерированные ключи.
- ```$ clip < ~/.ssh/id_rsa.pub
``` скопировать содержимое ключа;
- _На сайте GitHub в настройках профиля найти пункт SSH and GPG keys_;
- _Выбрать New SSH key и вставить скопированный ключ в поле "key" и нажать кнопку "Add SSH key"_;
- ```$ ssh -T git@github.com
``` проверить правильность ключа;
- _Скопировать url с вкладки SSH на сайте GitHub_;
- ```$ git remote add origin git@github.com:%ИМЯ_АККАУНТА%/first-project.git
``` связывает репозитории;
- ```$ git remote -v
``` проверяет связь репозиториев.
- ```$ git push -u origin main
``` или ```$ git push -u origin master
``` отправляет изменения в удаленный репозитарий при первом использовании;
- ```$ git push
``` отправляет изменения в дальнейшем.
# Создать описание проекта:
- ```$ touch README.md
``` создает файл описания проекта.
- _Отправить файл в удаленный репозиторий._

~~Ох и замучался я эту шпаргалку писать~~

