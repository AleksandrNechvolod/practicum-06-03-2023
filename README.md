# Репозиторий для практикума
## Соответствие групп и тем на практикум.

1. Что такое система контроля версий

Система контроля версий - система ,позволяющая записывать изменения в работе, корректировать их, а также создавать свои варианты сохранений, отличные от основных при командной работе, как в локальных репозиториях, так и в удаленных.

2. Для чего нужна система контроля версий

Она нужна для совместной и индивидуальной работы над общим проектом впрограммировании.

3. Установка git на ваш ПК (в зависимости от системы)

Загружаем последнюю версию Git с сайта https://git-scm.com/downloads
Устанавливаем с настройками по умолчанию.

4. Установка VSCode на ваш ПК

Сайт https://code.visualstudio.com/

Кнопка на головной странице "Download for Windows Stable Build", далее- выбрать рарядность своей операционной системы.

5. Что такое репозиторий и инструкция по созданию локальных репозиториев.

Репозиторий-ячейка (папка) хранения данных (файлов и изменений данных) и проектов.

При первом использовании Git необходимо представиться. Для этого нужно в термнале добавить две команды:
```
git config --global user.name` "Ваше имя английскими буквами"
git config --global user.email ваша почта@example.com

```
Далее инициализация локального репозитория:

используем комманду в термнале `git init` для обознаения локального репозитория и создания с ним дальнейших действий.

6. Базовая работа с локальным репозиторием

 ## Запись изменений в репозитории

* а) используем команду `git status` для получения иформации о наличии добавленной (изменненной) информации в депозиторий.
* б) используем команду `git add "Название текущего файла"` для подготовки изменененых и добавленных данных в репозиторий к сохранению.Для быстрого нахождения названия файла используем автозполнение кнопкой ``tab``.git
* в) используем команду `git add .` для подготовки к сохранению ***абсолютно всех файлов***, находящихся в работе в терминале.
* г) используем комманду `git commit -m` для фиксации сохранненной инофрмации в данном файле с указанием того, **что изменили**.
* д) используем комманду `git commit -a ` ,совмещающую в себе ***две команды***:  `git add` и `git commit`для подготовки к сохранению и фиксации сохранения файла в депозитории, **НО НЕ ПУТАТЬ(!)** со следующим пунктом, а именно:
* е) используем комманду `git commit -am`, подготавливающую к сохранению и сохранающую ***абсолютно все (!)*** файлы депозитория.
* ж) используем комманду `git diff` для просмотра добавленных, ***но еще не сохраненных*** данных в текущий файл.

## Просмотр истории сохранений в репозитории
Для просмотра вариантов сохраненных изменений (коммитов) в репозитории применяем комманду `git log`.

**!ВАЖНО!**

Для более краткого просмотра информации о коммитах используем комманду `git log --oneline`.

## Перемещение между сохранениями (коммитами) репозитория

Для перемещения между вариантами сохранений репозитория используем комманду `git checkout`.
Она дает возможность не только выйти на нужный вариант сохранения, но и начать с этого коммита новую ветку в терминале.

## Возврат из найденного сохранения (коммита) в текущее состояние работы в терминале

Для возврата в текущее (предудущее) состояние репозитория в терминале используем универсальную для всех версий Git комманду `git gheckout master`.

7. Что такое ветки и для чего они нужны при работе с системой контроля версий.

Ветки-самостоятельные ответвления от основного проекта, нужны для создания, добавления, корректировки основного проекта.

8. Базовая работа с ветками в git.

## Создание веток в Git

По умолчанию имя основной ветки в Git - **master**.

Создать ветку можно командой:
```
git branch <имя новой ветки>
```
Сразу одновременно создать и переключиться на новую ветку можно командой:
```
git branch -b <Имя новой ветки>
```
Список всех существующих веток можно посмотреть командой:
```
git branch
```
В той ветке, в которой находимся в настоящий момент будет стоять пометка знаком -`*`


## Слияние веток с разрешением конфликтов

Для слияния выбранной ветки с текущей нужно выполнить команду:

```
git merge <название ветки>
```

При слиянии веток с конфликтами можно выбрать несколько вариантов:

+ принять за верную информацию из сливаемой ветки
+ принять за верную информацию из основной ветки
+ принять информацию из обеих веток и далее разобраться уже вручную с отличающейся информацией в слиянии двух веток

9. Что такое удаленный репозиторий и для чего он нужен

Удаленный репозиторий - хранилище данных, находящееся на удаленном ресурсе (сервере), принадлежащее другому пользователю или пользователю, ведущему проект.
Нужен для поддержания, развития и завершения совместной командной работы программистов по определенному проекту (ряду проектов).

10. Базовая работа с удаленными репозиториями GitHub

###  Создать удалённый репозиторий

На странице в созданном аккаунте создаем новый репозиторий кнопкой:
```
new
```
далее, в появившемся окне нажимаем:
```
create repository
```
предварительно выбрав на странице нужные настройки для создаваемого удалённого репозитория.

### Создать локальный репозиторий

создается клонированием (напрямую или _**fork**_ репозитория коллеги у которого мы хотим взять его)

### Связать удалённый репозиторий с локальным

####  Клонирование и добавления нового репозитория на GiHub или открытого к доступу репозитория коллеги:

+ Добавить удалённый репозиторий к проекту в локальном репозитории:
```
git remote add <имя репозитория> <url-адрес репозитория в сети>
```
+ Создать новую ветку в проекте для создания и фиксации сових изменений на локальном репозитории

+ При первой передаче информации с локального на удалённый репозиторий необходимо:

поменять (переименовать) основную ветку локального репозитория командой
```
git branch -M main
```
направить на эту ветку удаленного репозитория командой
```
git push -u origin main
```

+ Для получения и слияния изменений из удалённого репозитория используетя команда:
 ```
 git pull
```

+ Также, можено получить информацию из удалённого репозитория без слияния с изменениями:
```
git fetch
```

+ Для отправки изменений на удаленный репозиторий используется команда:
```
git push
```

11. Как строится и для чего нужна совместная работа в системах контроля версий

Данная совместная работа строится  путем обработки выходящего материала согласно ТЗ каждым участником команды программистов, у каждого в своей ветке и в дальнейшем она сливается в один общий проект, либо системой слияния веток на локальном репозитории, а также системой Pull Request (добавлением для принятия комментариев, доработок и изменений участников команды, основным участником проекта).

12. Инструкция по созданию pull request

#### Клонирование и добавление репозитория коллеги на GiHub, закрытого  к доступу:

1. Делаем `fork` интересующего нас аккаунта.
2. Делаем ` git clone` для нашей версии этого (fork) репозитория.
3. Мы создаем ветку с предлагаемыми изменениями.
4. Производим все изменения только в этой ветке.
5. Отправляем эти изменения на свой аккаунт. Команда `push`.
6. В окне на **GitHub** появляется  возможность отправить `pull request`.

13. Книги и полезные ссылки по изучению git.

https://git-scm.com/doc

14. Альтернативные системы контроля версий.

GitLab
GitBucket
Trac
Gogs
Mercurial
