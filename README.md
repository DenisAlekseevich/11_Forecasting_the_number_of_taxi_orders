# Прогнозирование количества заказов такси

## Задача проекта

Компания «Чётенькое такси» собрала исторические данные о заказах такси в аэропортах. Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час. Необходимо построить модель для такого предсказания.

Значение метрики _**RMSE**_ на тестовой выборке должно быть не больше 48.

Необходимо:
- загрузить данные и выполнить их ресемплирование по одному часу;
- проанализировать данные;
- обучить разные модели с различными гиперпараметрами, сделать тестовую выборку размером 10% от исходных данных;
- проверить данные на тестовой выборке и сделать выводы.

## Инструменты и навыки
`Python`
`Pandas`
`Numpy`
`Matplotlib`
`Scikit-learn`
`Statsmodels`
`Catboost`

## Краткое описание выполнения проекта

Проанализированы исторические данные о заказах такси в аэропортах.
Спрогнозировано количество заказов такси на следующий час, чтобы привлекать больше водителей в период пиковой нагрузки. Построена модель для такого предсказания. Достигнуто значение метрики _**RMSE**_ на тестовой выборке менее 41. 

## Данные и выводы

Анализ данных показал заметную сезонность - пиковые нагрузки приходятся на 17 часов, тогда как минимальное количество заказов поступает ранним утром (6-7 часов). На основании этих данных можно создать рекомендацию о дополнительном увеличении количества экипажей такси именно в эти часы.

В ходе исследования были протестированы 3 модели - **логистическая регрессия**, **случайный лес** и **CatBoost**, и все они показали значение _**RMSE**_ на тестовой выборке меньше 48. Лучший показатель у **CatBoost** - 40.1.

Цели и задачи исследования достигнуты, однако для улучшения метрики стоит взять больший период времени или найти дополнительные фичи (например, ввести признаки праздничных и выходных дней).
