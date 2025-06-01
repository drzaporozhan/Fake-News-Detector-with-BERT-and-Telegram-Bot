# Fake News Detection Bot

Этот проект представляет собой Telegram-бота, который определяет, является ли новостная статья фейковой или настоящей. В основе лежит модель BERT, дообученная на политических новостях.

## Описание

Цель — выявление фейковых новостей в политической сфере.

В рамках проекта:

- Проведена предобработка и очистка текстов.
- Векторизация выполнена с использованием Sentence-BERT.
- Обучены и сравнены несколько моделей, из которых лучшей оказалась BERT.
- Разработан Telegram-бот, который принимает `.txt` файл и возвращает результат классификации.

## Структура проекта

- `notebooks/1_model_training.ipynb` — обучение моделей и сохранение дообученной BERT.
- `notebooks/2_telegram_bot.ipynb` — запуск Telegram-бота в Google Colab.
- `requirements.txt` — список библиотек.

Папки `bert_model/` и `data/` **не включены в репозиторий** из-за ограничений GitHub. Скачайте их вручную по ссылкам ниже.

## ⬇Загрузка необходимых данных

- **Модель BERT:**  
  [Скачать папку `bert_model/`](https://drive.google.com/drive/u/1/folders/1F24k1SFeRHXrW3c2SyGXFr1C79QfNYuk)

- **Файлы с данными (`Fake.csv`, `True.csv`, `.npy` и т. д.):**  
  [Скачать папку `data/`](https://drive.google.com/drive/u/1/folders/11RAcP6jRG49pK1FKbGAZ_WeLoTutJurq)

После скачивания:

- Разместите папку `bert_model/` в корне проекта.
- Поместите файлы из `data/` в корень проекта или настройте пути в `1_model_training.ipynb`.

## Как использовать

1. Откройте проект в Google Colab.
2. Загрузите `bert_model/` и `data/` с Google Drive.
3. В `notebooks/2_telegram_bot.ipynb` вставьте свой Telegram Bot Token.
4. Запустите ячейки и отправьте .txt файл в Telegram-бота.
5. Получите результат классификации: REAL или FAKE.

## Используемые технологии

- Python
- HuggingFace Transformers (`bert-base-uncased`)
- sentence-transformers (`all-MiniLM-L6-v2`)
- scikit-learn
- spaCy
- NLTK
- Telegram Bot API

## Пример

**Вход:** текстовая статья `.txt`  
**Выход:** сообщение `Результат анализа: REAL` или `FAKE`
