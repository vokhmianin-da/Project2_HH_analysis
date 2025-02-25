# <center> Проект 1: Анализ резюме из HeadHunter(SQL)

## Оглавление  
[1. Описание проекта](#Описание-проекта)  
[2. Задача](#Задача)  
[3. Краткая информация о данных](#Краткая-информация-о-данных)  
[4. Этапы работы над проектом](#Этапы-работы-над-проектом)  
[5. Результат](#Результаты)    
[6. Выводы](#Выводы) 

### Описание проекта    
Анализ базы банных HeadHunter с применением sql - запросов.

:arrow_up:[к оглавлению](#Оглавление)


### Задача    
Необходимо провести анализ базы данных HeadHunter, отражающей вакансии, размещенные работодателями, регионы нахождения вакансий, а также самих работодателей и их сферы деятельности.  


**Метрика качества**     
* Решение оформляется только в Jupyter Notebook;
* Решение оформляется в соответствии с ноутбуком-шаблоном;
* Каждое задание выполняется в отдельной ячейке, выделенной под задание (в шаблоне они помечены как ваш код здесь). Не следует создавать много ячеек для решения задачи — это провоцирует неудобства при проверке.
* Текст SQL-запросов и код на Python должны быть читаемыми. Не забывайте про отступы в SQL-коде.
* Выводы по каждому этапу оформляются в формате Markdown в отдельной ячейке (в шаблоне они помечены как ваши выводы здесь).
* Выводы можно дополнительно проиллюстрировать с помощью графиков. Они оформляются в соответствии с теми правилами, которые мы приводили в модуле по визуализации данных.
* Не забудьте удалить ячейку с данными соединения перед фиксацией работы в GitHub.

:arrow_up:[к оглавлению](#Оглавление)


### Краткая информация о данных
Для анализа были предоставлены 5 таблиц, содержащих следующую информацию:
1. Таблица Vacancies:
* id - идентификатор вакансии (тип данных int4);
* name - название вакансии (тип данных text);
* key_skills - ключевые навыки (тип данных text); 
* schedule - тип рабочего графика (тип данных text);
* experience - требования к опыту (тип данных text);
* employment - тип трудоустройства (тип данных text);
* salary_from - нижняя граница зарплатной вилки (тип данных int4);
* salary_to - верхняя граница зарплатной вилки (тип данных int4);
* area_id - идентификатор региона вакансии (тип данных int4);
* employer_id - идентификатор работодателя (тип данных int4).

2. Таблица Areas
* id - идентификатор города (тип данных int4);
* name - название города (тип данных text).

3. Таблица Employers
* id - идентификатор работодателя (тип данных int4);
* name - наименование работодателя (тип данных text);                               
* area - идентификатор региона работодателя (тип данных int4).

4. Таблица Industries:        
* id - идентификатор сферы деятельности (тип данных varchar(10));    
* name - название сферы деятельности (тип данных text).                        

5. Таблица Employers_Industries: 
* employer_id - идентификатор работодателя (тип данных int4);                           
* industry_id - идентификатор сферы деятельности(тип данных varchar(10)).                      

  
:arrow_up:[к оглавлению](#Оглавление)


### Этапы работы над проектом  
**Предварительный анализ данных:**  
Первичное изучение данных: 
* Анализ размерности таблиц.


**Детальный анализ вакансий**
Анализ данных отражающих информацию о количестве вакансий, их месте нахождения и графиках работы, а также данные об необходимом опыте работы и о предлагаемой заработной плате:
* Анализ городов с максимальным количеством вакансий в отношении всего рынка труда;
* Анализ зарплатной вилки;
* Анализ наиболее востребованных рынком труда специалистов. 


**Анализ работодателей**
Анализ данных отражающих информацию о работодателях, их сферах деятельности, а также регионах, в которых работодатели публикуют свои вакансии:
* Анализ популярности регионов среди работодателей;
* Анализ сфер деятельности работодателей.


**Предметный анализ**
Анализ вакансий, в частности, поскольку интерес проекта сосредоточен на вакансиях в сфере IT, бы проведен анализ вакансий на позицию Data scientist (далее - DS).:
* Анализ количества вакансий junior (начинающий специалист) DS;
* Анализ ключевых навыков DS, а также их среднего количества;
* Анализ средних значений зарплатной вилки DS.

:arrow_up:[к оглавлению](#Оглавление)


### Результаты:  
В результате проделанной работы были написаны sql - запросы, позволяющие произвести анализ представленных данных.    

:arrow_up:[к оглавлению](#Оглавление)


### Выводы:  
Настоящая задача наглядно показывает работу с базой данных PostgreSQL, развивает навык написания SQL-запросов.

:arrow_up:[к оглавлению](#Оглавление)
