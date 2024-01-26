# <center> *PROJECT-3. EDE + Feature Engineering*
# <center> *Соревнования на Kaggle*


## Оглавление
1. [Описание проекта](#описание-проекта)
2. [Используемые библиотеки](#используемые-библиотеки)
3. [Установка проекта](#установка-проекта)
4. [Авторы](#авторы)


## Описание проекта
> Представьте, что вы работаете дата-сайентистом в компании Booking. Одна из проблем компании — это нечестные отели,  
которые накручивают себе рейтинг. Одним из способов обнаружения таких отелей является построение модели,   
которая предсказывает рейтинг отеля. Если предсказания модели сильно отличаются от фактического результата,  
то, возможно, отель ведёт себя нечестно, и его стоит проверить.

Задача проекта заключается в разведывательном анализе исходных данных для построения модели.

Основные этапы анализа данных:

+ Постановка задачи
+ Подготовка Jupyter Notebook
+ Загрузка данных
+ Предварительный анализ данных
+ Разведывательный анализ и обработка данных
+ Проверка обучающих признаков
+ Подготовка тестовых данных
+ Машинное обучение



**Загрузка данных** — Данные для разведывательного анализа находятся в Data Frame hotel.csv,  
в котором содержатся сведения о 515 000 отзывов на отели Европы.  
Первоначальная версия датасета содержит 17 полей со следующей информацией:

- hotel_address — адрес отеля;
- review_date — дата, когда рецензент разместил соответствующий отзыв;
- average_score — средний балл отеля, рассчитанный на основе последнего комментария за последний год;
- hotel_name — название отеля;
- reviewer_nationality — страна рецензента;
- negative_review — отрицательный отзыв, который рецензент дал отелю;
- review_total_negative_word_counts — общее количество слов в отрицательном отзыве;
- positive_review — положительный отзыв, который рецензент дал отелю;
- review_total_positive_word_counts — общее количество слов в положительном отзыве;
- reviewer_score — оценка, которую рецензент поставил отелю на основе своего опыта;
- total_number_of_reviews_reviewer_has_given — количество отзывов, которые рецензенты дали в прошлом;
- total_number_of_reviews — общее количество действительных отзывов об отеле;
- tags — теги, которые рецензент дал отелю;
- days_since_review — количество дней между датой проверки и датой очистки;
- additional_number_of_scoring — есть также некоторые гости, которые просто поставили оценку сервису,   
  но не оставили отзыв. Это число указывает, сколько там дополнительных оценок без отзывов.
- lat — географическая широта отеля;
- lng — географическая долгота отеля.

Источник датасета: [hotel.csv](https://drive.google.com/file/d/1Qj0iYEbD64eVAaaBylJeIi3qvMzxf2C_/view?usp=sharing)

**Предварительный анализ данных** — В каждой таблице необходимо проанализировать ключевые признаки.

**Разведывательный анализ и обработка данных** 

- **Очистка данных** — необходимо проанализировать данные на дубликаты и пропуски.  
Дубликаты удалить пропуски заполнить недостающей информацией.  
Также удалить неинформативные признаки.  

- **Анализ существующих признаков** - необходимо исследовать существующий признаки на связь с целевым признаков.  
Провести построить зависимости и провести статистические тесты подтверждающие/опровергающие предварительные гипотезы.

- **Создание признаков** - необходимо использовать существующий признаки или дополнительные источники   
для создания новых признаков влияющих на целевой признак.

- **Отбор признаков для обучения модели** - после разведывательного анализа, необходимо собрать список с   
признаками для обучения модели.

**Проверка обучающих признаков** - на имеющихся данных обучить модель и проверить ее качество предсказания   
(Качество решения: результат метрики MAPE)

**Подготовка тестовых данных** - подгрузить данные для предсказания модели. Добавить в них признаки созданные  
на этапе разведывательного анализа.

**Машинное обучение** - обучить модель на всей выборке исходных данных. Сделать предсказание модели на   
тестовой выборке.

**О структуре проекта:**

* [Project-3.EDA+FE.Kaggly.ipynb](https://github.com/Wiruto/Skillfactory_project_2/blob/3901bf3492a2d94717cd0a2ebff4cda4017c6890/Project-2.ipynb) - jupyter-ноутбук, содержащий основной код проекта.

* [hotels.csv](https://github.com/Wiruto/Skillfactory_project_2/blob/3901bf3492a2d94717cd0a2ebff4cda4017c6890/Project-2.ipynb) - исходные данные для разведывательного анализа и обучения модели.

* [hotels_test.csv](https://github.com/Wiruto/Skillfactory_project_2/blob/3901bf3492a2d94717cd0a2ebff4cda4017c6890/Project-2.ipynb) - данные для проверки предсказания модели.


* [submission.csv](https://github.com/Wiruto/Skillfactory_project_2/blob/3901bf3492a2d94717cd0a2ebff4cda4017c6890/Project-2.ipynb) - результат предсказания модели.



## Используемые библиотеки


- библиотеки для работы с данными:
    - pandas
    - numpy

- библиотеки для работы с кодировщиками:
    - category_encoders

- библиотеки для подсчета в списках:
    - from collections import Counter

- библиотеки для работы со статистическим анализом:
    - scipy
    - statsmodels.api
    - statsmodels

- библиотеки для работы с регулярными выражениями:
    - re

- библиотеки для работы с геоданными:
    - geopy.geocoders
    - geopy.distance

- библиотека для разбивки выборок из данных:  
    - from sklearn.model_selection import train_test_split

- библиотеки для создания модели:  
    - from sklearn.ensemble import RandomForestRegressor  
    - from sklearn import metrics

- библиотек для работы с plotly графикой
    - plotly.graph_objects
    - plotly.figure_factory
    - plotly.express
    - plotly.subplots

- библиотеки для визуализации
    - import matplotlib.pyplot as plt
    - import seaborn as sns 
    - %matplotlib inline

- библиотеки для игнорирования сообщений warnings
    - warnings
    - warnings.filterwarnings('ignore')

## Установка проекта

```
git clone https://github.com/Wiruto/skillfactory_project_2.git

```

## Авторы

* [Колобов Виктор Валерьевич](https://github.com/Wiruto)

