# hw2_2024

Основная и бонусные части


https://colab.research.google.com/drive/1hg6SdeVDuBpHPwWd8MEndr6zz3jRb0ei?usp=sharing

Клеточная линия | Гистоновая метка | Реплика 1 | Реплика 2 | Контрольный эксперимент 
--- | --- | --- | --- | ---
A549 | H3K4me2 | ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ

1. Отчеты Fastqc
 
   При анализе Fastqc подрезание прочтений и фильтрация не потребовалось, так как большинство разделов в Summary отмечены, как корректно выполненные.



   Summary



     ENCFF507YIE
   
    <img width="181" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/86fdf1de-7b6c-401a-9222-5c9cb961d6ea">

    ENCFF826KAA

    <img width="195" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/f59799c1-1723-46f0-8642-90c8e7aa6b3a">

    ENCFF232NPZ

    <img width="179" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/0d88bbe5-9126-4e6d-b6ae-67f7e9bb2fa6">


Можем сделать вывод, что большинство анализов проведены корректно

Basic statistics



ENCFF507YIE

<img width="746" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/aed8fb98-218d-4790-acd8-1006137b8bf9">



ENCFF826KAA

<img width="753" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/251f9387-e011-407c-820b-429968452311">



ENCFF232NPZ

<img width="767" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/8fcc965f-5ca5-4816-aa1d-8978a5ea032c">



Выше представлена базовая информация FASTQ файле. Важными показателями являются: общее количество чтений, длина чтения и содержание GC.



Per tile sequence quality


ENCFF507YIE
<img width="755" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/8d279498-8607-417b-8e3b-8b445912e78e">




ENCFF826KAA
<img width="760" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/adc4c8aa-7a4a-4050-897a-6d9acac4dc18">



ENCFF232NPZ
<img width="760" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/2d86ce80-8a25-46c3-b582-643bbccf99b2">

Информация выше позволяет оценить средние показатели качества по всем данным. Результаты во всех трех экспериментах, включая контрольный, оказались почти идеальными. Единственное исключение — второй график (образец ENCFF826KAA), на котором видны несколько светлых участков, указывающих на то, что качество в этих позициях было на уровне или выше среднего.



Per base sequence content


ENCFF507YIE
<img width="761" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/602ac12f-2cb6-4255-9128-f306e716486b">



ENCFF826KAA
<img width="775" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/2b18fae2-08c6-4411-ac1b-8107b68ab816">



ENCFF232NPZ
<img width="763" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/265a72f6-bb61-42ad-844c-7dac24c94c16">

Уровни аденина (A), гуанина (G), цитозина (C) и тимина (T) остаются стабильными, причем азотистые основания разделились на две группы: тимин+аденин и цитозин+гуанин. Это наблюдение видно на всех трех графиках и свидетельствует о нормальных значениях.



Per sequence GC content


ENCFF507YIE
<img width="643" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/7a8f6e04-918c-4210-a89c-161b4524d454">

ENCFF826KAA
<img width="723" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/947b5951-c5a0-4f84-ba68-1bf81f9a17f4">

ENCFF232NPZ
<img width="717" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/ac4132d4-c600-47ff-be2c-e67b6a7d1132">

На третьем графике кривые напоминают нормальное распределение, где среднее значение соответствует среднему содержанию GC в секвенируемом организме. Однако для первых двух скриншотов можно заметить, что их распределение отличается от нормального, что отмечено в таблице Summary восклицательным знаком, указывающим на возможные проблемы в этом анализе.



2. Таблица со статистикой по каждому из 3 образцов

  Образец | Всего ридов | Выровнилось уникально | Выровнилось уникально(%) |	Выровнилось неуникально | Выровнилось неуникально(%) | Не выровнилось | Не выровнилось(%)
  --- | --- | --- | --- | --- | --- | --- | --- 
  ENCFF507YIE | 45551674 | 1278836 | 2.81% | 4569570 | 10.03% | 39703268	| 87.16%
  ENCFF826KAA	| 46522698 | 1129018	| 2.43%	| 3765869	| 8.09%	| 41627811	| 89.48%
  ENCFF232NPZ	| 26282868 | 865880	| 3.29%	| 3363247 |	12.80%	| 22053741	| 83.91%

 Процент выравниваний получился низким, так как выравнивание ридов производилось на одну хромосому, которая составляет небольшую часть генома человека.


 3. Диаграммы Венна
  
ENCFF507YIE


Количество участков из файла для ENCFF507YIE, которые пересекаются с файлом для ENCFF806AQL
<img width="587" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/ea38d71a-d459-4c08-a6bb-0177080b041b">

Количество участков из файла для ENCFF806AQL, которые пересекаются с файлом для ENCFF507YIE


<img width="583" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/ed4cb596-6bad-4bf6-a12e-694997e89081">

ENCFF826KAA


Количество участков из файла для ENCFF826KAA, которые пересекаются с файлом для ENCFF806AQL
<img width="594" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/dd86d1f1-df87-4f3c-b593-63203942e048">

Количество участков из файла для ENCFF806AQL, которые пересекаются с файлом для ENCFF826KAA

<img width="782" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/0cd60cd1-0f43-4cfc-a867-bd0c977e5bd3">


Количество пересекающихся участков небольшое. В начале наблюдается относительно небольшое количество пиков, так как выравнивание выполнялось только на одну хромосому. Для файла ENCFF806AQL из ENCODE количество пиков больше, поскольку выравнивание проводилось на все хромосомы. Также можно заметить, что пересечения на двух графиках в одной таблице не совпадают из-за различий в методах определения пересечений.

4. Бонусная часть

ngs.plot для ENCFF066HKS.bam

<img width="192" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/6db32569-ddc6-4d52-b2c4-fa5e125f3d2e">

ngs.plot для ENCFF346XTR.bam

<img width="186" alt="image" src="https://github.com/npoisoned/hw2_2024/assets/90446751/4524c7b3-3b32-4a42-bb70-bcb82333ea24">

Полученные графики для .bam файлов напоминают типичное распределение гистоновой метки относительно генов. Однако, на полученном графике наблюдается смещение в левую сторону: сначала виден резкий рост, затем более плавный спад. В то время как на графике с типичным распределением рост и спад более плавные и практически одинаковые. Таким образом, теоретическое расположение гистоновой метки относительно генов отличается от полученного результата.



