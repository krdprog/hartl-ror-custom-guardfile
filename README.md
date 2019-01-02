# Майкл Хартл "Автоматизация тестирования Rails-приложений" (файлы организации среды тестирования)

Custom Guardfile for Hartl book (lesson 3.7.3)

Файлы для книги Хартл "Ruby on Rails" из главы 3.7.3 про Автоматизацию тестирования Rails-приложений.

## Используемые гемы:

- minitest-reporters
- mini_backtrace
- guard
- guard-minitest

## Описание:

- Улучшенные отчёты об успешном/неуспешном прохождении тестов;
- Утилита фильтрации трассировки стека;
- Автоматический запуск тестов, определяющий изменение файлов.

## Файлы:

- Guardfile
- Gemfile
- /test/test_helper.rb
- дополнительная строка для .gitignore в файле add_to_gitignore

## Как настроить и как работать:

1. Инициализируем Guard для автозапуска тестов:

```bash
bundle exec guard init
```
2. Вставляем код из предложенного в репозитории файла Guardfile

3. Добавим Spring в файл .gitignore (см. код в файле add_to_gitignore)

4. Запустим Guard

```bash
bundle exec guard
``
и нажать Enter - для старта

Ctrl + D - для остановки

5. Если тормозит тестирование:

```bash
ps aux | grep spring
kill -9 121234 # это номер процесса

# или
spring stop

# или
pkill -9 -f spring
```
