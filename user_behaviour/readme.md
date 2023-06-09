# Анализ поведения пользователей мобильного приложения
## Задача
Необходимо проанализировать поведение покупателей на основании логов пользователей и результатов А/А/В - эксперимента (изменение шрифта во всем приложении).

## Данные
Логи пользователей мабильного приложения (файл logs_exp.csv)

- название события;
- уникальный идентификатор пользователя;
- время события;
- номер эксперимента: 246 и 247 — контрольные группы, а 248 — экспериментальная.
- 
## Используемые библиотеки
`pandas` `numpy` `matplotlib` `seaborn`

## Ход исследования
- Обзор и предобработка данных
- Анализ данных, воронка событий
- Анализ результатов экспериента
- Выводы

## Выводы
В результате исследования были проанализированы поведение покупателей на основании логов пользователей, а так же, результаты А/А/В-теста. После предобработки данных было рассмотрено поведение 7419-ти пользователей мобильного приложения.

Было выявлено, что:
- Главную страницу увидели 7419 пользователей (100% от общего числа пользователей); Страницу товара просмотрели 4593 пользователей (61% от общего числа); Карточку просмотрели 3734 пользователя (50% от общего числа); Завершили оплату 3539 пользователей (47% от общего числа). Еще одно событие (Tutorial) было исключено из анализа ввиду необязательного прохождения и отсутствия влияния на остальные шаги.
- Большее количество пользователей приложение теряло после первого шага (более 38%). Был проанализирован результат А/А/В-эксперимента(изменение шрифта во всем приложении), для этого были ипользованы логи событий за неделю (с 01/08/2019 по 07/08/2019).

В эксперименте были учтено поведение пользователей, разделенных на три группы:

246-ая - 2484 пользователя; 247-ая - 2513 пользователя; 248-ая - 2537 пользователя. Согласно предложенному процессу, нам нужно было сопоставить доли пользователей по каждому событию между: -контрольными группами 246 и 247; -каждой из контрольной группы по отдельности и экспериментальной (246-248 и 247-248); -объединенной контрольной группой и экспериментальной (246+247 и 248).

Множесто А/В-тестов, проведённых по каждому из событий, не обнаружили статистически значимой разницы между группами. Т.е. изменение шрифтов во всём приложении на поведение пользователей не повлияло. Однако стоит учитывать, что вероятность ни разу не ошибиться при 16 тестах равна: (1-0.99)^16 = 0.85, это довольно высокий показатель.

