# Майкл Хартл "Автоматизация тестирования Rails-приложений" (файлы организации среды тестирования)

Custom Guardfile for Hartl book (lesson 3.7.3)

Файлы для книги Хартл "Ruby on Rails" из главы 3.7.3 про Автоматизацию тестирования Rails-приложений.

## Используемые гемы:

- minitest-reporters
- guard
- guard-minitest

## Описание:

- Улучшенные отчёты об успешном/неуспешном прохождении тестов;
- Автоматический запуск тестов, определяющий изменение файлов.

## Файлы:

- Guardfile
- Gemfile
- /test/test_helper.rb
- дополнительная строка для .gitignore в файле add_to_gitignore

## Как настроить и как работать:

**1. Для отображения отчётов КРАСНЫЙ/ЗЕЛЁНЫЙ в цвете, добавим в файл /test/test_helper.rb**

```ruby
require "minitest/reporters"
Minitest::Reporters.use!
```

**2. Инициализируем Guard для автозапуска тестов:**

```bash
bundle exec guard init
```
**3. Вставляем код из предложенного в репозитории файла Guardfile из** https://github.com/krdprog/hartl-ror-custom-guardfile/blob/master/Guardfile

**4. Добавим Spring в файл .gitignore (см. код в файле add_to_gitignore):**

```ruby
/spring/*.pid
```

**5. Запустим Guard:**

```bash
bundle exec guard
```
- и нажать Enter - для старта

- Ctrl + D - для остановки

**6. Если тормозит тестирование:**

```bash
ps aux | grep spring
kill -9 121234 # это номер процесса

# или
spring stop

# или
pkill -9 -f spring
```
## Ссылки по теме:

- https://github.com/guard/guard
- https://www.railstutorial.org/book/static_pages
