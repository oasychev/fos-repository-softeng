# РЕСУРСЫ ДЛЯ ПРЕПОДАВАТЕЛЯ

## по дисциплине «Разработка прикладных программных решений для систем искусственного интеллекта»

---

Настоящий документ содержит структурированный перечень ресурсов, которые могут быть полезны преподавателю при проведении курсового проекта. Ресурсы сгруппированы по тематическим разделам и сопровождаются краткими рекомендациями по использованию.

---

### 1. ОТКРЫТЫЕ ДАТАСЕТЫ ДЛЯ КУРСОВЫХ ПРОЕКТОВ

#### 1.1. Рекомендуемые датасеты (из РПД)

| Название | Источник | Описание | Ссылка |
|----------|----------|----------|--------|
| **Telco Customer Churn** | Kaggle | 7043 записи, 21 признак. Бинарная классификация (отток клиентов). Рекомендуемый датасет для примера. | https://www.kaggle.com/datasets/blastchar/telco-customer-churn |
| **Home Credit Default Risk** | Kaggle | Прогнозирование кредитного риска. Несколько связанных таблиц. | https://www.kaggle.com/c/home-credit-default-risk/data |
| **Pima Indians Diabetes** | UCI | 768 записей. Бинарная классификация (диабет). | https://archive.ics.uci.edu/ml/datasets/Pima+Indians+Diabetes |

#### 1.2. Дополнительные источники данных

| Ресурс | Описание | Ссылка |
|--------|----------|--------|
| **Kaggle Datasets** | Крупнейшая платформа с открытыми датасетами | https://www.kaggle.com/datasets |
| **UCI Machine Learning Repository** | Классический репозиторий датасетов | https://archive.ics.uci.edu/ |
| **OpenML** | Платформа для обмена датасетами и экспериментами | https://www.openml.org/ |

---

### 2. ОФИЦИАЛЬНАЯ ДОКУМЕНТАЦИЯ ПО ТЕХНОЛОГИЯМ

#### 2.1. Язык программирования и инструменты разработки

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **Python 3.10+** | Официальная документация | https://docs.python.org/3/ |
| **Poetry** | Управление зависимостями и упаковка | https://python-poetry.org/docs/ |
| **pre-commit** | Управление git-хуками | https://pre-commit.com/ |
| **Ruff** | Быстрый линтер и форматтер Python (заменяет flake8, black, isort) | https://docs.astral.sh/ruff/ |

#### 2.2. Работа с данными и визуализация

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **NumPy** | Работа с многомерными массивами | https://numpy.org/doc/stable/ |
| **Pandas** | Анализ и обработка данных | https://pandas.pydata.org/docs/ |
| **Matplotlib** | Визуализация данных | https://matplotlib.org/stable/ |
| **Seaborn** | Статистическая визуализация | https://seaborn.pydata.org/ |

#### 2.3. Машинное обучение

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **Scikit-learn** | ML-модели, пайплайны, метрики | https://scikit-learn.org/stable/ |
| **XGBoost** | Градиентный бустинг | https://xgboost.readthedocs.io/ |
| **LightGBM** | Градиентный бустинг (высокая производительность) | https://lightgbm.readthedocs.io/ |
| **CatBoost** | Градиентный бустинг с поддержкой категориальных признаков | https://catboost.ai/en/docs/ |
| **joblib** | Сохранение и загрузка моделей | https://joblib.readthedocs.io/ |

#### 2.4. Веб-разработка

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **FastAPI** | Веб-фреймворк для REST API | https://fastapi.tiangolo.com/ |
| **Pydantic** | Валидация данных и настройки | https://docs.pydantic.dev/ |
| **python-dotenv** | Загрузка переменных окружения из .env | https://github.com/theskumar/python-dotenv |

#### 2.5. Базы данных

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **PostgreSQL** | Реляционная СУБД | https://www.postgresql.org/docs/ |
| **asyncpg** | Асинхронный драйвер для PostgreSQL | https://magicstack.github.io/asyncpg/ |
| **psycopg2** | Синхронный драйвер для PostgreSQL | https://www.psycopg.org/docs/ |

#### 2.6. Тестирование

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **pytest** | Фреймворк для тестирования | https://docs.pytest.org/ |
| **pytest-cov** | Плагин для измерения покрытия кода | https://pytest-cov.readthedocs.io/ |
| **pytest-mock** | Плагин для мокирования | https://pytest-mock.readthedocs.io/ |
| **pytest-asyncio** | Поддержка асинхронных тестов | https://pytest-asyncio.readthedocs.io/ |
| **httpx** | HTTP-клиент для тестирования API | https://www.python-httpx.org/ |

#### 2.7. Контейнеризация и CI/CD

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **Docker** | Контейнеризация приложений | https://docs.docker.com/ |
| **Docker Compose** | Управление многоконтейнерными приложениями | https://docs.docker.com/compose/ |
| **GitHub Actions** | CI/CD пайплайны | https://docs.github.com/en/actions |

#### 2.8. Мониторинг

| Инструмент | Описание | Ссылка |
|------------|----------|--------|
| **prometheus-client** | Метрики для Prometheus | https://github.com/prometheus/client_python |
| **logging** | Встроенный модуль логирования в Python | https://docs.python.org/3/library/logging.html |

---

### 3. ПРИМЕРЫ РЕАЛИЗАЦИЙ И ШАБЛОНЫ

#### 3.1. Образцы проектов студентов (референсы)

Преподаватель может использовать следующие репозитории как примеры выполнения курсового проекта (рекомендуется проверять актуальность перед демонстрацией студентам):

| Проект | Описание | Ссылка |
|--------|----------|--------|
| **Telco Churn ML** | Анализ и прогнозирование оттока клиентов | https://github.com/Busra-Deveci/telco-churn-ml |
| **Home Credit Default Risk** | Анализ кредитного риска | https://github.com/sultanbeishenkulov/home-credit-default-risk |

#### 3.2. Шаблоны конфигураций

**Шаблон `.pre-commit-config.yaml`:**

```yaml
repos:
  - repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.6.0
    hooks:
      - id: trailing-whitespace
      - id: end-of-file-fixer
      - id: check-yaml
      - id: check-added-large-files

  - repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.3.0
    hooks:
      - id: ruff
        args: [--fix, --exit-non-zero-on-fix]
      - id: ruff-format
```


**Шаблон `pyproject.toml` (Poetry):**

```toml
[tool.poetry]
name = "churn-prediction"
version = "0.1.0"
description = "ML service for customer churn prediction"
authors = ["Your Name <email@example.com>"]

[tool.poetry.dependencies]
python = "^3.10"
pandas = "^2.0.0"
numpy = "^1.24.0"
scikit-learn = "^1.3.0"
fastapi = "^0.100.0"
pydantic = "^2.0.0"
asyncpg = "^0.29.0"
python-dotenv = "^1.0.0"
joblib = "^1.3.0"

[tool.poetry.group.dev.dependencies]
pytest = "^7.0.0"
pytest-cov = "^4.0.0"
pytest-mock = "^3.0.0"
pytest-asyncio = "^0.21.0"
httpx = "^0.24.0"
ruff = "^0.1.0"
pre-commit = "^3.0.0"

[build-system]
requires = ["poetry-core"]
build-backend = "poetry.core.masonry.api"
```

**Шаблон `.env.example`:**

```env
# Database
POSTGRES_HOST=localhost
POSTGRES_PORT=5432
POSTGRES_DB=churn_db
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres

# Application
APP_ENV=development
LOG_LEVEL=INFO
MODEL_PATH=./models/best_model.joblib
```

#### 3.3. Структура репозитория (рекомендуемая)

```
project/
├── .github/
│   └── workflows/
│       └── ci.yml                # GitHub Actions
├── app/
│   ├── __init__.py
│   ├── main.py                   # FastAPI приложение
│   ├── models.py                 # Pydantic схемы
│   ├── database.py               # Подключение к БД
│   ├── routers/                  # Эндпоинты
│   │   ├── __init__.py
│   │   ├── predict.py
│   │   ├── health.py
│   │   └── metrics.py
│   └── ml/
│       ├── __init__.py
│       ├── pipeline.py           # Пайплайн предобработки
│       └── model.py              # Загрузка и использование модели
├── data/
│   └── raw/                      # Исходные CSV
├── notebooks/
│   └── eda.ipynb                 # Jupyter Notebook с EDA
├── scripts/
│   ├── etl.py                    # ETL-скрипт
│   └── train.py                  # Обучение модели
├── sql/
│   └── create_tables.sql         # SQL-скрипты
├── tests/
│   ├── __init__.py
│   ├── test_etl.py
│   ├── test_models.py
│   └── test_api.py
├── models/                       # Сохранённые модели (игнорируются Git)
├── docker-compose.yml
├── Dockerfile
├── .env.example
├── .pre-commit-config.yaml
├── pyproject.toml
├── poetry.lock
└── README.md
```

---

### 4. ЧЕК-ЛИСТЫ ДЛЯ ПРОВЕРКИ ЭТАПОВ

#### 4.1. Чек-лист для Этапа 1 (EDA и проектирование БД)

- [ ] Датасет загружен и изучен (df.info(), df.describe())
- [ ] Обработаны пропуски (обоснованный выбор стратегии)
- [ ] Удалены дубликаты
- [ ] Оптимизированы типы данных
- [ ] Категориальные признаки закодированы
- [ ] Числовые признаки масштабированы
- [ ] Построены гистограммы для числовых признаков
- [ ] Построены столбчатые диаграммы для категориальных признаков
- [ ] Построена корреляционная матрица (тепловая карта)
- [ ] Проверен баланс классов
- [ ] Сформулированы и проверены ≥3 гипотезы
- [ ] Выделены сущности, определены PK и FK
- [ ] ER-диаграмма соответствует 3NF
- [ ] SQL-скрипты создают таблицы корректно
- [ ] Настроен Poetry
- [ ] Настроен pre-commit
- [ ] Есть type hints и docstrings
- [ ] Есть README.md
- [ ] Создан тег v1.0

#### 4.2. Чек-лист для Этапа 2 (ML-модель и ETL)

- [ ] Создана БД PostgreSQL
- [ ] Реализован ETL-скрипт загрузки из CSV
- [ ] Использована пакетная вставка (COPY)
- [ ] Написаны SQL-запросы с GROUP BY, JOIN, оконными функциями
- [ ] Обработка ошибок при загрузке
- [ ] Обучены ≥3 модели
- [ ] Проведён подбор гиперпараметров (GridSearchCV/RandomizedSearchCV)
- [ ] Сравнение моделей по метрикам
- [ ] Выбрана лучшая модель
- [ ] Построен пайплайн предобработки (sklearn.pipeline.Pipeline)
- [ ] Модель и пайплайн сохранены (joblib)
- [ ] Настроено логирование
- [ ] Написаны тесты (pytest) с покрытием ≥80%
- [ ] Добавлена конфигурация через .env
- [ ] Создан тег v2.0

#### 4.3. Чек-лист для Этапа 3 (REST API)

- [ ] Реализован эндпоинт `/health` (GET)
- [ ] Реализован эндпоинт `/predict` (POST) с валидацией
- [ ] Реализован эндпоинт `/metrics` (GET)
- [ ] Реализован эндпоинт `/features` (GET)
- [ ] Реализован эндпоинт `/history` (GET) с пагинацией (опционально)
- [ ] Созданы Pydantic-схемы для валидации
- [ ] Использован asyncpg для подключения к БД
- [ ] Реализован пул соединений
- [ ] Асинхронное сохранение запросов/ответов в БД
- [ ] Настроено логирование запросов и ошибок
- [ ] Реализован глобальный обработчик ошибок
- [ ] Доступна Swagger-документация (/docs)
- [ ] Написаны интеграционные тесты (pytest + httpx)
- [ ] Покрытие кода API ≥85%
- [ ] Создан тег v3.0

#### 4.4. Чек-лист для Этапа 4 (Контейнеризация и CI/CD)

- [ ] Создан Dockerfile (оптимизированный, многослойная сборка)
- [ ] Создан docker-compose.yml (app, db, опционально pgadmin)
- [ ] Настроены переменные окружения через .env
- [ ] Настроены тома (volumes) для БД
- [ ] Есть скрипт ожидания БД (wait-for-it)
- [ ] В репозитории есть теги всех этапов (v1.0–v4.0)
- [ ] README.md содержит инструкции по установке, запуску, тестированию
- [ ] Настроен GitHub Actions (линтинг, тесты, сборка образа)
- [ ] Настроено логирование в JSON-формате
- [ ] Добавлен эндпоинт `/metrics` с Prometheus-метриками
- [ ] Подготовлен итоговый отчёт в PDF
- [ ] Создан тег v4.0

---

### 5. РЕКОМЕНДУЕМАЯ ЛИТЕРАТУРА (ДЛЯ ПРЕПОДАВАТЕЛЯ)

#### 5.1. Основная литература

| Автор | Название | Издательство, год |
|-------|----------|-------------------|
| Лутц М. | Изучаем Python. — 5-е изд. | СПб.: Диалектика, 2021 |
| Жерон О. | Прикладное машинное обучение с помощью Scikit-Learn и TensorFlow. — 2-е изд. | М.: ДМК Пресс, 2023 |
| Маккини У. | Python и анализ данных. — 3-е изд. | М.: ДМК Пресс, 2022 |
| Рашка С., Мирджалили В. | Машинное обучение с PyTorch и Scikit-Learn | М.: ДМК Пресс, 2023 |
| Lubanovic B. | FastAPI: Modern Python Web Development | O'Reilly Media, 2023 |
| Poulton N. | Docker Deep Dive | 2023 Edition |
| Chacon S., Straub B. | Pro Git. — 2-е изд. | СПб.: Питер, 2016 |
| Okken B. | Python Testing with pytest. — 2nd ed. | Pragmatic Bookshelf, 2022 |

#### 5.2. Дополнительная литература

| Автор | Название | Издательство, год |
|-------|----------|-------------------|
| Molnar C. | Interpretable Machine Learning | 2nd ed., 2022 |
| Voron F. | Building Data Science Applications with FastAPI. — 2nd ed. | Packt, 2023 |
| Laster B. | GitHub Actions Essentials | Packt, 2023 |
| Фиайли К. | SQL. — 3-е изд. | Саратов: Профобразование, 2024 |

---

### 6. ПОЛЕЗНЫЕ ИНСТРУМЕНТЫ ДЛЯ ПРОВЕРКИ

| Инструмент | Назначение | Ссылка |
|------------|------------|--------|
| **pytest-cov** | Проверка покрытия кода тестами | https://pytest-cov.readthedocs.io/ |
| **ruff** | Быстрая проверка стиля кода | https://docs.astral.sh/ruff/ |
| **mypy** | Статическая проверка типов | https://mypy-lang.org/ |
| **Swagger UI** | Визуальная проверка API (/docs) | Встроен в FastAPI |
| **Postman** | Тестирование API вручную | https://www.postman.com/ |
| **DBeaver** | Визуальное управление БД | https://dbeaver.io/ |
| **pgAdmin** | Управление PostgreSQL | https://www.pgadmin.org/ |
| **draw.io** | Создание ER-диаграмм | https://app.diagrams.net/ |

---

### 7. РЕКОМЕНДАЦИИ ПО ИСПОЛЬЗОВАНИЮ РЕСУРСОВ

#### 7.1. На установочных консультациях

Рекомендуется демонстрировать студентам:
- Официальные документации FastAPI, Poetry, pytest — как основные источники для самостоятельного изучения.
- Примеры структуры репозитория и конфигурационных файлов.
- Чек-листы этапов — чтобы студенты могли самостоятельно контролировать выполнение.

#### 7.2. При проверке этапов

- Использовать чек-листы для быстрой и объективной оценки.
- Проверять наличие тегов в репозитории (`git tag -l`).
- Запускать `pytest --cov` для проверки покрытия.
- Проверять работу pre-commit хуков.

#### 7.3. При подготовке к защите

- Рекомендовать студентам использовать Swagger для демонстрации API.
- Проверять, что приложение запускается через Docker Compose.
- Обращать внимание на наличие логов и метрик.
