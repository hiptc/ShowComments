# ShowComments 
Представляю вашему внимаю ShowComments для DLE 9.x - 10.x. С помощью этого модуля вы сможете вывести последние комментарии в любом месте сайта в любом tpl файле. 

***

# Установка :
* Скопировать содержимое папки **upload** в корень сайта, предварительно поменять название шаблона сайта на своё.
* Открыть **main.tpl** перед закрывающим тегом HEAD прописать: `<link media="screen" href="{THEME}/comm/style.css" type="text/css" rel="stylesheet" />`
* В нужное место вставить строку: `{include file="engine/modules/comm.php"}`

***

# Параметры фильтров :
* max_comm - максимальное кол-во выводимых комментариев (принимает число)
* max_text - максимальное кол-во символов при выводе комментария (принимает число)
* max_title - максимальное кол-во символов при выводе заголовка новости (принимает число)
* stop_category - из каких категорий не выводить (принимает числа через запятую или дефис пример 1,4-5,7)
* from_category - из каких категорий выводить (принимает числа через запятую или дефис пример 1,4-5,7)
* stop_id - исключаем комментарии по id новостей (принимает числа через запятую или дефис пример 1,4-5,7)
* from_id - выводит комментарии только из этих новостей (принимает числа через запятую или дефис пример 1,4-5,7)
* avatar - выводит только комментарии авторов которые имеют загруженный аватар (принимает 1)
* news - выводит только комментарии авторов которые имеют новости (принимает 1)
* news_user - выводит комментарии авторов которые имеют кол-во новостей больше чем (принимает число)
* comm - выводит комментарии авторов которые имеют кол-во комментариев больше чем (принимает число)
* fav - выводит только комментарии авторов которые имеют закладки (принимает 1)
* fullname - выводит только комментарии авторов которые заполнили полное имя (принимает 1)
* land - выводит только комментарии авторов которые заполнили место жительства (принимает 1)
* rating - выводит только комментарии у которых рейтинг больше чем (принимает число)
* nxf - выводит комментарии только из тех новостях которые имеют доп поле(я) с заполненным(и) значением(ями)(принимает значения name|value^name1|value1 (name - название доп поля на латинице | value - значение доп поля)
* uxf - выводит комментарии только тех пользователей у которых доп поле(я) с заполненным(и) значением(ями) (принимает значения name|value^name1|value1 (name - название доп поля на латинице | value - значение доп поля)
* ncomm - выводит комментарии только из тех новостей которые имеют кол-во комментариев больше чем (принимает число)
* fixed - выводит только комментарии из тех новостей которые зафиксированы (принимает 1)
* tags - выводит только комментарии из тех новостей которые имеют теги (принимает слова через запятые : музыка,гранж,гражднаская оборона)
* read - выводит только комментарии из тех новостей которые имеют просмотров больше чем (принимает число)
* nrating - выводит только комментарии из тех новостей которые имеют рейтинг больше чем (принимает число)

***

# Использования фильтров :
* Для того что бы как то их применить нужно к строке дописать : `{include file="engine/modules/comm.php?max_comm=15"}`
* а потом дописывать через `&`
* Пример : `{include file="engine/modules/comm.php?max_comm=15&fullname=1&rating=4"}`

Этот код выведет в блоке 15 комментариев при условии того что у всех комментаторов заполнено Полное имя и рейтинг их комментария больше 4
