## Http Parser

### Задача
Одна из главных частей любого веб сервера это http parser, задача которого, разбирать http заголовки для дальнешей обработки.
В этом задании предлагается реализовать простейший http parser.

### Принцип работы
Для того чтобы не ограничиваться одним языком, взаимодействие с парсером строится посредством [стандартных потоков ввода/вывода](http://ru.wikipedia.org/wiki/Стандартные_потоки).
На вход в `bin/http_parser` подаются заголовки (это делают тесты). В STDOUT вам нужно отправить:

в случае успеха:

    {
      method: (GET|POST|...),
      http_version: (1.0|1.1),
      body: <body>,
      url: <url>,
      <header>: <value> // любой заголовок http
    }

в случае ошибки парсинга: `{error: <reason>}`

### Порядок работы
* Произведите подготовку `make install`
* Напишите код (на любом языке) в файле `bin/http_parser` и убедитесь что проходят тесты `make test`
* Отправьте код на проверку

### Структура директорий
* `bin` - директория исполняемыйх файлов
* `test` - готовые тесты. которые проверяют выполненность задания