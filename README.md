# DjangoD2
Создание моделей для будущего приложения NewsPortal.
В проекте лежит пять моделей:

Author - модель содержит объекты всех авторов, связана с встроенной моделью User.
Category - модель содержит доступные категории статей ("главные новости", "политика", "новости спорта", "новости искусства").
Post - модель содержит созданные статьи и новости, соответствующие разным категориям.
PostCategory - модель содержит связь между статьёй и её категориями.
Comment - модель содержит комментарии к статьям, которые могут оставлять как сами авторы, так и обычные пользователи.
Пользователи могут ставить оценки комментариям и постам с помощью методов like() и dislike() в соответствующих моделях. В соответствии с этими оценками формируется финальный рейтинг авторов - методом update_rating() модели Author.

Последовательность команд в Django Shell, необходимых для заполнения базы данных, задокументирована в файле Список команд.txt.


Пока что благодаря свойствам рейтинг не может стать меньше нуля - но возможно будет лучше убрать эту настройку, раз пользователь может поставить как "лайк", так и "дизлайк". Тогда у самых непопулярных текстов и мнений будет отрицательный рейтинг(но это не точно)
