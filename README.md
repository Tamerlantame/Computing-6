# Computing-6
being developed   | completed but not delivered   | all passed
:------: | :------:| :------:
❌      | ❌✅     | ✅
## ✅Task 1 
Для СЛАУ с некоторой матрицей A:
- вычислить числа обусловленности
- поварьировав матрицу и правую часть (например, на 10^(−2) – 10^(−10)), вычислить |x − ̃x|
- посмотреть, есть ли корреляция между величинами чисел обусловленности и погрешностью решения

### Result
- Произведены вычисления чисел обусловленности
- вычислена |x − ̃x| для вариаций матрицы (10^(−1) – 10^(−10))
- Определено: число обусловленности характеризует насколько велика будет погрешность решения при произвольном ненулевом b

## ✅Task 2
 - Реализовать метод решения СЛАУ, на выбор: LU-разложение или метод квадратногокорня. Для матриц A, L, U вычислить числа обусловленности (см. задание 1).Протестировать на разных матрицах: хорошо обусловленных, [очень] плохообусловленных.
 - Для нескольких плохо обусловленных матриц (например, для матриц Гильберта разного,больше 15, порядка) реализовать метод регуляризации:
 - - параметрαварьироватьвпределахот 10^(−12) до 10^(−1)
 - - для каждого конкретного значения α найти числа обусловленности (матриц A + αE) и норму погрешности получившегося решения
 - - понять, какоезначение α=α~ в каждом конкретном случае кажется наилучшим.
 - Наилучшее α можно:
 - - находить из предположений, что точным решением является вектор x0=(1, 1,..., 1)T
 - - находить из предположений, что точным решением является случайный вектор x0.
## ❌✅Task 3
- Реализовать метод решения СЛАУ, на выбор: метод вращений или метод отражений.
- Вычислить числа обусловленности.
- Протестировать на тех же матрицах, что использовались в задании 2; сравнить.
### Result
- реализован метод вращений
- Получены cond
- При сравнении выявлено, что при достаточно малых числах обусловденности QR разложение скорее всего даст тот же результат, что и LU
## ❌Task 4
- Реализовать решение СЛАУ двумя итерационными методами:
методом простой итерации + методом Зейделя или методом релаксации.
- Сравнить количество итераций.
- Находить решения с разной точностью (т.е. варьировать ε, до достижения которого
проводятся итерации). Может быть между ε и количеством итераций k есть зависимость?
Примечание: поскольку релаксационные методы используют более “свежую” информацию о сделанных
преобразованиях, то обычно они сходятся быстрее метода простой итерации.
Протестировать работу методов на плохо обусловленных матрицах — например, на
примере из методички А.Н.Пакулиной и на матрице Гильберта (см. задание 1).
- Если есть возможность — протестировать работу методов на симметричных с диагональным преобладанием
разреженных матрицах большого порядка (больше 200).
- Реализация метода релаксации с тестированием на больших разреженных матрицах дает дополнительный “плюсик”.
## ❌Task 5
Реализовать для нахождения максимального по модулю собственного числа и
соответствующего собственного вектора матрицы степенной метод и метод скалярных
произведений.
- Вычисления проводить до достижения точности ε.
- Варьируя ε, скажем, от 10−2 до 10−5, изучить зависимость количества итераций от ε.
- Сравнить количество итераций в методах (при каждом фиксированном ε).
## ❌Task 5.1
### Part 1. 
Реализовать для нахождения минимального (или минимального по модулю)
собственного числа и соответствующего собственного вектора матрицы степенной метод
и метод скалярных произведений.
Вычисления проводить до достижения точности ε.
Варьируя ε, скажем, от 10−2 до 10−5, изучить зависимость количества итераций от ε.
Сравнить количество итераций в методах (при каждом фиксированном ε).
### Part 2 (исследовательская).
Вычислив круги Гершгорина, взять произвольное начальное
приближение из объединения кругов (например, середину) и методом обратных итераций
со сдвигом попробовать найти какое-нибудь “среднее” с.ч.
## ❌Task 6
Реализовать метод Якоби поиска всех собственных чисел. Использовать две какие-либо
стратегии выбора обнуляемого элемента.
Вычисления проводить до достижения точности ε.
Варьируя ε, скажем, от 10−2 до 10−5, изучить зависимость количества итераций от ε.
Обязательно протестировать на матрице Гильберта порядка >5.
Выводить количество итераций.
По теореме Гершгорина определить область, в которую должны попадать с.ч.
матрицы. Проверить, действительно ли найденные значения в область попали.
## ❌Task 7
Реализовать решение ОДУ сеточным методом.
- Уравнения с граничными условиями для тестирования можно взять в методичке
А.Н.Пакулиной, часть 2, стр. 11 и далее.
- Можно построить уравнение самостоятельно, взяв известное u(x ). (и тут сразу будет
ясно, к какому ответу нужно прийти)
- Начинать вычисления с грубой сетки (примерно 10 интервалов); измельчать сетку и
уточнять по Ричардсону. В идеале — до момента выхода на ошибки округления.
- Отследить, какая точность (например, от 10−2 до 10−6) достигнута при каком шаге
сетки.
- Выводить полученное приближение. Можно на картинке.
- Доп.задание на 10 баллов: реализовать метод стрельбы. Сравнить результат с сеточным
методом
## ❌Task 8
Реализовать один из проекционных методов: метод Ритца или метод Галеркина.
Условия можно взять в [5].
Сравнить решения при разных N (либо графически, либо выводить значения решений на
достоточно частой сетке).
Т.Е. (СПбГУ) 10 марта 2022 40 / 42

