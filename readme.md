# Описание
Этот код реализует простую нейронную сеть для распознавания рукописных цифр из набора данных MNIST. Вот что делает этот код:

Загрузка данных MNIST: Код загружает набор данных MNIST, который содержит 60,000 изображений тренировочных данных и 10,000 изображений тестовых данных рукописных цифр.
Предварительная обработка данных: Изображения нормализуются, чтобы значения пикселей находились в диапазоне от 0 до 1.
Построение модели: Создается последовательная модель Keras, состоящая из следующих слоев:
Flatten: Преобразует двумерные изображения в одномерные входные данные.
Dense(128, activation='relu'): Полносвязный слой с 128 нейронами и функцией активации ReLU.
Dense(10): Полносвязный выходной слой с 10 нейронами (по одному на каждый класс цифры от 0 до 9).
Компиляция модели: Модель компилируется с оптимизатором Adam, функцией потерь SparseCategoricalCrossentropy и метрикой точности.
Обучение модели: Модель обучается на тренировочных данных в течение 10 эпох.
Оценка модели: Модель оценивается на тестовых данных, и выводится значение точности.
Вывод предсказаний: Создается новая последовательная модель, которая добавляет к исходной модели слой Softmax для получения вероятностей предсказаний. Затем эта модель используется для предсказания класса одного из тестовых изображений, и результат выводится на экран вместе с изображением.
Таким образом, этот код демонстрирует основы построения, обучения и использования простой нейронной сети для распознавания рукописных цифр.
# Использование
Клонировать репозиторий:
```
git clone https://github.com/Processori7/WhatInum.git```
Перейти в каталог:
```
cd Emotion_recognition
```
Создать виртуальное окружение:
```
python -m venv venv
```
Активировать окружение:
```
venv\Scripts\activate.bat
```
или
```
.venv\Scripts\activate.bat
```
Выполнить установку зависимостей:
```
pip install -r requirements.txt
```
Далее запустить файл:
```
python WhatInum.py
```