Программа выбирает город, в который лучше всего улететь на ближайших выходных (то есть где теплее всего). 

Данные берутся с сайта gismeteo.ru

Рассматриваются 24 самых популярных города.

С помощью `api aviasales` подбирается самый дешевый билет.

Функция возвращает словарь вида {'price': 1999 } или {'error_text': 'No tickets'}


Примечания:
* Если билета нет, то выводится соответствующая информация.
* Если нынешний день - воскресенье, то билеты смотрятся на следующую неделю.
* Считается скользящее среднее арифметическое максимальной температуры с шириной окна в 3 дня (просто так).
* Используются `requests`, `bs4`, `fake_useragent`, `datetime`, `jsonpandas `.
