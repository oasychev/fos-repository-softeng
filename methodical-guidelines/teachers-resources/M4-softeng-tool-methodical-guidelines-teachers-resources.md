# Ресурсы для преподавателя

## Модуль 4. Инструменты промышленной разработки на Python

### Лабораторные работы (КИМ-4.2)


Настоящий документ содержит структурированный перечень ресурсов, необходимых преподавателю для проведения лабораторных работ по модулю «Инструменты промышленной разработки на Python». Ресурсы сгруппированы по инструментам и темам, снабжены краткими аннотациями и рекомендациями по использованию в учебном процессе.


## 1. Общие ресурсы

### 1.1. Стандарты и методологии

| Ресурс | Описание | Применение |
|--------|----------|------------|
| [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/) | Официальный стандарт оформления кода на Python | Базовый документ для требований к качеству кода во всех вариантах работ |
| [PEP 621 – Storing project metadata in pyproject.toml](https://peps.python.org/pep-0621/) | Стандарт описания метаданных проекта | Используется при работе с Poetry и pyproject.toml |
| [12-Factor App](https://12factor.net/) | Методология построения современных приложений | Контекст для понимания принципов управления конфигурацией (Вариант 3) |

### 1.2. Платформы и сообщества

| Ресурс | Описание | Применение |
|--------|----------|------------|
| [PyPI – Python Package Index](https://pypi.org/) | Официальный репозиторий пакетов Python | Поиск и проверка актуальных версий зависимостей |
| [GitHub](https://github.com/) | Платформа для хостинга репозиториев | Размещение студенческих работ, поиск примеров |
| [Real Python](https://realpython.com/) | Образовательные материалы по Python | Дополнительные туториалы для студентов |

---

## 2. Инструменты и их документация

### 2.1. Poetry – управление зависимостями

**Официальная документация:** https://python-poetry.org/docs/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Основы | [Basic usage](https://python-poetry.org/docs/basic-usage/) | Быстрый старт, создание проекта |
| Управление зависимостями | [Managing dependencies](https://python-poetry.org/docs/managing-dependencies/) | Добавление, обновление, группировка зависимостей |
| Файл pyproject.toml | [The pyproject.toml file](https://python-poetry.org/docs/pyproject/) | Структура и настройка конфигурационного файла |
| Команды CLI | [Commands](https://python-poetry.org/docs/cli/) | Все доступные команды Poetry |
| FAQ | [FAQ](https://python-poetry.org/docs/faq/) | Ответы на частые вопросы |

**Ключевые команды для демонстрации студентам:**
```bash
poetry new <project_name>          # Создание проекта
poetry add <package>               # Добавление зависимости
poetry add --group dev <package>   # Добавление dev-зависимости
poetry install                     # Установка всех зависимостей
poetry run <command>               # Запуск команды в виртуальном окружении
```

**Рекомендация:** Обратить внимание студентов на различие между `project.dependencies` (PEP 621) и `tool.poetry.dependencies` (legacy), а также на механизм dependency groups.

---

### 2.2. Pre-commit – контроль качества кода

**Официальная документация:** https://pre-commit.com/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Установка | [Installation](https://pre-commit.com/#install) | Настройка pre-commit в проекте |
| Конфигурация | [Configuring hooks](https://pre-commit.com/#configuration) | Создание `.pre-commit-config.yaml` |
| Создание хуков | [Creating hooks](https://pre-commit.com/#creating-new-hooks) | Разработка собственных хуков |
| Поддерживаемые хуки | [pre-commit-hooks](https://github.com/pre-commit/pre-commit-hooks) | Репозиторий стандартных хуков |

**Пример конфигурации для лабораторных работ:**
```yaml
repos:
  - repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.5.0
    hooks:
      - id: trailing-whitespace
      - id: end-of-file-fixer
  - repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.3.0
    hooks:
      - id: ruff
        args: [--fix]
```

**Рекомендация:** После настройки продемонстрировать выполнение `pre-commit install` и `pre-commit run --all-files`. Обратить внимание, что хуки из `ruff-pre-commit` используют конфигурацию из `pyproject.toml`.

---

### 2.3. Pytest – тестирование

**Официальная документация:** https://docs.pytest.org/en/stable/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Введение | [Getting Started](https://docs.pytest.org/en/stable/getting-started.html) | Быстрый старт с pytest |
| Написание тестов | [Writing tests](https://docs.pytest.org/en/stable/how-to/writing_hook_functions.html) | Синтаксис, assertions |
| Фикстуры | [Fixtures](https://docs.pytest.org/en/stable/how-to/fixtures.html) | Механизм фикстур для подготовки тестов |
| Параметризация | [Parametrizing tests](https://docs.pytest.org/en/stable/how-to/parametrize.html) | Тестирование с разными наборами данных |
| How-to guides | [How-to guides](https://docs.pytest.org/en/stable/how-to/index.html) | Практические руководства |

**Ключевые возможности для демонстрации:**
- Автоматическое обнаружение тестов (файлы `test_*.py`, функции `test_*`)
- Использование стандартного `assert`
- Фикстуры для подготовки тестового окружения
- Параметризация для сокращения дублирования кода

---

### 2.4. Pytest-cov – покрытие кода

**Официальная документация:** https://pytest-cov.readthedocs.io/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Обзор | [Overview](https://pytest-cov.readthedocs.io/en/latest/) | Функциональность плагина |
| Конфигурация | [Configuration](https://pytest-cov.readthedocs.io/en/latest/config.html) | Настройка через CLI и файлы |
| Контексты | [Contexts](https://pytest-cov.readthedocs.io/en/latest/contexts.html) | Детализация покрытия по тестам |

**Ключевые команды:**
```bash
poetry run pytest --cov=<package>              # Запуск с покрытием
poetry run pytest --cov=<package> --cov-report=term-missing  # С указанием непокрытых строк
poetry run pytest --cov=<package> --cov-report=html           # HTML-отчёт
```

**Рекомендация:** Объяснить студентам, что плагин автоматически стирает предыдущие данные покрытия при каждом запуске, а для комбинирования результатов нескольких запусков используется `--cov-append`.

---

### 2.5. Pytest-mock – мокирование

**Официальная документация:** https://pytest-mock.readthedocs.io/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Основы | [pytest-mock documentation](https://pytest-mock.readthedocs.io/en/latest/) | Фикстура `mocker` и её возможности |
| Конфигурация | [Configuration](https://pytest-mock.readthedocs.io/en/latest/configuration.html) | Настройка вывода при ошибках |

**Ключевые возможности для демонстрации:**
- Фикстура `mocker` – обёртка над `unittest.mock`
- Автоматический сброс моков после каждого теста
- Улучшенный вывод при ошибках `assert_called_with()`
- Поддержка type hints

**Пример для демонстрации:**
```python
def test_fetch_weather_success(mocker):
    mock_response = mocker.Mock()
    mock_response.json.return_value = {"main": {"temp": 20.5}}
    mock_response.raise_for_status.return_value = None
    mocker.patch('requests.get', return_value=mock_response)
    
    result = fetch_weather("Moscow")
    assert result["temperature"] == 20.5
```

---

### 2.6. Pydantic и Pydantic-settings – валидация и конфигурация

**Официальная документация Pydantic:** https://docs.pydantic.dev/

**Официальная документация Pydantic-settings:** https://docs.pydantic.dev/latest/concepts/pydantic_settings/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Pydantic Settings | [Settings Management](https://docs.pydantic.dev/latest/concepts/pydantic_settings/) | Загрузка конфигурации из окружения |
| Установка | [Installation](https://docs.pydantic.dev/latest/install/) | `pip install pydantic-settings` |
| Префиксы переменных | [Environment variable names](https://docs.pydantic.dev/latest/concepts/pydantic_settings/#environment-variable-names) | Настройка `env_prefix` |

**Ключевые концепции для объяснения:**
- `BaseSettings` автоматически загружает переменные из окружения
- Приоритет источников: инициализация > переменные окружения > `.env` > secrets > defaults
- `env_prefix` позволяет задать префикс для всех переменных

---

### 2.7. Python-dotenv – работа с .env-файлами

**Официальная документация:** https://github.com/theskumar/python-dotenv

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| PyPI | [python-dotenv on PyPI](https://pypi.org/project/python-dotenv/) | Описание и установка |
| GitHub | [GitHub Repository](https://github.com/theskumar/python-dotenv) | Исходный код и документация |

**Ключевые возможности:**
- Чтение пар «ключ-значение» из `.env`-файла
- Поддержка 12-factor principles
- Интерполяция переменных (POSIX variable expansion)

---

### 2.8. BeautifulSoup – парсинг HTML

**Официальная документация:** https://beautiful-soup-4.readthedocs.io/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Быстрый старт | [Quick Start](https://beautiful-soup-4.readthedocs.io/en/latest/#quick-start) | Базовые примеры использования |
| Навигация по дереву | [Navigating the tree](https://beautiful-soup-4.readthedocs.io/en/latest/#navigating-the-tree) | Поиск и перемещение по элементам |
| Поиск | [Searching the tree](https://beautiful-soup-4.readthedocs.io/en/latest/#searching-the-tree) | Методы `find()`, `find_all()`, селекторы |

**Примеры селекторов для Books to Scrape (Вариант 2):**
- `article.product_pod` – контейнер каждой книги
- `h3 > a` – ссылка на книгу (название)
- `p.price_color` – цена
- `p.star-rating` – рейтинг (классы: `One`–`Five`)
- `p.instock.availability` – наличие

**Рекомендация:** Напомнить студентам, что Beautiful Soup требует установки парсера (`lxml` или `html.parser`).

---

### 2.9. Requests – HTTP-запросы

**Официальная документация:** https://docs.python-requests.org/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Быстрый старт | [Quickstart](https://docs.python-requests.org/en/latest/user/quickstart/) | Основы выполнения запросов |
| API | [API Reference](https://docs.python-requests.org/en/latest/api/) | Полная спецификация |

**Ключевые возможности для демонстрации:**
- `requests.get(url, params=..., timeout=...)`
- Обработка статус-кодов (`response.raise_for_status()`)
- Работа с JSON (`response.json()`)

---

### 2.10. Ruff – линтинг и форматирование

**Официальная документация:** https://docs.astral.sh/ruff/

| Раздел | Ссылка | Назначение |
|--------|--------|------------|
| Конфигурация | [Configuration](https://docs.astral.sh/ruff/configuration/) | Настройка Ruff через `pyproject.toml` |
| Linter | [Linter](https://docs.astral.sh/ruff/linter/) | Правила и автоматические исправления |
| Форматтер | [Formatter](https://docs.astral.sh/ruff/formatter/) | Автоматическое форматирование кода |

**Ключевые особенности для объяснения:**
- Замена Flake8, isort, Black, pydocstyle, pyupgrade, autoflake
- Скорость: в 10–100 раз быстрее традиционных линтеров
- Автоматические исправления (удаление неиспользуемых импортов, переформатирование докстрингов и др.)

---

## 3. Внешние API и тестовые ресурсы

### 3.1. OpenWeatherMap API (Вариант 1)

**Официальная документация:** https://openweathermap.org/api

| Ресурс | Ссылка | Назначение |
|--------|--------|------------|
| Current Weather Data | [Current weather data](https://openweathermap.org/current) | Получение текущей погоды по координатам |
| Геокодинг | [Geocoding API](https://openweathermap.org/api/geocoding-api) | Преобразование названия города в координаты |
| Регистрация | [Sign Up](https://home.openweathermap.org/users/sign_up) | Получение бесплатного API-ключа |

**Инструкция для студентов по получению API-ключа:**
1. Зарегистрироваться на [openweathermap.org](https://openweathermap.org/)
2. Подтвердить email
3. Перейти в раздел API Keys в личном кабинете
4. Скопировать API-ключ (APPID)

**Пример API-запроса:**
```
https://api.openweathermap.org/data/2.5/weather?q=Moscow&appid={API_KEY}&units=metric
```


**Рекомендация:** Бесплатный тариф OpenWeatherMap позволяет до 60 запросов в минуту, этого достаточно для учебных целей. Рекомендуется создать один общий ключ для группы или дать студентам инструкцию по самостоятельной регистрации.

---

### 3.2. Books to Scrape (Вариант 2)

**Сайт:** https://books.toscrape.com/

| Ресурс | Описание |
|--------|----------|
| Главная страница | Каталог книг с пагинацией (до 50 страниц) |
| Структура | Каждая книга представлена в элементе `article.product_pod` |

**Рекомендация:** Это тестовый сайт, созданный специально для обучения веб-скрейпингу. Он не требует авторизации и не блокирует запросы при разумной частоте.

---

### 3.3. Альтернативные API (Вариант 3)

| Ресурс | Ссылка | Назначение |
|--------|--------|------------|
| DummyJSON | https://dummyjson.com/ | Тестовое REST API для примеров |
| Open-Meteo | https://open-meteo.com/ | Бесплатный погодный API |

---

## 4. Примеры проектов и шаблоны

### 4.1. Шаблоны конфигураций

**Pre-commit конфигурация:**
- [trailofbits/skills – pre-commit-config.yaml](https://github.com/trailofbits/skills/blob/main/plugins/modern-python/skills/modern-python/templates/pre-commit-config.yaml)
- [Пример с Ruff и mypy](https://github.com/Polycentric-Labs/evidentia/blob/main/.pre-commit-config.yaml)

**pyproject.toml с настройками Ruff:**
```toml
[tool.ruff]
line-length = 88
target-version = "py310"

[tool.ruff.lint]
select = ["E", "F", "W", "I", "N", "D"]
ignore = ["D100", "D104"]
```

### 4.2. Примеры студенческих проектов

| Ресурс | Описание |
|--------|----------|
| [friemari/mipt_python_hw3](https://github.com/friemari/mipt_python_hw3) | Пример парсера Books to Scrape |
| [Oreandr83/books_scraper](https://github.com/Oreandr83/books_scraper) | Парсер с тестами |

---

## 5. Учебные материалы

### 5.1. Рекомендуемая литература

| Издание | Описание |
|---------|----------|
| Okken, B. (2022). *Python Testing with pytest* (2nd ed.). Pragmatic Bookshelf. | Исчерпывающее руководство по pytest |
| Jaworski, M., & Ziadé, T. (2021). *Expert Python Programming* (4th ed.). Packt. | Современные практики разработки на Python |
| Asif, M. (2021). *Python for Geeks*. Packt. | Production-ready разработка на Python |

### 5.2. Онлайн-курсы и туториалы

| Ресурс | Ссылка | Назначение |
|--------|--------|------------|
| Real Python – pytest | [pytest tutorials](https://realpython.com/tutorials/pytest/) | Практические руководства по pytest |
| Real Python – pre-commit | [pre-commit tutorials](https://realpython.com/python-pre-commit/) | Настройка pre-commit |

### 5.3. Справочные материалы по type hints

| Ресурс | Ссылка | Назначение |
|--------|--------|------------|
| Python typing documentation | [typing — Support for type hints](https://docs.python.org/3/library/typing.html) | Официальная документация |
| mypy cheatsheet | [mypy cheatsheet](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html) | Быстрый справочник по аннотациям |

---

## 6. Диагностика типичных проблем

### 6.1. Poetry

| Проблема | Решение |
|----------|---------|
| Конфликт версий зависимостей | Использовать `poetry show --tree` для визуализации дерева зависимостей |
| Медленное разрешение зависимостей | Использовать `poetry lock --no-update` для повторного использования существующего lock-файла |
| Ошибка при добавлении пакета | Проверить, что пакет существует на PyPI; использовать `poetry add --dry-run` для проверки |

### 6.2. Pre-commit

| Проблема | Решение |
|----------|---------|
| Хуки не запускаются | Проверить выполнение `pre-commit install` в корне репозитория |
| Ошибки при запуске | Проверить синтаксис `.pre-commit-config.yaml`; запустить `pre-commit run --all-files --verbose` |
| Ruff не находит конфигурацию | Убедиться, что настройки Ruff указаны в `pyproject.toml` |

### 6.3. Pytest

| Проблема | Решение |
|----------|---------|
| Тесты не обнаруживаются | Проверить命名ование: файлы должны называться `test_*.py` или `*_test.py` |
| Ошибка импорта модуля | Убедиться, что проект установлен в режиме editable (`pip install -e .` или `poetry install`) |
| Покрытие ниже ожидаемого | Использовать `--cov-report=term-missing` для выявления непокрытых строк |

### 6.4. BeautifulSoup

| Проблема | Решение |
|----------|---------|
| Не найден парсер | Установить `lxml` или `html5lib`: `poetry add lxml` |
| Элементы не найдены | Проверить селекторы с помощью инспектора браузера; использовать `soup.prettify()` для отладки |

### 6.5. OpenWeatherMap API

| Проблема | Решение |
|----------|---------|
| Код 401 (Unauthorized) | Проверить корректность API-ключа |
| Код 404 (Not Found) | Проверить название города; использовать Geocoding API для преобразования |
| Таймаут | Увеличить значение `timeout` в настройках |

---

## 7. Полезные ссылки для быстрого доступа

### 7.1. Основные инструменты

| Инструмент | Документация | Репозиторий |
|------------|--------------|-------------|
| Poetry | [python-poetry.org/docs](https://python-poetry.org/docs/) | [github.com/python-poetry/poetry](https://github.com/python-poetry/poetry) |
| pre-commit | [pre-commit.com](https://pre-commit.com/) | [github.com/pre-commit/pre-commit](https://github.com/pre-commit/pre-commit) |
| pytest | [docs.pytest.org](https://docs.pytest.org/) | [github.com/pytest-dev/pytest](https://github.com/pytest-dev/pytest) |
| pytest-cov | [pytest-cov.readthedocs.io](https://pytest-cov.readthedocs.io/) | [github.com/pytest-dev/pytest-cov](https://github.com/pytest-dev/pytest-cov) |
| pytest-mock | [pytest-mock.readthedocs.io](https://pytest-mock.readthedocs.io/) | [github.com/pytest-dev/pytest-mock](https://github.com/pytest-dev/pytest-mock) |
| Pydantic | [docs.pydantic.dev](https://docs.pydantic.dev/) | [github.com/pydantic/pydantic](https://github.com/pydantic/pydantic) |
| Pydantic-settings | [docs.pydantic.dev/latest/concepts/pydantic_settings](https://docs.pydantic.dev/latest/concepts/pydantic_settings/) | [github.com/pydantic/pydantic-settings](https://github.com/pydantic/pydantic-settings) |
| Ruff | [docs.astral.sh/ruff](https://docs.astral.sh/ruff/) | [github.com/astral-sh/ruff](https://github.com/astral-sh/ruff) |
| BeautifulSoup | [beautiful-soup-4.readthedocs.io](https://beautiful-soup-4.readthedocs.io/) | [git.launchpad.net/beautifulsoup](https://git.launchpad.net/beautifulsoup) |
| Requests | [docs.python-requests.org](https://docs.python-requests.org/) | [github.com/psf/requests](https://github.com/psf/requests) |

### 7.2. Краткая шпаргалка для преподавателя

**Инициализация проекта с Poetry:**
```bash
poetry new project_name
cd project_name
poetry add requests pydantic pydantic-settings python-dotenv
poetry add --group dev pytest pytest-cov pytest-mock pre-commit
```

**Настройка pre-commit (минимальный набор):**
```yaml
repos:
  - repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.5.0
    hooks:
      - id: trailing-whitespace
      - id: end-of-file-fixer
  - repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.3.0
    hooks:
      - id: ruff
        args: [--fix]
```

**Запуск тестов с покрытием:**
```bash
poetry run pytest --cov=<package> --cov-report=term-missing
```

**Ключевые требования к студенческим работам:**
- Type hints для всех функций
- Docstrings в Google-стиле
- Покрытие тестами ≥85%
- Pre-commit хуки настроены и проходят
- README.md с инструкцией по установке и запуску


## 8. Заключительные рекомендации

1. **Актуализация ссылок:** Перед началом семестра рекомендуется проверить актуальность всех ссылок, так как документация и версии инструментов могут обновляться.

2. **Создание репозитория-шаблона:** Для ускорения аудиторной работы рекомендуется создать репозиторий-шаблон с предварительно настроенными файлами (`.pre-commit-config.yaml`, `pyproject.toml` с базовыми зависимостями), чтобы студенты могли клонировать его и сосредоточиться на написании кода.

3. **Демонстрация «живого» кода:** На вводной части рекомендуется не только показывать слайды, но и писать код в реальном времени, чтобы студенты видели процесс от создания проекта до первого запуска.

4. **Подготовка тестовых данных:** Для варианта 3 рекомендуется подготовить примеры JSON и YAML-файлов конфигурации, которые студенты могут использовать для тестирования.

5. **Обратная связь:** После проверки самостоятельных работ полезно провести общий разбор типичных ошибок на занятии или в письменном виде.
