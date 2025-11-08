# MachineLearning
2025-2026

It's the analyzer of films. 

First a ball we **import the libraries**, which we will work with (**import pandas as pd**). Than we get **first 5 lines** from table (**movies_df.head()**). After it, we get all **information by groups** about this table, as the **number columns (24)** (**movies_df.info()**). By the next line (**movies_df.describe()**) we gen a **little bit more information** about it. 
Now, after we **know enough about this information**, we can **start work with it**. More exacly, **separeit to groops**, by line (**movies_df.isnull().sum()**) we do it. For example, the sum of **original_language** is **11**. From this table, we can find **empty boxes**, we **can't have** them. So we need **fill them**, (**movies_df["homepage"].fillna("with out link",inplace=True)**). We here fill the boxes **in column "homepage", with "without link"**.
Now we can **delete all empty boxes** by line (**movies_df.dropna(inplace=True)**).
But, on this stage I want **add one more column**, **separet** information about **data on two column**, (**movies_df["release_year"] = pd.to_datetime(movies_df["release_date"]).dt.year**). Here we **take the year from all dates.**
Perfect work. We can **check the information**. For example, **get the number, how many films and with "genres"**, (**genre_counts = movies_df["genres"].value_counts()**). We get the **35 Comedies**.


Это анализатор фильмов.

Сначала мы **импортируем библиотеки**, с которыми будем работать (**import pandas as pd**). Затем получаем **первые 5 строк** из таблицы (**movies_df.head()**). После этого получаем всю **информацию по группам** об этой таблице, например, **количество столбцов (24)** (**movies_df.info()**). В следующей строке (**movies_df.describe()**) мы генерируем **немного больше информации** о ней.

Теперь, когда мы **узнаем достаточно об этой информации**, мы можем **начать с ней работать**. Точнее, **разделяем её на группы**, построчно (**movies_df.isnull().sum()**). Например, сумма **original_language** равна **11**. В этой таблице мы находим **пустые поля**, которых у нас **не может быть**. Поэтому нам нужно **заполнить их** (**movies_df["homepage"].fillna("with out link",inplace=True)**). Здесь мы заполняем поля **в столбце "homepage", указав "without link"**.

Теперь мы можем **удалить все пустые поля** построчно (**movies_df.dropna(inplace=True)**).

Но на этом этапе я хочу **добавить ещё один столбец**, **разделить** информацию о **данных по двум столбцам** (**movies_df["release_year"] = pd.to_datetime(movies_df["release_date"]).dt.year**). Здесь мы **берём год из всех дат.**
Отличная работа. Мы можем **проверить информацию**. Например, **получите количество фильмов с указанием «жанров»** (**genre_counts = movies_df["genres"].value_counts()**). Мы получим **35 комедий**.
