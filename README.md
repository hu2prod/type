# type
There was some repeatable code I wrote 2-3 times. Let's make module one time and forever.

 * Модуль представляет абстракцию "тип данных"
 * Бывают скалярные типы `int`, `bool`, `string`
 * Бывают контейнерные типы `array<int>`, `hash<int>`, `function<int,int>`
   * Функция возвращает свой первый тип, и принимает в качестве аргумента все остальные типы
 * Бывают структурные типы `struct{x: int, y: int}`
   * Это пример структуры из 2 полей типа `int` с именами `x` и `y`
 * Особый случай `void`. Он скалярный, но переменной этого типа быть не может. Это оборначение, что функция не возвращает никакого значения `function<void>`
# Как использовать
 * `new Type 'int'`
   * прим. заведите себе сразу удобный alias `type = (t)-> new Type t`
 * `t1.cmp(t2)` сравнить два типа
 * `"my type is #{t1}"` у него есть toString(), потому он нормально вставляется в интерполяцию строк
