# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.
CLI
Руководство
Примечания к выпуску
набор псевдонимов gh
Создайте ярлык для команды gh

Синопсис
Объявите слово как псевдоним команды, который будет расширяться до указанной команды (команд).

В раскрытии могут быть указаны дополнительные аргументы и флаги. Если расширение включает позиционные заполнители, такие как «$ 1», «$ 2» и т. Д., Любые дополнительные аргументы, следующие за вызовом псевдонима, будут вставлены соответствующим образом.

Если указан '--shell', псевдоним будет запущен через интерпретатор оболочки (sh). Это позволяет вам составлять команды с "|" или перенаправить с помощью ">". Обратите внимание, что дополнительные аргументы, следующие за псевдонимом, не будут автоматически переданы в расширенное выражение. Чтобы псевдоним оболочки принимал аргументы, вы должны явно принять их, используя «$ 1», «$ 2» и т. Д. Или «$ @», чтобы принять их все.

Примечание по платформе: в Windows псевдонимы оболочки выполняются через "sh", установленную Git для Windows. Если вы установили git в Windows каким-либо другим способом, псевдонимы оболочки могут вам не подойти.

При определении команды, как в примерах, всегда следует использовать кавычки.

gh alias set <alias> <expansion> [flags]
Примеры
$ gh alias set pv 'pr view'
$ gh pv -w 123
#=> gh pr view -w 123

$ gh alias set bugs 'issue list --label="bugs"'
$ gh bugs

$ gh alias set homework 'issue list --assigned @me'
$ gh homework

$ gh alias set epicsBy 'issue list --author="$1" --label="epic"'
$ gh epicsBy vilmibm
#=> gh issue list --author="vilmibm" --label="epic"

$ gh alias set --shell igrep 'gh issue list --label="$1" | grep $2'
$ gh igrep epic foo
#=> gh issue list --label="epic" | grep "foo"

Опции
  -s, --shell   Declare an alias to be passed through a shell interpreter
Параметры, унаследованные от родительских команд
      --help   Show help for command
Товар
Функции
Безопасность
Предприятие
Истории клиентов
Ценообразование
Ресурсы
Платформа
API разработчика
Партнеры
Атом
Электрон
GitHub Desktop
Поддерживать
Помощь
форум сообщества
Профессиональные услуги
Учебная лаборатория
Положение дел
Связаться с GitHub
Компания
О
Блог
Карьера
Нажмите
Магазин
© 2021 GitHub, Inc.
Условия
Конфиденциальность
