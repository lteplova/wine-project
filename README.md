# Проект классификации качества "Wine Quality"
Датасет получен с Kaggle - https://www.kaggle.com/datasets/rajyellow46/wine-quality
## Цель проекта

Предсказать класс качества вина.

## Описание

Датасет содержит физико-химические характеристики и и органолептические (выходные) переменные красного и белого португальского вина Vinho Verde. 

Набор данных был загружен из репозитория машинного обучения [UCI](https://https://archive.ics.uci.edu/ml/datasets/wine+quality).

Классы упорядочены и не сбалансированы.


Описание от  [Kaggle](https://https://www.kaggle.com/datasets/rajyellow46/wine-quality?resource=download)

Описание переменных:

0 - тип (белое или красное)

1 - fixed acidity (фиксированная кислотность)

2 - volatile acidity (летучая кислотность)

3 - citric acid (лимонная кислота)

4 - residual sugar (остаточный сахар)

5 - chlorides (хлорид)

6 - free sulfur dioxide (свободный диоксид серы)

7 - total sulfur dioxide (общий диоксид серы)

8 - density (плотность)

9 - pH

10 - sulphates (сульфаты)

11 - alcohol (содержание спирта)

Выходные данные:

12 - quality (score between 0 and 10) - качество от 0 до 10

## Процесс ведения работы

* Проведено предварительное тестирование на baseline данных без предобработки StackingClassifier ( метрика -  accuracy - 0.61)
* Проведен анализ данных на корреляцию, удалены зависимые признаки
* Удалены выбросы
* Удалены пропуски
* Сгенерированы несколько новых признаков 


## Итоги

В ходе проведения работы было проведено обучение с помощью стэкинга моделей
StackingClassifier(
    [
        ('DecisionTreeClassifier', DecisionTreeClassifier()),
        ('RandomForestClassifier', RandomForestClassifier()),
        ('LinearSVC', LinearSVC())
    ])
Результирующая метрика -  accuracy - 0.67
Обработка данных позволила. улучшить результат.

