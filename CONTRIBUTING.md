# CONTRIBUTING

Добро пожаловать в Mathematics. Это руководство объясняет как вы можете добавить
свой вклад в проект.

## Структура проекта

Каждая раздел математики это отдельная книга. Каждая книга хранится в папке с
английском названием раздела. Обращайте внимание на правильную разделения тем по
главам

Заметьте что вы должны использовать следующие единицы в latex.
* *part* для объединение глав;
* *chapter* для глав;
* *section* для тем в главах;
* *subsection* для подтем в главах;

## Процесс

Вы можете рассмотреть раздел Issues если хотите добавить свой вклад. По любым
проблемам или желанием также создайте issue (даже если вы сами хотите что-то
добавить или изменить). Любой pull-request принимается с прикрепленным issue.
Соответствующий branch должен называется с номером issue.

## Замечание по поводу пакетов

Во первых класс должен быть *book* с параметрами '*a4paper, 16pt, oneside*'

Это обязательная часть преамбулы.
~~~latex
\documentclass[a4paper, 16pt, oneside]{book}
\usepackage[utf8]{inputenc}
\usepackage[T2A]{fontenc}
\usepackage[english, russian]{babel}
\usepackage{indentfirst}
\usepackage{cmap}
\usepackage[unicode, hidelinks]{hyperref}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage[indent, blackqed]{nccthm}
\usepackage{graphicx}

\countstyle{section}
\ProofStyleParameters{\bfseries}{Доказательство.}
\newtheorem{Definition}{Определения}[theorem]
\newtheorem{Note}{Замечание}[theorem]
\newtheorem{Theorem}{Теорема}[theorem]
\newtheorem{Lemma}{Лемма}[theorem]

\graphicspath{ {images/} }
~~~

## Labels

Все теоремы, леммы, определение, рисунки и т.д. должен иметь метку вида
"Тип_указанного_объекта:название". Например метка теоремы пифагора:
```latex
\label{theorem:pythagoras_theorem}
```

## Рисунки

Рисунки должны находится соответствующем папке внутри папки images
