﻿# agglomerative_clustering

*** ПРЕДНАЗНАЧЕНИЕ ПРОГРАММЫ ***

Программа решает задачу кластеризации (кластерного анализа).

	Справка:
	Кластерный анализ (Data clustering) — задача разбиения заданной выборки объектов (ситуаций) на непересекающиеся подмножества, называемые  кластерами, так, чтобы каждый кластер состоял из схожих объектов, а объекты разных кластеров существенно отличались.
	Подробнее: http://www.machinelearning.ru/wiki/index.php?title=Кластеризация

Программа реализует алгоритм агломеративной иерархической кластеризации, вариант Ланса-Вильямса с оптимизизацией производительности (редуктивный алгоритм) и пятью различными функциями нахождения расстояния между кластерами.
Подбробнее: https://ru.wikipedia.org/wiki/Иерархическая_кластеризация

Программа получает на входе набор объектов с указанием их параметров (признаков), разбивает их на кластеры и позволяет изучать эти разбиения, изменяя количество кластеров и способ нахождения расстояния между ними. Результат разбиения можно сохранить в файл.


*** АЛГОРИТМ РАБОТЫ С ПРОГРАММОЙ ***

1. Выберите набор объектов (датасет) для исследования. Для этого нажмите "Загрузить объекты" и выберите файл с расширением .txt.
Файл должен иметь следующий формат:
Первая строка: <Название_первого_признака> <Название_второго_признака> mark(опционально)
Каждая следующая строка описывает один объект: <Значение_первого_признака> <Значение_второго_признака> <Метка(опционально)>
Разделитель - пробел ( ).
Значение признаков могут быть, как целыми, так и дробными (разделитель целой и дробной части - запятая (,)).
Дождитесь окончания обработки файла и первичной отрисовки объектов.
Примеры наборов можете найти в папке Datasets.

2. Выберите алгоритм кластеризации, функцию нахождения расстояния между кластерами, параметры кластеризации и количество кластеров (все настройки можно оставить по умолчанию (заранее выбраны наиболее эффективные параметры для большинства случаев)).

3. Нажмите кнопку "Кластеризовать объекты".
Дождитесь окончания кластеризации (время ожидания зависит от количества объектов (400 объектов ~ 1 с, 2000 объектов ~ 15 с. 5000 ~ 1 мин.)).

4. Изменяя количество отображаемых кластеров и размер точек, по нажатию кнопки "Отобразить кластеры", можете найти интересующее Вас разбиение на кластеры. Для получения другого разбиения измените функцию нахождения расстояния между кластерами, а также иные параметры кластеризации и нажмите кнопку "Кластеризовать объекты".

5. Сохраните отображаемое разбиение на кластеры в файл с помощью кнопки "Сохранить кластеры".
Примеры сохранённых кластеров можете найти в папке Clusters.


*** ЗНАЧЕНИЕ ПАРАМЕТРОВ ***

Параметры кластеризации

	* Алгоритм кластеризации - определяет алгоритм кластерного анализа (сильно влияет на результат кластеризации). 

	* Функция нахождения расстояния между кластерами - определяет способ нахождения расстояния между кластерами, исследуя количество и параметры входящих в них объектов (сильно влияет на результат кластеризации).

	* n_1 - определяет минимальное количество объектов, с которым начинает использоваться механизм повышения скорости кластеризации. Рекомендуемые значения: 20 ~ 500 (влияет на скорость работы алгоритма).

	* n_2 - определяет количество случайно выбираемых расстояний, используемых в механизме повышения скорости кластеризации. Рекомендуемые значения: 20 ~ 100 (влияет на скорость работы алгоритма).

Параметры отображения

	* Количество кластеров - влияет на количество отображаемых на экране и сохраняемых в файл кластеров.

	* Радиус точек - определяет размер отобраемых точек-объектов.
