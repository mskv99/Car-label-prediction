# Car-label-prediction
В этом проекте сравниваются различные алгоритмы машинного обучения с подбором гиперпараметров для предсказания марки автомобиля. С данными подробнее можно ознакомиться [здесь](https://archive.ics.uci.edu/dataset/149/statlog+vehicle+silhouettes). Предобработка данных включает в себя поиск пропущенных значений, поиск лишних столбцов, например дублирующих индекс датафрейма, анализ корреляции признаков, анализ распредления переменных. Для оценки результатов работы модели используются метрики accuracy, recall, f1-мера,площадь по ROC-кривой. В работе также используется метод главных компонент для сокращения размерности данных при использовании логистической регрессии. 
***
Используемые алгоритмы машинного обучения:
* Логистическая регрессия;
* Метод главных компонент;
* Решающие деревья;
* Случайный лес;
* Бэггинг
***

## Выводы
Ниже будет представлена часть выводов, которые были сделаны в данной работе. Более подробный анализ сравнения моделей можно почитать с самой работе:
* Ансамбль из лог. регрессий показал лучший результат, чем ансамбль из решающих деревьев;
* Максимальная точность у ансамбля из лог. регрессий наблюдалась при `N = 22`(N - кол-во моделей при использовании ансамбля). Далее с ростом N колебалаась около значения 0.74;
* У ансамбля из решающих деревьев наблюдалось скачкообразное измнение точности. Максимум при `N = 57`;
* Графики accuracy и f1-меры практически не отличаются друг от друга для одного и того же ансамбля;
* Анасамбль из решающих деревье показал лучшую точность по сравнению с одним решающим деревом(0.69 > 0.66), поэтому нет смысла подбирать другие гиперпараметры для ансамбля деревьев;
* Ансамбль из лог. регрессий показал результат хуже, чем обычная лог. регрессия(0.74 < 0.79 )
