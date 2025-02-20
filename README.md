# Rubizza Survival Camp: Summer 2019

![](https://s3.eu-central-1.amazonaws.com/rubizza/rubizza-logo.png)


# [Как сдавать задания](#how-to-submit)

Алгоритм примерно следующий:

* Для сдачи всех заданий каждому нужно будет [форкнуть](http://lmgtfy.com/?q=%D1%84%D0%BE%D1%80%D0%BA%D0%BD%D1%83%D1%82%D1%8C) этот репозиторий.
* Каждый курсант ( он же участник курсов ) должен в этом репозитории создать папку со своим личным номером ( например __3522__ ).
* Каждое задание должно выполняться в отдельной [ветке](http://lmgtfy.com/?q=github+fork) и для него необходимо создать отдельную папку, которая будет отражать номер задания. ( например для задания 0 - __3522/0/__ )
* После завершения задания - нужно выслать [pull request](http://lmgtfy.com/?q=pull+request) ( он же далее PR ) в master-ветку этого репозитория. Формат названия PR должен быть __персональный номер__ - __номер задания__ ( например 3522 - 0 ). Обратите внимание что при отправки нужно заполнить все поля в шаблоне.
* PR после отправки всегда будет проверять шальная собака на соответствие человеческим стилям. Если стиль кода ей не понравится - она будет ругаться.
* Только если собака довольна - на вашу задачу будет назначен ментор, который уже будет просматривать код и принимать задание.
* После того как ментор решил что задание выполнено полностью и ему все нравится - он зальет ваше задание в основной репозиторий. Именно этот момент и будет считаться временем сдачи задания.

# Задание 0

Чтобы показать все прелести языка Ruby вам придется пройти через сложный путь к просветлению.
На выходе вы получите незабываемые впечатление и навыки написания кода согласно тому, как все привыкли его видеть!
Запомните, что каждое следующее задание должно строго следовать букве закона и быть на [стиле](https://github.com/rubocop-hq/ruby-style-guide)!

0. Форкаем [репозиторий](https://github.com/rubizza-camp/ruby_koans)
1. Фиксим все коэны. (см. инструкцию к репу ruby_koans)
2. ...
4. Profit!

### Как доказать, что я справился

* Все решения ( вместе с кодом решения ) должны быть залиты в папку, которая отражает номер текущего задания.
* Видео, прикрепленное к PR, обязательно должно показывать, что все koans пройдены.

### Дедлайн
2019-07-09 18:00:00 UTC+3

# Задание 1

Существует масса Ruby gems, которые помогают нам в повседневной жизни создавать продукты.
Но просто существовать мало, интересно насколько они популярны и как их сравнить между собой,
так сказать, подбить статистику.

Помним про оформление - жалеем ревьюверов!

### Общее описание

В рамках задания пишем консольную утилиту, определяющую популярность Ruby gems.
Запуск выполняется следующей командой:

```bash
ruby top_gems.rb
```

Cписок гемов для проверки находится в файле в формате YAML следующего вида:

```yaml
gems:
  - sinatra
  - rspec
  # ...
```

Для каждого гема в этом списке мы находим его Github repo, со страницы этого repo достаем следующие данные: Used by, Watch, Star, Fork, Contributors, Issues.

Популярость гема определяется по совокупности всех этих параметров, алгоритм определения данного фактора оставляем за каждым курсантом.

Вывод программы должен быть следующего вида:

```
rails    | used by xxx | watched by xx |  x stars | xx forks | xx contributors | x issues |
sinatra  | used by xxx | watched by xx |  x stars | xx forks | xx contributors | x issues |
```

### Обязательное задание со звездочкой:

Мы можем передать дополнительные аргументы:

- Параметр `--top`, показывает количество гемов согласно рейтинга:

```bash
ruby top_gems.rb --top=2
```

- Параметр `--name`, выводит все Gems согласно рейтинга в имя которых входит заданное слово:

```bash
ruby top_gems.rb --name=active
```

- Параметр `--file`, который является путем к yml файлу, содержащему список имен гемов:

```bash
ruby top_gems.rb --file=gems.yml
```

### Как доказать, что я справился

* Все решения (вместе с кодом решения) должны быть залиты в папку, которая отражает номер текущего задания.
* Видео, прикрепленное к PR, обязательно должно показывать, что ваша программа работает.

### Дедлайн
2019-07-15 18:00:00 UTC+3
