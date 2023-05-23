Проект "Прогнозирование данных о раке с помощью логистической регрессии" направлен на создание модели, которая будет предсказывать наличие рака у пациента на основе данных о его заболевании. Для этого используется алгоритм логистической регрессии, который обучается на предоставленных данных и определяет вероятность наличия рака.

Переменные:
- data: датасет с данными о раке
- x_data: данные без столбца "diagnosis"
- y: столбец "diagnosis" с бинарными значениями (1 - рак, 0 - нет рака)
- x: нормализованные значения x_data
- x_train, x_test, y_train, y_test: разделенные на тренировочные и тестовые данные
- w: веса
- b: сдвиг
- z: результат умножения весов на данные и добавления сдвига
- y_head: вероятность наличия рака, полученная с помощью сигмоидной функции
- loss: функция потерь
- cost: среднее значение функции потерь
- gradients: градиенты для весов и сдвига
- Y_prediction: предсказанные значения наличия рака

Функции:
- initialize_weights_and_bias(dimension): инициализация весов и сдвига
- sigmoid(z): сигмоидная функция, преобразующая z в вероятность
- forward_bacward_propagation(w, b, x_train, y_train): прямое и обратное распространение для определения функции потерь и градиентов
- update(w, b, x_train, y_train, learning_rate, number_of_iteration): обновление весов и сдвига с помощью градиентного спуска
- predict(w, b, x_test): предсказание наличия рака на основе обученных весов и сдвига

В ходе проекта выполняются следующие шаги:
1. Загрузка данных о раке.
2. Предобработка данных: удаление ненужных столбцов, преобразование столбца "diagnosis" в бинарные значения.
3. Разделение данных на тренировочные и тестовые.
4. Нормализация данных.
5. Инициализация весов и сдвига.
6. Обучение модели с использованием градиентного спуска.
7. Предсказание наличия рака на основе обученной модели.
8. Визуализация изменения функции потерь в процессе обучения.
