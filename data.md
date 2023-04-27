---
layout: default
---

## Подготовка данных

Фреймворк предоставляет несколько готовых функций для предварительной обработки данных:

* `map` - применяет маппер `func` к каждому элементу `iterable`, возвращает измененную структуру данных.
* `minibatch` - нарезает входные данные `data` на пачки записей размера `batch_size`. 
* `shuffle` - случайное перемешивание порядка входных данных `data`.
* `train_test_split` - разделяет массив входных данных `arr` на обучающую и тестовую выборки так, что `размер тестовой выборки` = `part` * `размер всей выборки`. По умолчанию `part` = 0.8.

## Использований функций для обработки данных

```python
iris_data = shuffle(list(zip(iris.data, iris.target)))
```

```python
train_x, test_x = train_test_split(feauters_labels[0], 0.8)
```

```python
 x_batches = minibatch(x_train, 4)
 y_batches = minibatch(y_train, 4)
```
[Назад](./)
