# 🧠 Распознавание токсичных комментариев с помощью BERT

## 📌 Описание проекта

Компания **«Викишоп»** запустила сервис пользовательских комментариев и столкнулась с проблемой токсичных высказываний.  
Для поддержания комфортной среды на платформе требуется **автоматическая система модерации**, которая сможет выявлять токсичные комментарии и отправлять их на ручную проверку.

🎯 **Цель проекта**:
- Обучить модель, определяющую токсичность комментария.
- Достичь F1-score ≥ 0.75 для практического использования.
- Сравнить разные подходы (TF-IDF, BERT).
- Разработать решение для автоматической фильтрации комментариев.

---

## 🎯 Основные задачи

- Загрузка и анализ данных (text, toxic).
- Предобработка текста: очистка, лемматизация, удаление шумов.
- Векторизация текста: TF-IDF, BERT (RuBERT).
- Балансировка классов: использование SMOTE.
- Обучение моделей: Logistic Regression, BERT.
- Оценка метрик: accuracy, precision, recall, F1.
- Анализ ошибок и улучшения.

---

## 📂 Содержание

[📌 Посмотреть проект можно здесь](project/toxic_comments_BERT.ipynb)

---

## 🔬 Используемые методы и библиотеки

### 📚 Библиотеки:
- `pandas`, `numpy` — работа с данными
- `nltk`, `spaCy`, `pymystem3` — обработка текста
- `matplotlib`, `seaborn`, `wordcloud` — визуализация
- `scikit-learn`, `imblearn` — ML, метрики, балансировка
- `transformers`, `torch` — нейросети и BERT

### 🤖 Методы:
- TF-IDF + Logistic Regression (baseline)
- RuBERT (BERT для русского языка): эмбеддинги, дообучение
- SMOTE для борьбы с дисбалансом классов
- F1-score как основная метрика качества
- SHAP-анализ и визуализация ошибок

---

## 📈 Основные результаты

🏆 **Итоговая модель — RuBERT**

| Метрика      | Значение     |
|--------------|--------------|
| Accuracy     | 96.4%        |
| Precision    | 89.6%        |
| Recall       | 72.5%        |
| **F1-score** | **80.2%**    |

✅ Модель демонстрирует **высокую точность** и **достаточный recall** для практического применения.  
✅ Использование BERT обеспечило **значительно лучшие результаты**, чем классические методы.

---

## 📌 Выводы и рекомендации

- Модель подходит для реальной модерации комментариев.
- Возможны улучшения:
  - Дообучение на дополнительных токсичных примерах;
  - Оптимизация гиперпараметров;
  - Добавление текстовых аугментаций;
  - Интеграция модели через API в продакшен.

---

## 🔧 Установка

Для запуска проекта потребуется Python 3.x и следующие библиотеки:

```bash
pip install pandas numpy nltk spacy matplotlib seaborn torch transformers wordcloud imbalanced-learn scikit-learn pymystem3
