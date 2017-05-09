Cpp часть автоматического тестировщика стратегий игры реверси,
для [бонусного задания](https://docs.google.com/document/d/1jqrUPjPN5uFB7aOBuW464JNkXq3mCxUuhhbh31tNN7I/edit)
продвинутого потока (2 курс, четвёртый семестр, 2017).

# Содание стратегии для отправки на сервер

1. Доска - массив 8x8, нумерация с левого верхнего угла с нуля. Черному цвету
соответствует 1 на доске и номер игрока 1. Белому - 2 на доске и
номер игрока 2. Изначально в клетках (3, 3) и (4, 4) стоят белые фишки,
в клетках (3, 4) и (4, 3) - черные. В поле currentPlayer класса Reversi
лежит номер игрока, ход за которого надо сделать.
2. Ваша стратегия должна реализовывать класс Reversi из файла
package/Reversi.h. Пример базовой реализации лежит там же, нужно просто
ее изменить.
3. Компиляция происходит с помощью cmake с конфигурацией из CMakeLists.txt.
Менять ее в процессе отправки нельзя, а значит нужно соблюдать следующие
правила:

   * Ваш код должен находиться либо в файлах Reversi.h, Reversi.cpp, либо
   в новых .h файлах (без пары .cpp, так как файл с реализацией не будет
   добавлен в CMakeLists.txt).
   * В силу особенностей линковки, все функции, реализованные в .h файлах,
    должны быть явно объявлены как inline.
4. На сервер нужно отправлять все файлы из папки package, которые вы изменили,
а так же все новые файлы.