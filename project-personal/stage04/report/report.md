---
## Front matter
title: "Отчёт по 4 этапу индивидуального проекта"
subtitle: "Использование nikto"
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

# Задание

Установить DVWA в гостевую систему к Kali Linux.

# Выполнение лабораторной работы

Клонирую заданный репозиторий по ссылке:

![Клонирую заданный репозиторий по ссылке.](image/1.png){#fig:001 width=70%}

Далее перемещаем необходимые файлы согласно примеру: 

![Перемещение файлов.](image/2.png){#fig:002 width=70%}

И заходим в эту директорию: 

![Заходим в эту директорию.](image/3.png){#fig:003 width=70%}

По ссылке $https://localhost$ ничего нет


![$https://localhost$.](image/4.png){#fig:004 width=70%}

Открываем файл $config.inc.php$ в $config$:

![Содержимое файла $config.inc.php$.](image/5.png){#fig:005 width=70%}

Запускаем $apache2$ и выполняем следующие действия:

![Запуск $apache2$.](image/6.png){#fig:006 width=70%}

Чтобы зайти от имени администратора я сначала устанавливаю пароль $root$, а потом уже захожу от имени администратора:

![Вход от имени администратора.](image/7.png){#fig:007 width=70%}

Затем выполняю команду $mysql$ и ввожу там следующие команды: 

![Выполняю команду $mysql$ и некоторые команды внутри открывшегося MariaDB monitor.](image/8.png){#fig:008 width=70%}

![Выполняю команду $mysql$ и некоторые команды внутри открывшегося MariaDB monitor.](image/10.png){#fig:009 width=70%}

Теперь по адресу $localhost/DVWA/login.php$ создаю базу данных с помощью кнопки на сайте "Create/Change Database". 
И захожу с именем пользователя и паролем по умолчанию:

![Вход с именем пользователя и паролем по умолчанию.](image/11.png){#fig:010 width=70%}

Оказываемся на следующей странице: 

![Страница входа.](image/12.png){#fig:011 width=70%}

Устанавливаем низкий уровень $DVWA Security$ для дальнейшей работы. 

![Установка низкого уровня $DVWA Security$ для дальнейшей работы.](image/13.png){#fig:012 width=70%}

Затем выполняем ряд команд по примеру: 

![Выполнение команд от имени администратора.](image/14.png){#fig:013 width=70%}

![Выполнение команд от имени администратора.](image/15.png){#fig:014 width=70%}

# Выводы

В результате выполнения второго этапа индиивидуального проекта я установила DVWA в гостевую 
систему Kali Linux.

