## Логирование
**logStatementsQty = 0** во всех классах, кроме **Cookbook.java**, что означает отсутствие логирования в течении работы приложения
#### Решение: 
Добавить больше логов, особенно в контроллерах и моделях.
## Неиспользованные методы и переменные
В коде присутствуют не использованные методы и переменные: **Cookbook.java** - 2 метода (**loadIngridients, loadRecipe**), **Recipe.java** - 1 метод (**getIngredientList**) и 1 переменная (**previewImage**). 
#### Решение: 
Удалить неиспользованные сущности
## Низкие показатели связности (TCC, LCOM*)
Класс **Controller.java TCC = 0.464, LCOM\* = 0.71**; **Cookbook.java TCC = 0.571, LCOM\* = 0.67**, что говорит о слабой связанности методов внутри класса.
#### Решение: 
Убедиться, что все методы класса связаны с его основной функциональностью. В противном случае, можно выделить методы в отдельные классы.
## Высокий CBO (Coupling Between Objects)
У класса **Controller.java CBO = 12**, а у **Cookbook.java CBO = 1**, что может означать либо слишком сильную зависимость (**Controller**), либо наоборот, слабую связанность (**Cookbook**). Сильная связанность затрудняет повторное использование кода и усложняет тестирование. 
#### Решение: 
Разделение ответственности (Controller может быть слишком перегружен зависимостями). Стоит выделить части функционала в отдельные сервисы.
## Высокая когнитивная сложность
У класса **Controller WMC=10, RFC = 19, LOC = 61** y **Cookbook WMC = 16, RFC = 10, LOC=61**, то есть высокое количество вызовов/методов внутри класса, степень ветвления, что увеличивает сложность поддержания кода, ухудшает читаемость.
#### Решение:
Вынести часть методов в отдельные сущности и хранить их внутри классов.
## Отсутствие JavaDoc
Во всех классах отсутствует комментарии к сущностям. Метрика hasJavaDoc = false
#### Решение:
Добавить комментарии + JavaDoc

