# **Инструкция по работе с Git**

![эмблема Git](git-branch.jpg)

## Предварительная настройка Git

Чтобы 'представиться' программе Git нужно ввести команды:

    git config --global user.name "ваше имя"
    git config --global user.email "ваш эл.адрес" 

## Создание репозитория

Чтобы инициализировать новый репозиторий нужно ввести команду

    git init

## Добавление в индекс

Чтобы добавить изменения в индекс для фиксации в след commitе нужно ввести команду

    git add <имя файла>


## Фиксация изменений

Чтобы зафиксировать изменения, добавленные в индекс нужно ввести команду:

    git commit 

## Фиксация всех изменений

Чтобы зафиксировать все изменения в отслеживаемых файлах нужно ввести команду:

    git commit -a 

Позволяет автоматически индексировать все отслеживаемые файлы перед их фиксацией, позволяя обойтись без команды git add. 
Новые файлы при этом индексироваться не будут!

## Оставление комментария из командной строки

Для того чтобы оставить комментарий в измененной версии файла прямо из командной строки терминала, нужно набрать команду:

    git commit -m "Комментарий"


## Фиксация всех изменений с оставлением комментария

Чтобы зафиксировать все изменения в отслеживаемых файлах и одновременно с этим оставить комментарий, нужно набрать команду:

    git commit -am "Комментарий изменений"

## Исторя версий файла

Для того чтобы посмотреть все версии файла с указанием автора их изменений и даты изменения нужно набрать команду:

    git log

## История версий файла в упрощенном виде

Для того чтобы просмотреть все версии файла в упрощенном виде (без указания автора, изменившего файл, и даты изменения) нужно набрать команду:

    git log --oneline


## История версий файла по всем веткам проекта

Для того чтобы просмотреть все версии файла по всем веткам необходимо набрать команду:

    git log --all


## Просмотр подробных изменений в файле

Для того чтобы просмотреть подробно все вставки в программу (добавленные и удаленные строки), необходимо набрать команду:

    git diff

Команда позволяет показать что именно изменилось в файле.
Команда diff показывает разницу между текущим состоянием файла и тем состоянием которое уже сохранено.

## Просмотр подробных отличий одного файла от другого

Для того чтобы просмотреть подробные отличия между двумя файлами, необходимо набрать команду:

    git diff 'hash1' 'hash2'

где,

hash1 - первые семь символов хэша файла 1;

hash2 - первые семь символов хэша файла 2.

## Переход к нужной версии файла

Для того чтобы перейти к нужной версии файла, нужно набрать команду:

    git checkout 'hash'

## Состояние рабочего каталога

Для того чтобы посмотреть состояние рабочего катлога (какие файлы в каталоге отслеживаются, а какие нет; какие файлы изменены; какие файлы добавлены либо удалены ), нужно ввести команду:

    git status

## Переход к текущей ветви проекта

Для того чтобы перейти в текущую(настоящее время) ветку проекта,необходимо набрать команду:

    git checkout master

## Ветвления

Ветвления в Гит нужны для:
- работы над разными версиями исходного кода;
- ведения работы над одним и тем же проектом или файлом одновременно n-ому числу разработчиков, при это не мешая друг другу;
- тестирования экспериментальных функций (чтобы не повредить основному проекту);
- разных, выходящих одновременно, итоговых версий проекта. 

## Создание новой ветки

Для того чтобы создать новую ветку, нужно ввести команду:

    git branch <new_branch>

где, 
new_branch - название новой ветки. 


## Слияние веток

Для того чтобы произвести слияние двух веток, нужно перейти на ветку, в которую вы хотите "залить" другую ветку и набрать команду:

    git merge <name_branch>

где,

 name_branch - имя ветки, с которой нужно "слиться".


## Удаление ветки

Для того чтобы произвести удаление ветки, нужно перейти на ветку "мастер" и набрать следующую команду:

    git branch -d <name_branch>

    где,

    name_branch - имя удаляемой ветки.


## Переключение между ветками

Для того чтобы произвести переход на нужную ветку, нужно набрать команду:

    git checkout <name_branch>

где, 

name_branch - имя ветки на которую необходимо перейти.


## Конфликты при слиянии веток 

Кофликт слияния веток может возникать при условии когда объединенные ветви изменяют одну и ту же строку файла по-разному или когда одна ветвь изменяете файл, а другая ветвь удаляет его.

>**Разрешение конфликтов**

Конфликты слияния можно разрешить в Visual Studio или с помощью командной строки и любого текстового редактора.

При работе в Visual Studio в случае возникновения конфликта при слиянии веток, программа предложит 4 варианта решения конфликта:

1. __*accept current change*__ - принять текущее изменение. Т.е. тот вариант кода который находится в ветке мастер (в которую вливают  ветку);
2. __*accept incoming change*__ - принять входящие изменения.Т.е. тот вариант кода, который находится в ветке, которую вливают в основную ветку.
3. __*accept both change*__ - принять оба варианта.
4. __*compare change*__ - сравнить изменения.

Чтобы разрешить конфликт, пользователь должен выбрать один из четырех вариантов.

## Удаленные репозитории

Удаленные репозитории нужны для того чтобы...

## Связь локального и удаленного репозитория

Информация о связи ...
