# Инструкция по работе с GIT

Чтобы начать работать с Git нужно его установить, скачав по ссылке: 
 https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git

После установки необходимо «представиться» системе контроля версий. Это нужно сделать всего один раз, и git запомнит вас. Для этого нужно ввести в терминале 2 команды:

**git config --global user.name «Ваше имя англ буквами»**

**git config --global user.email ваша_почта@example.com**

## Основные команды

- **git init** - это сокращение от _initializ_ (т.е. "инициализировать", "включать" или "запускать").

- **git add** - добавляет содержимое рабочего каталога в индекс (staging area) для последующего коммита.

- **git commit** - берёт все данные, добавленные в индекс с помощью _git add_, и сохраняет их слепок во внутренней базе данных.

- **git statut** - показывает состояния файлов в рабочем каталоге и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе.

- **git log** - отображает коммиты.

- **git diff** - используется для вычисления разницы между любыми двумя Git деревьями.

- **git checkout** - копирует файлы со сцены в рабочую директорию.

- **git checkout master** - вернуться в самое актуальное состояние.

- **git --version** - узнать версию git.

* **branch** - позволяет создавать, просматривать, переименовывать и удалять ветки.

* **merge** - cлияние используется в Git, чтобы собрать воедино разветвленную историю.

* **git clone** - git скопирует тот репозиторий, который находится _**GitHub**_  в локальный репозиторий.

* **git remote add origin** - связывает локальный репозиторий с удоленным.

* **git pull** - скачать с удоленног репозитория на локальный все изменения.

* **git push** - отправить свою версию репозитория во
внешний репозиторий. 

* **pull request** - запрос на вливание изменений в репозиторий.

## Подробно о командах

### Git init

Cоздает новый репозиторий Git. С ее помощью можно преобразовать существующий проект без управления версиями в репозиторий Git или инициализировать новый пустой репозиторий.

Создание Git-репозитория: **git init**

![](/img/command_init.PNG)

### Git Add

Это первая команда в цепочке операций, предписывающей Git «сохранить» снимок текущего состояния проекта в истории коммитов:
_**git add <file_name>**_

![](/img/command_add.PNG)

### Git commit

Cделать для проекта снимок текущего состояния изменений:
_**git commit -m "commit message"**_.
Флаг **-m** позволяет указать комментарий
![](/img/command_commit.PNG)

### Git status

Отображает состояние рабочего каталога и раздела проиндексированных файлов. С ее помощью можно проверить индексацию изменений и увидеть файлы, которые не отслеживаются Git. Информация об истории коммитов проекта не отображается при выводе данных о состоянии.

**git status**

![](/img/command_status1.PNG)

### Git log

По умолчанию (без аргументов) **git log** перечисляет коммиты, сделанные в репозитории в обратном к хронологическому порядке — последние коммиты находятся вверху.

![](/img/command_log.PNG)

**got log --graph** - `опция --graph добавляет ASCII-граф, показывающий историю ветвлений и слияний.`
![](/img/command_log_graph.PNG)

### Git diff

Представляет собой многоцелевую команду Git, которая инициирует функцию сравнения источников данных Git — коммитов, веток, файлов и т. д.

![](/img/command_diff.PNG)

### Git checkout

Позволяет перемещаться между ветками, созданными командой git branch . При переключении ветки происходит обновление файлов в рабочем каталоге в соответствии с версией, хранящейся в этой ветке, а Git начинает записывать все новые коммиты в этой ветке.

**git chechout <_несколько первых знаков коммита или название ветки_>** 

**git checout master** - _возврат к самой актуальной версии_

![](/img/command_chekcout.PNG)

### Git --version

С помощью этой команды можно определить версию _**Git**_

![](/img/command_version.PNG)

### Git branch

Это своего рода "менеджер веток". Она умеет перечислять ваши  `git branch`, создавать новые, удалять `git branch <branch_name>` и переименовывать их.

**git branch**
![](/img/command_branch.PNG)

**git branch command_log** - *`создали ветку command_log`*.
![](/img/command_branch_creation.PNG)

**git branch -d command_log** - *`удолили ветку command_log (-d "delete" указывает на удоление)`*.
![](/img/command_branch_delete.PNG)

### Git merge

Команда git merge выполняет слияние отдельных направлений разработки, созданных с помощью команды git branch , в единую ветку.

![](/img/command_merge.png)

Практически все использования имеют вид **git merge  _`<branch>`_** с указанием единственной ветки для слияния.
![](/img/command_merge_1.PNG)

### Git clone

Копировать внешний репозиторий на свой ПК можно командой **git clone**.
Команда **git clone** составная: она не только
загружает все изменения, но и пытается слить 
все ветки на локальном компьютере и в
удаленном репозитории.

![](/img/command_clone.PNG)

### Git push

Отправить свою версию репозитория во
внешний репозиторий поможет команда **git
push**. При первом её использовании нужна
авторизация на внешнем репозитории.

![](/img/command_push.PNG)

### Git pull

Эта команда позволяет скачать все из текущего репозитория и автоматически
сделать _**merge**_ с нашей версией. 

![](/img/command_pull.PNG)

### Git remote add origin

![](/img/command_remote.PNG)

* **git remote add origin https://github.com/AlexCh1975/dz_test.git** - связывает локальный репозиторий с удоленным.
* **git branch -M main** - говорит как буден называться главная ветка.
* **git push -u origin main** - добавляет локальный репозиторий на GitHub.

### Git pull request

* команда для предложения изменений
* запрос на вливание изменений в репозиторий

В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают
команду **pull request**. Предлагать изменения на GitHub нужно в отдельной ветке. Сначала
пользователь копирует репозиторий на свой компьютер, делает **Fork** репозитория, затем
клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет
изменения командой push в свой аккаунт на **GitHub** и даёт команду **pull request**. 

#### Как сделать pull request
* Делаем   (ответвление) репозитория **fork**
![command_fork](/img/command_fork.PNG)
* Делаем **git clone**   версии репозитория СВОЕЙ
![command_clone_pull_request](/img/command_clone_pull_reguest.PNG)
* Создаем новую **ветку** и в НЕЕ вносим свои изменения
![command_branch_pull_request](/img/command_branch_pull_request.PNG)
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой **GitHub**
![command_push_pull_request](/img/command_push_pull_request.PNG)
* На сайте **GitHub** нажимаем кнопку **pull request**