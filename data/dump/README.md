Данные собраны с http://www.vybory.izbirkom.ru/region/izbirkom?action=show&root_a=null&vrn=100100067795849&region=0&global=true&type=0&prver=0&pronetvd=0

# uiks.tsv

Список УИКов из раздела "Данные об открытии помещений для голосования" http://www.vybory.izbirkom.ru/region/region/izbirkom?action=show&root=1&tvd=100100067795854&vrn=100100067795849&region=0&global=true&sub_region=0&prver=0&pronetvd=0&vibid=100100067795854&type=238 .

address берётся со страничек региональных ИКов, например, http://www.kirov.vybory.izbirkom.ru/kirov/ik/4434001113184 . По этому адресу определяются координаты: latitude, longitude.


```
id	name	region_id	region_name	oik	tik_id	tik_name	address	latitude	longitude
4364022101535	УИК №2203	voronezh	Воронежская область	88	23620001147696	Нововоронежская городская	396070, Воронежская область, г.Нововоронеж, пл.имени Ленина, д.1 (здание Дворца культуры)	51.309213	39.216277
4504062211518	УИК №3401	moscow_reg	Московская область	127	25020002005583	Щелковская	141100, Московская область, Щелковский муниципальный район, городское поселение Щёлково, ул.Комсомольская, д.8А (МОАУ СОШ №2 ЩМР)		
4244045149781	УИК №654	krasnoyarsk	Красноярский край	57	22420001180066	Норильская городская	663333, Красноярский край, г. Норильск, ул. Енисейская, д. 26 (здание МБОУ 'Средняя школа № 38')	69.497807	88.395419
4664016137314	УИК №1326	sverdlovsk	Свердловская область	168	26620001732912	Екатеринбург, Железнодорожная	620027, Свердловская область, муниципальное образование 'город Екатеринбург', Железнодорожный район, Мамина-Сибиряка, 16 (здание техникума 'Кулинар')	56.852263	60.612845
```

# odnomandats.tsv

Список фамилий из раздела "Сведения о кандидатах, выдвинутых по одномандатным избирательным округам" http://www.vybory.izbirkom.ru/region/region/izbirkom?action=show&root=1&tvd=100100067795854&vrn=100100067795849&region=0&global=true&sub_region=0&prver=0&pronetvd=0&vibid=100100067795849&type=220 .

nominated 1, когда в колонка "выдвижение" = "выдвинут".

```
id	fio	date	party_id	party_name	oik	nominated
4744041290994	Барышев Андрей Викторович	1966-02-02	er	"Всероссийская политическая партия ""ЕДИНАЯ РОССИЯ"""	189	1
2402000677538	Авдеев Александр Александрович	1975-08-12	er	"Всероссийская политическая партия ""ЕДИНАЯ РОССИЯ"""	99	1
2432000880419	Азимов Рахим Азизбоевич	1964-08-16	er	"Всероссийская политическая партия ""ЕДИНАЯ РОССИЯ"""	105	1
2422000977091	Алексеева Татьяна Олеговна	1962-12-16	er	"Всероссийская политическая партия ""ЕДИНАЯ РОССИЯ"""	101	1
```

# party_results.tsv

Данные из раздела "Сводная таблица предварительных итогов голосования по федеральному избирательному округу" http://www.vybory.izbirkom.ru/region/region/izbirkom?action=show&root=1&tvd=100100067795854&vrn=100100067795849&region=0&global=true&sub_region=0&prver=0&pronetvd=0&vibid=100100067795854&type=233 .

uik_id берётся из файла uiks.tsv . Если в колонке строка, например, "apple", то это число голосов за "Яблоко". Если название колонки число, то это номер строки в таблица izbirkom.ru http://www.vybory.izbirkom.ru/region/region/izbirkom?action=show&root=1&tvd=100100067795854&vrn=100100067795849&region=0&global=true&sub_region=0&prver=0&pronetvd=0&vibid=100100067795854&type=233 . Например, 2 -- это "Число избирательных бюллетеней, полученных участковой избирательной комиссией".

```
uik_id	1	2	3	4	5	6	7	8	9	10	11	12	13	14	15	16	17	18	apple	er	gp	green	gs	kommumist	kprf	ldpr	old	parnas	partiot	rodina	rost	sp
401400192739	2584	2328	0	2067	50	211	50	2067	11	2106	30	4	3	26	3	0	0	0	0	1796	0	0	0	0	97	157	0	0	0	0	0	56
401400192763	2943	2661	0	2598	17	46	17	2598	0	2615	30	8	1	22	2	0	0	0	14	1984	2	4	3	28	170	249	8	4	3	2	4	140
401400192775	2047	1846	0	1739	22	85	22	1739	3	1758	30	0	1	30	0	0	0	0	0	1441	0	0	0	0	71	140	0	0	0	0	0	106
401400192787	743	672	0	331	43	298	43	331	6	368	20	2	0	18	0	0	0	0	2	240	1	1	1	14	70	21	7	1	2	2	3	3
```

# odnomandat_resuls.tsv

Данные из раздела "Сводная таблица предварительных итогов голосования по одномандатному избирательному округу" http://www.vybory.izbirkom.ru/region/region/izbirkom?action=show&root=1&tvd=100100067795854&vrn=100100067795849&region=0&global=true&sub_region=0&prver=0&pronetvd=0&vibid=100100067795854&type=464 .

uik_id берётся из файла uiks.tsv. Если row_id меньше 19, то это номер строчки в таблице на izbirkom.ru, как в party_results.tsv. Если больше, то это id из таблицы odnomandats.tsv -- число голосов за одномандатника.


```
uik_id	row_id	value
401400192739	1	2584
401400192817	1	2511
401400192763	1	2943
401400192775	1	2047
401400192787	1	743
```