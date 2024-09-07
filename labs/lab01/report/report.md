---
## Front matter
title: "Отчёт по лабораторной работе 1"
subtitle: "Установка и конфигурация операционной системы на виртуальную машину"
author: "Аристова Арина Олеговна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---


# Цель работы

Приобретение практических навыков
установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Установить на виртуальную машину операционную систему Linux Rocky, произвести ее минимальную настройку. 

# Выполнение лабораторной работы


## Создание виртуальной машины

Создаю новую виртуальную машину, задаю ей имя и тип операционной системы — Linux, RedHat:

![Задание имени и типа ос виртуальной машины](image/1.png){#fig:001 width=90%}

Настраиваю размер основной памяти виртуальной машины — 2048 МБ:

![Настройка размера памяти ВМ](image/2.png){#fig:002 width=90%}

Задаю размер виртуального жесткого диска: пока 20 ГБ, в случае необходимости увеличим.

![Задание размера виртуального жесткого диска](image/3.png){#fig:003 width=90%}

А затем мы можем посмотреть всю общую информацию о произведенных настройках:

![Итог создания виртуальной машины](image/4.png){#fig:004 width=90%}

Далее подключаю образ операционной системы, который я заранее скачала с официального сайта Linux Rocky:

![Подключение образа ос](image/5.png){#fig:005 width=90%}


## Настройка виртуальной машины

Запускаю виртуальную машину и выполняю необходимые настройки. Выбираю язык: English.

![Задание имени и типа ос виртуальной машины](image/6.png){#fig:006 width=90%}

Затем я проверяю дату и часовой пояс, настраиваю раскладку клавиатуры, далее в разделе выбора 
программ указываю в качестве базового окружения **Server with GUI**, а в качестве дополнения — 
**Development Tools**.

![Задание окружения](image/7.png){#fig:007 width=90%}

Отключаю KDUMP:

![Отключение KDUMP](image/8.png){#fig:008 width=90%}

Место установки ОС оставляю без изменения. Включаю сетевое соединение и в качестве имени узла указываю
aoaristova.localdomain.

![Настройки сетевого соединения](image/9.png){#fig:009 width=90%}

Задаю пароль root:

![Задание пароля root](image/10.png){#fig:010 width=90%}

Создаю пользователя:

![Создание пользователя](image/11.png){#fig:011 width=90%}

И запускаю установку: 

![Запуск установки](image/12.png){#fig:012 width=90%}

В VirtualBox оптический диск отключился автоматическ.



## Домашнее задание 

Чтобы проанализировать последовательность загрузки системы, выполняю команду $dmesg$, также это можно сделать с помощью $dmesg less$

![Использование команды dmesg](image/13.png){#fig:013 width=90%}

Затем я использую поиск для этого вывода: $dmesg | grep -i "то, что ищем"$:

![Пробую использовать поиск](image/14.png){#fig:014 width=90%}

Получаю информацию о:

1. Версии ядра Linux (Linux version).

![Получаю информацию о версии ядра Linux](image/15.png){#fig:015 width=90%}

2. Частоте процессора (Detected Mhz processor).

![Получаю информацию о частоте процессора установки](image/16.png){#fig:016 width=90%}

3. Модели процессора (CPU0).

![Получаю информацию о модели процессора](image/17.png){#fig:017 width=90%}

4. Объеме доступной оперативной памяти (Memory available).

![Получаю информацию о объеме доступной оперативной памяти](image/18.png){#fig:018 width=90%}

5. Типе обнаруженного гипервизора (Hypervisor detected).

![Получаю информацию о типе обнаруженного гипервизора](image/19.png){#fig:019 width=90%}

6. Типе файловой системы корневого раздела

![Получаю информацию о типе файловой системы корневого раздела](image/20.png){#fig:020 width=90%}

7. Последовательность монтирования файловых систем.

![Получаю информацию о последовательности монтирования файловых систем](image/21.png){#fig:021 width=90%}


# Выводы
По результатам работы мною были закреплены практические навыки установки операционной системы на 
виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов, а также в рамках 
выполнения домашнего задания вспомнила и закрепила на практике использование команды dmesg.



# Список литературы{.unnumbered}

- Описание лабораторной работы 
