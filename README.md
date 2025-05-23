# Telegram Bot: Assistant & Moderator

Этот Telegram-бот предназначен для улучшения опыта в групповых чатах, предоставляя функции поиска информации, развлечения в виде игр и модерации для поддержания порядка.

## Особенности

•   **Поиск информации:**
    •   Поиск в Google: Использует поисковый API для предоставления быстрых результатов поиска прямо в чате.
    •   Поиск в Wikipedia: Предоставляет краткие выдержки из Wikipedia по запросу.
•   **Игры:**
    •   Викторина: Запускает викторину с вопросами и вариантами ответов.
    •   Угадай число: Предлагает пользователям угадать случайное число в заданном диапазоне.
    •   Кости: Бросает виртуальные кости и сравнивает результаты между пользователями.
•   **Модерация чата:**
    •   Приветствие новых участников: Автоматически приветствует новых пользователей в чате.
    •   Удаление сообщений: Позволяет модераторам удалять нежелательные сообщения (требует прав администратора).
    •   Предупреждения: Выдает предупреждения пользователям за нарушение правил чата.
    •   Мут: Временно ограничивает возможность отправки сообщений нарушителям.
•   **Утилиты:**
    •   Генерация случайных чисел: Генерирует случайные числа в заданном диапазоне.
    •   Подбрасывание монетки: Имитирует подбрасывание монетки (орел или решка).
•   **Конфигурация:**
    •   Настройка через переменные окружения: Все ключевые параметры (токен бота, ключи API и т.д.) настраиваются через переменные окружения.
    •   Настраиваемые приветствия и правила: Возможность настройки приветственных сообщений и правил чата через конфигурационные файлы.
•   **Логирование:**
    •   Ведение логов: Записывает действия бота и важные события для отладки и мониторинга.

## Необходимые компоненты

•   **Python 3.7+**
•   **Библиотеки Python:**
    •   `aiogram` (основная библиотека для работы с Telegram Bot API)
    •   `google-api-python-client` (для доступа к Google Custom Search API)
    •   `wikipedia` (для поиска информации в Wikipedia)
    •   `python-dotenv` (для загрузки переменных окружения из файла `.env`)
    •   `logging` (для ведения логов)
    •   (и другие, указанные в `requirements.txt`)

## Установка

1.  **Клонируйте репозиторий:**
```bash
    git clone https://github.com/Forden/aiogram-bot-template.git
    cd <repository_directory>
```

2. **Создайте и активируйте виртуальное окружение (рекомендуется):**

  
```bash
  python3 -m venv venv
  source venv/bin/activate # Linux/macOS
  venv\Scripts\activate # Windows
```

3. **Установите зависимости:**

  
```bash
  pip install -r requirements.txt
```

4. **Настройте переменные окружения:**
```
  •  Создайте файл .env в корневой директории проекта.
  •  Добавьте необходимые переменные, например:

    TELEGRAM_BOT_TOKEN=YOUR_BOT_TOKEN
    GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY
    GOOGLE_CSE_ID=YOUR_GOOGLE_CSE_ID
    ADMIN_USER_ID=YOUR_TELEGRAM_USER_ID #ID пользователя с правами администратора

```

  •  Получите TELEGRAM_BOT_TOKEN у @BotFather (https://t.me/BotFather) в Telegram.
  •  Получите GOOGLE_API_KEY и GOOGLE_CSE_ID в Google Cloud Console, создав проект и включив Custom Search API. Затем создайте Custom Search Engine (CSE) и скопируйте его ID.

5. Запустите бота:

```bash
  python bot.py
```