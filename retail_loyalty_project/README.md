# retail_loyalty_project


## Исследование программы лояльности сети строительных магазинов (окончен)

### Цели
- проверить данные на наличие аномалий, выбросов и дубликатов;
- сравнить поведение покупателей вошедших в программу лояльности с остальными покупателями, по:
    - среднему количеству товаров в корзине;
    - средней сумме корзин;
    - RetentionRate;
    - LTV.
- провреить статистическую значимость различия по среднему количеству товаров и средней сумме корзины;
- классифицировать покупателей алгоритмами машинного обучения для выявления потенциально лояльных;
- провести кластеризацию для определения особенностей поведения лояльных покупателей.

### Инструменты
- **pandas**
    - read_csv, info, sample, head, nunique, describe(percentiles), value_counts, rename, astype, map(lambda x), drop_duplicates, copy, shape, query, reset_index, groupby, agg, sort_values, apply, dt, merge, drop, pivot_table, DataFrame, cumsum, to_list, corr, 
- **matplotlib**
    - title, xlabel, уlabel, figure, hist, show, xlim, legend
- **seaborn**
    - set, scatterplot, histplot, boxplot, heatmap, kdeplot
- **numpy**
    - polyfit, poly1d, timedelta64, 
- **scipy**
    - ttest_ind, pvalue, linkage, dendrogram
- **sklearn**
    - train_test_split, fit_transform, transform, fit, predict, StandardScaler, LogisticRegression, RandomForestClassifier, GradientBoostingClassifier, accuracy_score, precision_score, recall_score, f1_score, KMeans
    
### Выводы
**Без привязки вариантов стоимости товаров к дате, результаты исследования могли получиться ошибочными.**  
Среднее количество товаров в корзине лояльных покупателей меньше на: 25.9%  
Средняя сумма корзины лояльных покупателей меньше на: 23.5%  
Оба различия статистически значимы.  
**При этом, Retantion Rate лояльных покупателей на третий месяц - становится выше.**
**А с учётом ежемесячной платы, LTV покупателей программы лояльности выше.**  
Наилучший результат показала модель машинного обучения "Градиентный бустинг", но данных для обучения пока не хватает.
Для лояльных клиентов может быть характерно:
- меньше, как общее количество, так и количество типов товаров в корзине

**Рекомендую продолжить программу лояльности и посмотреть на динамику Retantion Rate и LTV**
### Используемые данные
Реальные данные сети строительных магазинов с 2016-12-01 по 2017-02-28.
