### Реализация проекта

Для реализации задачи классификации эмоций было осуществлено несколько ключевых этапов:

1. Подготовка окружения и настройка данных, включающая в себя извлечение данных из источников, скачивание тренировочных и тестовых изображений, загрузка, а так же визуальный анализ и отчистка данных

2. Подготовка данных: предобработка изображений и разделение данных

3. Создание модели EmotionClassifier, на основе сверточной нейронной сети MobileNetV2, преимуществом которой является ее предварительная подготовка и обучение на большом количестве изображений. Обучение
модели происходило в течение 3 эпох с использованием функции потерь CrossEntropyLoss и оптимизатора Adam. Для ускорения вычислений и обработки больших объемов данных
использовались пакеты размером 64 и параллельная обработка данных. Финальный слой классификации модели был заменен на слой с 9 выходными нейронами, соответствующими числу категорий эмоций:
- Гнев (anger) - 0
- Презрение (contempt) - 1
- Отвращение (disgust) - 2 
- Страх (fear) - 3
- Радость (happy) - 4
- Нейтральное выражение (neutral) - 5
- Печаль (sad) - 6
- Удивление (surprise) - 7
- Неуверенность (uncertain) - 8

5. Оценка модели и тестирование: работа модели была оценена на валидационном наборе данных, а так же были предсказаны эмоции на тестовом наборе, по результатам предсказания был сформирован итоговый файл 