🎬 Text Sentiment Analysis Model for Movie Reviews

Модель для классификации тональности текстовых отзывов о фильмах на положительные (positive) или отрицательные (negative) с высокой точностью.

📌 Пример работы
Входной текст:

"A wonderful way to spend a hot summer weekend... Woody Allen still in full control of his style... I laughed more than in any of Woody's comedies in years..."

Прогноз модели:

json
{
  "sentiment": "positive",
  "confidence": 0.96
} 

📊 О модели

Архитектура


🔹 Embedding Layer (vocab_size, embedding_dim, input_length=max_length)

🔹 SpatialDropout1D (0.39)

🔹 Bidirectional(GRU(128)) (return_sequences=True, recurrent_dropout=0.3, dropout=0.37)

🔹 LayerNormalization()

🔹 Dropout(0.55)

🔹 Bidirectional(GRU(64))

🔹 LayerNormalization()

🔹 Dense(64, activation='swish')

🔹 Dropout(0.4)

🔹 Dense(2, activation='softmax')

Оптимизация

🔸 Optimizer: Adam (learning_rate=0.001)

🔸 Loss: categorical_crossentropy

🔸 Metrics: accuracy

Метрики на тестовых данных
📈 Accuracy: 0.897
📉 Loss: 0.263

🎥 Датасет
Модель обучена на IMDB Movie Reviews Dataset с Kaggle:
✔ 35,000 отзывов (из 50,000 возможных)
✔ Сбалансированные классы (50% positive, 50% negative)

🚀 Быстрый запуск

Google Colab

📥 Скачайте ноутбук:

🔗 Использование_модели__Анализ_тональности_текста_ (1).ipynb

📌 Запустите в Google Colab( В нем будет загружена модель, токенизатор и параметры)


⭐ Если проект вам понравился, поставьте звезду!
🔄 Пулл-реквесты и предложения приветствуются!

Контакты
📧 Email: volodya.zorin.06@mail.ru


🎭 Классифицируйте отзывы с легкостью! 🚀
