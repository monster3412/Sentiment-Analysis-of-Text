
Модель для классификации тональности текстовых отзывов о фильмах на положительные (positive) или отрицательные (negative).

## 📌 Пример работы

**Входной текст:**
"A wonderful way to spend a hot summer weekend... Woody Allen still in full control of his style... I laughed more than in any of Woody's comedies in years..."


**Прогноз модели:**
```json
{
  "sentiment": "positive",
  "confidence": 0.96
}
📊 О модели:

Архитектура:

Embedding Layer ( vocab_size, embedding_dim, input_length=max_length)

SpatialDropout1D(0.39))

Bidirectional(GRU(128, return_sequences=True, recurrent_dropout=0.3, dropout=0.37))

LayerNormalization())

Dropout(0.55))

Bidirectional(GRU(64)))

LayerNormalization())


Dense(64, activation='swish')

Dropout(0.4)

Dense(y_train_cat.shape[1], activation='softmax')

optimizer - Adam

learning_rate=0.001

loss-categorical_crossentropy,

metrics-accuracy



Метрики на тестовых данных:

Метрика	Значение
Accuracy	0.897
Loss	0.263

Датасет
Модель обучена на IMDB Movie Reviews Dataset с Kaggle:

35,000 отзывов из 50000 возможных

Сбалансированные классы (50% positive, 50% negative)

🚀 Запуск с готовой моделью:

1. Скачайте файл "Анализ тональности текста (2).ipynb"

2. Запустите его в Google Colaboratory
