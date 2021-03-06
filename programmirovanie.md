# Программирование

В заданиях на программирование лучше рассматривать код написанный на языке Python: у него проше структура, он менее строг к разного рода излишествам в виде точеек с запятой, допукает присвоение типа переменной "на лету" - в момент её использования в программе.

Про Python говорят, что это язык программирования с достаточно ясным и легко читаемым кодом. Это связано с тем, что в нем **сведены к минимуму вспомогательные элементы \(скобки, точка с запятой\)**, а **для разделения синтаксических конструкций** используются **отступы от начала строки**.

Это делает язык проще для освоения элементаных опраций.

#### **Совет**

> Решая задачу обязательно держите под рукой листочек, на котороый предварительно выпишите имена и значения всех переменных. Большинство задач дано с целью выяснить "_какое значение примет переменная \( какое значение будет выведено на экран\) после выполенния программы_" - поэтому после анализа кажддой строчки программы заносите на листочек новые значения переменных. Это поможет вам ориентироваться в работе предложенного кода.

Базовые алгоритмы

Есть три, и только три, программных алгоритма:

* линейный - выполенние команд подряд, друг за другом, ни одна команда не может быть выполнена раньше или позже назначенного ей срока;
* циклический - повторение **линейной** цепочки команд до тех пор, пока не будет выполнено условие прекращающее цикл;
* ветвления - выбор между **двумя** \( или **больше** \) альтернативными вариантами развития событий в зависимости от того, как сложатся условия на предыдущем этапе выполнения.

Именно на их основе строится всё программирование.

### Основные операторы языка

#### Обявление переменных и присваивание данных

В программе на языке Python связь между данными и переменными устанавливается с помощью знака =. Такая операция называется присваиванием. Например, выражениеsq = 4означает, что на объект \(данные\) в определенной области памяти ссылается имя sq и обращаться к ним теперь следует по этому имени.

![](/assets/Снимок экрана 2017-05-28 в 11.23.00.png)

Имена переменных могут быть любыми. Однако есть несколько общих правил их написания:

1. Желательно давать переменным осмысленные имена, говорящие о назначении данных, на которые они ссылаются.

2. Имя переменной не должно совпадать с командами языка \(зарезервированными ключевыми словами\).

3. Имя переменной должно начинаться с буквы или символа подчеркивания \(\_\).

Чтобы узнать значение, на которое ссылается переменная, находясь в режиме интерпретатора, достаточно ее вызвать \(написать имя и нажать Enter\).

#### Пример работы с переменными в интерактивном режиме:

```
>>>apples = 100
>>>eat_day = 5
>>>day = 7
>>>apples = apples - eat_day * day
>>>apples 
>>>65
```

### Типы данных

Каждая перменная имеет свой тип данных. Для школы достаточно знать лишь  некоторые.

1. **целые числа \(integer\) **– положительные и отрицательные целые числа, а также 0 \(например, _4, 687, -45, 0_\).
2. **числа с плавающей точкой \(float point\) **– дробные числа \(например, _1.45, -3.789654, 0.00453_\). Примечание: разделителем целой и дробной части служит **точка**, _а не запятая_.
3. **строки \(string\) **— набор символов, заключенных в кавычки \(например, _"ball", "What is your name?", 'dkfjUUv', '6589'_\). Примечание: кавычки в Python могут быть одинарными или двойными.

#### Изменение типа данных

В отличие от днекоторых других языков программирования, операции над данными \( переменными \) в некоторых случаях могут приводить к изменению их типа.

| Выражение | Результат выполнения |
| :--- | :--- |
| 1 + 0.65 | 1.6499999999999999 |
| "Hi, " + 15 | Oшибка |

Бываю случаи когда программа получает данные в виде строк, а оперировать должна числами \(или наоборот\). В таком случае используются специальные функции \(особые операторы\), позволяющие преобразовать один тип данных в другой. Так функция **int\(\)** преобразует переданную ей строку \(или число с плавающей точкой\) в целое, функция **str\(\)** преобразует переданный ей аргумент в строку, **float\(\)** - в дробное число.

| Выражение | Результат выполнения |
| :--- | :--- |
| int \("56"\) | 56 |
| int \(4.03\) | 4 |
| int \("comp 486"\) | Oшибка \( попытка преобразования строки в целое число \) |
| str \(56\) | '56' |
| str \(4.03\) | '4.03' |
| float \(56\) | 56.0 |
| float \("56"\) | 56.0 |

### Логические выражения

#### Логического выражения и логический тип данных

Часто в реальной жизни мы соглашаемся или отрицаем то или иное утверждение, событие, факт. Например, "Сумма чисел 3 и 5 больше 7" является правдивым утверждением, а "Сумма чисел 3 и 5 меньше 7" - ложным. Можно заметить, что с точки зрения логики подобные фразы предполагают только два результата: "Да" \(правда\) и "Нет" \(ложь\). Подобное используется в программировании: если результатом вычисления выражения может быть лишь истина или ложь, то такое выражение называется логическим.

У логических оперций может быть только два ответа:

"**Правда**" \( true, 1 \)

"**Ложь**" \( false, 0 \)

То, что значения можут рассматриваться как цифры 0 и 1, пожзоляет работать с Правдой и Ложью как с арифметическими величинами. Это полужило созданию нескольких разледов математики, в том числе и Математической логики, с её положениями ознакомтесь в [соотвествующем разделе этой книжки](/matematicheskaya-logika.md).

#### Логические операторы

Говоря на естественном языке \(например, русском\) мы обозначаем сравнение словами "равно", "больше", "меньше". В языках программирования используются специальные знаки, подобные тем, которые используются в математических выражениях: &gt; \(больше\), &lt; \(меньше\), &gt;= \(больше или равно\), &lt;= \(меньше или равно\).

Новыми для вас могут оказаться обозначение равенства: == \(два знака "равно"\); а также неравенства !=. Здесь следует обратить внимание на следующее: не путайте операцию присваивания, обозначаемую в языке Python одиночным знаком "равно", и операцию сравнения \(два знака "равно"\). Присваивание и сравнение — совершенно разные операции.

#### Примеры работы  с логическими выражениями на языке программирования Python

\(после \# написаны комментарии\):

```
x = 12 – 5 # это не логическая операция,
# а операция присваивания переменной x результата выражения 12 — 5
x == 4 # x равен 4
x == 7 # x равен 7
x != 7 # x не равен 7
x != 4 # x не равен 4
x > 5 # x больше 5
x < 5 # x меньше 5
x >= 6 # x больше или равен 6 x <= 6 # x меньше или равен 6
```

#### Ещё раз обратите внимание

**==** - это **сравнение**, а **не присваивание**, по русски это звучит "**Правда**, если _левая часть выражения **эквивалентна** правой_"

!= - это **обратная сравнению операция **\( _см. строку выше_ \), по русски это звучит "**Правда**, если _левая часть выражения **не эквивалентна** правой_"

### Сложные логические выражения

Логические выражения типаverymuch &gt;= 1023 является простым. Однако, на практике не редко используются более сложные. Может понадобиться получить ответа "Да" или "Нет" в зависимости от результата выполнения двух простых выражений. Например, "на улице идет снег или дождь", "переменная new больше 12 и меньше 20" и т.п.

В таких случаях используются специальные операторы, объединяющие два и более простых логических выражения. Широко используются два способа объединения: через, так называемые, логические **И \(and\)** и **ИЛИ \(or\)**.

**Чтобы получить истину \(True\)** при использовании оператора **and**, необходимо, чтобы результаты** обоих простых выражений, которые связывает данный оператор, были истинными**. Если **хотя бы в одном** случае результатом будет False\(ложь\), то и все сложное выражение будет ложным.

Чтобы получить истину \(True\) при использовании оператора **or**, необходимо, чтобы результаты **хотя бы одного простого выражения, входящего в состав сложного, был истинным**. В случае оператора **or** сложное выражение становится ложным лишь тогда, **когда ложны все составляющие его простые выражения**.

#### Примеры работы со сложными логическими выражениями на языке программирования Python

```
(после # написаны комментарии):
x =8
y = 13
x == 8 and y < 15 # x равен 8 и y меньше 15
x > 8 and y < 15 # x больше 8 и y меньше 15
x != 0 or y >15 # x не равен 0 или y меньше 15 x < 0 or y >15 # x меньше 0 или y меньше 15
```

### Цикл while

Циклы— это инструкции, выполняющие **одну и туже последовательность действий**, пока **действует заданное условие**.

В компьютерных программах наряду с **инструкциями ветвлениями** \( т.е. _выбором пути действия _\) также существуют **инструкции циклов** \( _повторения действия _\). Если бы инструкций цикла не существовало, пришлось бы много раз вставлять в программу один и тот же код подряд столько раз, сколько нужно выполнить одинаковую последовательность действий.

Универсальным организатором цикла в языке программирования Python \(как и во многих других языках\) является конструкция **while**. Слово "while" с английского языка переводится как "**пока**" \("**пока** _логическое выражение_ возвращает истину, **выполнять определенные операции**"\). Конструкцию **while** на языке Python можно описать следующей схемой:

![](/assets/Снимок экрана 2017-05-28 в 12.28.03.png)Эта схема _приблизительна_, т.к. логическое выражение в заголовке цикла** while** может быть более сложным, **а изменяться может переменная \(или выражение\) b**.

Может возникнуть вопрос: "_Зачем изменять a или b_?".

Когда выполнение программного кода **доходит до цикла while**, выполняется логическое выражение **в заголовке**, и, если было получено**True\(истина\)**, выполняются **вложенные выражения**. **После** поток выполнения программы снова **возвращается в заголовок цикла while**, и **снова проверяется условие**. Если условие никогда не будет ложным, то не будет причин остановки цикла и программазациклится. Чтобы этого не произошло, необходимо предусмотреть возможность **выхода из цикла** — ложность выражения в заголовке. Таким образом, _изменяя значение переменной в теле цикла, можно **довести логическое выражение до ложности**_.

![](/assets/Снимок экрана 2017-05-28 в 12.39.50.png)

Эту изменяемую переменную, которая используется в заголовке цикла **while**, обычно называют** счетчиком**. Как и всякой переменной ей можно давать произвольные имена, однако очень часто используют буквы i и j. Простейший цикл на языке программирования Python может выглядеть так:

Простой пример использования цикла

---

```
str1 = "+" # это простое привсваивание переменной строчки "+" для вывода на печать в каждом такте
i=0           # начальное значение счётчика
while i < 10: # проверка, может ли работать цикл: до тех пор пока переменная i меньше 10
    print (str1) # печатается "+"
    i=i+1 # а к счетчику прибавляется единичка, приближая цикл к финалу
```

---

Результатом выполнения скрипта приведенного выше является **вывод на экран десяти знаков + в столбик**

```
+
+
+
+
+
+
+
+
+
+
```

В последней строчке кода происходит **увеличение значения переменной i на единицу**, поэтому с каждым оборотом цикла ее значение увеличивается.  
Когда будет **достигнуто число 10**, логическое выражение **i &lt; 10 даст ложный результат**, выполнение тела цикла будет _**прекращено**_, а поток выполнения программы _перейдет на команды следующие **за всей конструкцией** цикла_.

Если увеличивать счетчик в теле цикла не на единицу, а на 2, то будет выведено **только пять знаков**, т.к цикл сделает лишь пять оборотов.

#### Более сложный пример с использованием цикла:

```
fib1 = 0 
fib2 = 1 
print (fib1) 
print (fib2) 
n = 10 
i=0

while i < n:

fib_sum = fib1 + fib2

    print (fib_sum) 
    fib1 = fib2 
    fib2 = fib_sum 
    i=i+1
```

Этот пример выводит **числа Фибоначчи**— ряд чисел, в котором каждое последующее число равно сумме двух предыдущих: **0, 1, 1, 2, 3, 5, 8, 13 и т.д**.

Скрипт выводит двенадцать членов ряда: два \(0 и 1\) выводятся вне цикла и десять выводятся в результате выполнения цикла.

#### Как это происходит?

Вводятся две переменные \(**fib1 **и **fib2**\), которым присваиваются начальные значения. Присваиваются значения переменной **n** и счетчику** i**, между которыми те или иные математические отношения формируют желаемое число витков цикла. Внутри цикла создается переменная **fib\_sum**, которой присваивается сумма двух предыдущих членов ряда, и ее же значение выводится на экран. Далее изменяются значения** fib1** и **fib2** \(_**первому** присваивается **второе**, а **второму** - **сумма**_\), а также **увеличивается значение счетчика**.

### Условный оператор. Инструкция if

Ход выполнения программы может быть **линейным**, т.е. таким, когда выражения выполняются, начиная с первого и заканчивая последним, по порядку, не пропуская ни одной строки кода. Но чаще бывает совсем не так. **При выполнении программного кода некоторые его участки могут быть пропущены**.

Чтобы лучше понять почему, проведем **аналогию с реальной жизнью**.

Допустим, **человек живет по расписанию** \(можно сказать, **расписание** — это своеобразный "линейный программный код", который следует выполнить\). В его расписании в 18.00 стоит поход в бассейн. Одним из **условий** посещения бассейна является **наличие в нем воды**, иначе должны выполняться **другие действия**. Человеку поступает информация, что **воду слили**, и бассейн не работает.  Вполне логично **отменить** свое занятие по плаванию и **заняться чем-то другим**.

Похожая нелинейность действий может быть предусмотрена и в компьютерной программе. Например, **часть кода должна выполняться лишь при определенном значении конкретной переменной.** Обычно в языках программирования используется приблизительно такая конструкция:

#### ![](/assets/Снимок экрана 2017-05-28 в 13.18.17.png)Пример ее реализации на языке программирования Python:

```
if numbig < 100: # если значение переменной numbig меньше 100, то ... 
c = a**b         # возвести значение переменной a в степень b,
                 # результат присвоить c.
```

Первая строка конструкции **if**— это заголовок, в котором **проверяется условие выполнения строк кода после двоеточия** \(_тела конструкции_\). В примере выше тело содержит **всего лишь одно выражение**, однако чаще их бывает куда больше.

В конструкции **if** код, который выполняется при соблюдении условия, должен **обязательно иметь отступ вправо**. Остальной код \(основная программа\) должен иметь** тот же отступ, что и слово **_**if**_.

Обычно отступ делается **с помощью клавиши Tab**.

![](/assets/Снимок экрана 2017-05-28 в 13.32.39.png)

Можно изобразить **блок-схему программы**, содержащей инструкцию** if**, в таком виде:![](/assets/Снимок экрана 2017-05-28 в 13.35.10.png)Встречается и **более сложная форма ветвления**: **if–else**. **Если** условие при инструкции** if** оказывается **ложным**, то **выполняется** блок кода при инструкции **else**.

#### Пример кода **с веткой else**

на языке программирования Python:

```
print "Привет"
tovar1 = 50
tovar2 = 32
if tovar1 + tovar2 > 99 :
    print "Сумма не достаточна" 
else:
    print "Чек оплачен" 
    print "Пока"
```

### Множественное ветвление

Логика выполняющейся программы **может быть сложнее, чем выбор одной из двух ветвей**.

Например, в зависимости от значения той или иной переменной, может выполняться одна из трех \(или более\) ветвей программы.

#### Как организовать множественное ветвление?

**Можно** использовать **несколько инструкций if**: **сначала** проверяется условное выражение в **первой инструкции if** \(_если оно возвращает истину, то будет выполняться вложенный **в нее** блок кода_\), затем **во второй инструкции if **и т.д.

**Однако** при таком подходе **проверка последующих инструкций** будет **продолжаться** даже тогда, когда первое условие было истинным, и блок кода при данной ветке был выполнен. **Проверка последующих условий** в этом случае оказывается **бессмысленной**.

Такую проблему **можно** решить **с помощью вложенных конструкций if-else**. Однако при этом часто появляется **проблема правильной трактовки кода**: непонятно, **к какому if относится else** \(хотя в Python такая путаница не возможна из-за обязательных отступов\).

С другой стороны, в ряде языков программирования, в том числе и Python, предусмотрено **специальное расширение инструкции if**, позволяющее **направить поток выполнения программы по одной из множества ветвей**. Данная расширенная инструкция, **помимо необязательной части else**, содержит **ряд ветвей elif** \(_сокращение от "else if" - "**еще если**"_\) и выглядит примерно так, как показано на блок-схеме.

**Частей elif может быть сколь угодно** много \(в пределах разумного, конечно\).![](/assets/Снимок экрана 2017-05-28 в 13.57.11.png)**В отличии** от использования **множества одиночных инструкций if**, инструкция **if-elif - else** **прекращает просмотр последующих ветвей**, как только логическое выражение в текущей ветке **вернет true**.

Например, если выражение при** if** \(_первая ветка_\) будет **истинным**, то **после выполнения вложенного блока** выражений, программа **вернется в основную ветку**.

#### Примеры скриптов с использованием инструкции if-elif-else

на языке программирования Python:

```
x = -10

if x > 0: 
    print 1
elif x < 0:
    print -1
else:
    print 0

result = "no result" 
num1 = 3

if num1 == 0: 
    result = 0
elif num1==1: 
    result = 1
elif num1==2: 
    result = 2
elif num1==3: 
    result = 3
elif num1==4: 
    result = 4
elif num1==5: 
    result = 5
else:
    print "Error"
print result
```

В какой момент **прекратиться выполнение инструкции if-elif-else** в примерах выше. **При каком значении** переменной могла сработать **ветка else**?

### Ввод данных с клавиатуры

**Выводом на экран** \(_и не только_\) в языке программирования Python занимается функция **print\(\).**

**Данные в программу** можно "_заложить_" в процессе **разработки программы**.

Однако такая программа **всегда будет обрабатывать одни и те же данные** и **возвращать один и тот же результат**.

**Чаще требуется другое** —** программа должна обрабатывать разные  данные**, которые **поступают в нее из внешних источников:** **файлов или клавиатуры**. Программа **обменивается информацией** с внешней средой: выводит и получает данные в процессе выполнения, **не замыкается сама на себе**.

**Ввод данных с клавиатуры** в программу \(_начиная с версии Python 3.0_\) осуществляется **с помощью функции input\(\)**. Когда данная функция выполняется, то **поток выполнения программы останавливается в ожидании данных**, которые пользователь **должен** ввести с помощью клавиатуры. **После ввода данных и нажатия Enter**, функция** input\(\)** **завершает** **свое** выполнение и возвращает результат в виде **строки символов**, _введенных_ пользователем.

В **интерактивном** режиме **терминала** ввод данных **с клавиатуры** выглядит так:

```
>>> input() 
1234
'1234'
>>> input() 
Hello World! 
'Hello World!' 
>>>
```

Когда выполняющаяся программа **предлагает пользователю что-либо ввести**, то пользователь может не понять, что от него хотят. Надо **как-то сообщить**, **ввод каких данных ожидает программа**.

Функция **input\(\)** может принимать **необязательный аргумент-приглашение** строкового типа; при выполнении функции сообщение будет **появляться на экране и информировать** человека о запрашиваемых **от него **данных.

```
>>> input("Введите номер карты: ") 
Введите номер карты: 98765 
'98765'
>>> input('Input your name: ')
Input your name: Sasha 
'Sasha'
>>>
```

Данные **возвращаются в виде строки**, даже если было введено число. В **более ранних версиях Python** были **две** встроенные функции, позволяющие получать данные с клавиатуры: **raw\_input\(\)**, **возвращающая** в программу **строку** и **input\(\)**, **возвращающая число**. Начиная **с версии Python 3.0**, если требуется **получить число**, то результат выполнения функции** input\(\)** изменяют с помощью **функций int\(\)** \( возвращение **целого** числа \) или **float\(\)** \( **дробного** числа \).

```
>>> input('Введите число: ')
Введите число: 10
'10'
>>> int(input('Введите число: ')) 
Введите число: 10
10
>>> float(input('Введите число: ')) 
Введите число: 10
10.0
>>>
```

**В реальном программировании **результат, возвращаемый функцией **input\(\)**,  **присваивают переменной** для **дальнейшего использования** в программе.

```
>>> userName = input('Как твоё имя? ') # обявляется переменная userName
Как твоё имя? Маша # в с клавиатуры вводится строковое значение переменной userName
>>> exp = input('3*34 = ') # объявляется переменная exp
3*34 = 102 # с клавиатуры вводится значение переменной exp
>>> exp = int(exp) + 21 # переменная exp преобразуется из строки в число и склалывается с 21
>>> userName # что теперь лежит в переменной userName?
'Маша'
>>> exp # что теперь лежит в переменной exp?
123 
>>>
```

### Строки как последовательности символов

**Строки** уже упоминались в **типах данных**.

**Строка**— это сложный тип данных, представляющий собой **последовательность символов**.

**Строки** в языке программирования Python могут **заключаться** как в **одиночные**, так и **двойные кавычки**. Однако, начало и конец строки **должны обрамляться одинаковым типом кавычек**.

Функция **len\(\)**, позволяет **измерить длину строки**. Результатом является **число, показывающее количество символов в строке.**

Для строк существуют операции **конкатенации** \( + - _слияния строк _\) и **дублирования **\( \* - множественного **повторения** \).

```
len('It is a long string') # измеряем длину строки( без кавычек!!! )
19
>>> '!!!' + ' Hello World ' + '!!!' # сливаем вместе три строки заключённые в кавычки
'!!! Hello World !!!'
>>> '-' * 20 # повторяем 20 раз тире
'--------------------'
>>>
```

В последовательностях важен **порядок символов**, у **каждого** символа в строке есть **уникальный порядковый номер** —**индекс**. Можно о**бращаться к конкретному символу** в строке и **извлекать** его с помощью **оператора индексирования**, который представляет собой **квадратные скобки с номером символа в них**.

```
>>> 'morning, afternoon, night'[1] # обратите внимание, что нумерация начинается с "0"
'o' # поэтому под интексом "1" будет буква "о", а не "m"
>>> tday = 'morning, afternoon, night' # строчка заностится в переменную tday
>>> tday[4] # а вот уже из нее извлекается
'i' # "i" имеющая индекс "4"
>>>
```

Когда требуется **извлечь первый символ**, то **оператор индексирования** выглядит так: **\[0\]**.

**Можно** извлекать символы, **начиная отсчет с конца**. В этом случае отсчет начинается с** -1** \( "**минус первый символ**" - **последний** символ\).

```
>>> tday_ru = 'утро, день, ночь'
>>> tday_ru[0] 
'у'
>>> tday_ru[-1]
'ь'
>>> tday_ru[-3] 
'о'
>>>
```

Можно извлекать из строки **не один символ**, а несколько, т.е. получать **срез** \(_подстроку_\).  
Оператор извлечения среза из строки выглядит так: **\[X:Y\]**. **X** – это **индекс начала среза**, а **Y** – его **окончания**; причем **символ с номером Y в срез уже не входит **\(!!!\). Если **отсутствует первый индекс**, то срез берется **от начала до второго индекса**; при **отсутствии второго индекса**, срез берется **от первого индекса до конца строки**.

```
>>> tday = 'morning, afternoon, night'
>>> tday[0:7]
'morning'
>>> tday[9:-7]
'afternoon'
>>> tday[-5:]
'night'
>>>
```

Кроме того, можно **извлекать символы не подряд**, а **через** определенное количество символов. В таком случае оператор индексирования выглядит так: **\[X:Y:Z\]**; **Z** – это **шаг**, через который осуществляется **выбор элементов**.

```
>>> str4 = "Full Ball Fill Pack Ring"
>>> str4[::5]
'FBFPR'
>>> str4[0:15:2]
'Fl alFl '
>>>
```

### Списки — изменяемые последовательности

**Списки** в языке программирования Python, **как и строки**, являются _упорядоченными **последовательностями**_.

**В отличии от строк**, _списки_ состоят **не из символов, а из различных объектов** \(_значений, данных_\), и заключаются **не в кавычки**, а в** квадратные скобки \[ \]**. **Объекты отделяются друг от друга** с помощью **запятой**.

Списки **могут** состоять из **различных объектов**: _чисел, строк и даже **других** списков_. В последнем случае, списки называют **вложенными**.

```
[23, 656, -20, 67, -45] # список целых чисел
[4.15, 5.93, 6.45, 9.3, 10.0, 11.6] # список из дробных чисел
["Katy", "Sergei", "Oleg", "Dasha"] # список из строк
["Москва", "Титова", 12, 148] # смешанный список
[[0, 0, 0], [0, 0, 1], [0, 1, 0]] # список, состоящий из списков
```

Как и над строками **над списками** можно выполнять операции **соединения** \( + \) и **повторения \( ;\*\)**:

```
>>> [45, -12, 'april'] + [21, 48.5, 33] # сливаем два списка
[45, -12, 'april', 21, 48.5, 33]
>>> [[0,0],[0,1],[1,1]] * 2
 # удваиваем имеющийся список списков
[[0, 0], [0, 1], [1, 1], [0, 0], [0, 1], [1, 1]]
>>>
```

По **аналогии** с символами строк, можно получать **доступ** к объектам списка **по их индексам**, **извлекать срезы**, измерять **длину списка**:

```
>>> li = ['a','b','c','d','e','f'] 
>>> len(li)
6
>>> li[0]
'a'
>>> li[4]
'e'
>>> li[0:3]
['a', 'b', 'c']
>>> li[3:]
['d', 'e', 'f']
>>>
```

В отличии от строк, **списки** — это **изменяемые последовательности**. Если представить **строку как объект** в оперативной памяти компьютера,  то когда над ней выполняются **операции конкатенации и повторения**, то **это строка не меняется**, а в результате операции **создается другая строка в другом месте памяти**. В строку **нельзя добавить новый символ или удалить существующий**, не создав при этом **новой строки**.

Со списком дело обстоит иначе. При выполнении операций **новые** списки могут **не создаваться**, **а изменяться **непосредственно **оригинал**. Из списков можно **удалять элементы**, **добавлять новые**. При этом следует помнить, **многое зависит от того, как вы распоряжаетесь переменными**. Бывают ситуации, когда списки **все-таки** копируются. Например, результат операции **присваивается другой переменной**.

Символ в строке изменить **нельзя**, элемент списка — **можно**:

```
>>> mystr = 'abrakadabra' # определяем строковую переменную и даем ей значение 'abrakadabra'
>>> mylist = ['ab','ra','ka','da','bra'] # определяем список и хаполнчем его слогами
>>> mystr[3] = '0' # пробуем заменить символ с индексом "3" на "0"
Traceback (most recent call last): # получаем от программы сообещение об ошибке
 File "<pyshell#11>", line 1, in <module> mystr[3] = '0' 
  TypeError: 'str' object does not support item assignment 
>>>mylist[1] = 'ro' # пробуем заменить в списке слог с индексом "1" на "ro"
>>>mylist
['ab', 'ro', 'ka', 'da', 'bra'] # и это нам удаётся
>>>
```

В **списке** можно **заменить целый срез**:

```
>>> mylist[0:2] = [10,20]
>>> mylist
[10, 20, 'ka', 'da', 'bra'] 
>>>
```

Более сложная ситуация:

```
>>> alist = mylist[0:2] + [100,'it is ',200] + mylist[2:] # новый список
>>> a2list = mylist # создается вторая ссылка-переменная на первый список 
>>> alist
[10, 20, 100, 'it is ', 200, 'ka', 'da', 'bra']
>>> a2list
[10, 20, 'ka', 'da', 'bra']
>>>a2list[0] = '!!!' # изменяем список
>>>a2list
['!!!', 20, 'ka', 'da', 'bra']
>>> mylist # обе переменные связаны с одним списком
['!!!', 20, 'ka', 'da', 'bra']
>>>
```

### Введение в словари

Одним из **сложных типов данных** \(наряду со **строками** и **списками**\) в языке программирования Python являются словари.

**Словарь** - это **изменяемый** \(как **список**\) **неупорядоченный** \(в _отличие от **строк** и **списков**_\) набор **пар** "_ключ:значение_".

Чтобы представление о словаре стало более понятным, можно провести **аналогию с обычным словарем**, например, **англо-русским**. На **каждое** _английское_ слово в таком словаре **есть** _русское слово-перевод_: **cat** – **кошка**, **dog** – **собака**, **table** – **стол** и т.д. Если англо-русский словарь _**описывать** с помощью **Python**_, то **английские слова будут ключами**, а **русские — их значениями**:

```
{'cat':'кошка', 'dog':'собака', 'bird':'птица', 'mouse':'мышь'}
```

Обратите внимание на **фигурные скобки**, именно с их помощью определяется словарь.

**Синтаксис словаря** на _**Python**_ можно описать такой схемой:![](/assets/Снимок экрана 2017-05-28 в 16.22.23.png)Если **создать словарь** в интерпретаторе Python, то **после нажатия Enter** можно наблюдать, что последовательность **вывода** пар "ключ:значение" **не совпадает с тем, как было введено**:

```
>>> {'cat':'кошка', 'dog':'собака', 'bird':'птица', 'mouse':'мышь'}
{'bird': 'птица', 'mouse': 'мышь', 'dog': 'собака', 'cat': 'кошка'}
>>>
```

Дело в том, что **в словаре абсолютно не важен порядок пар**, и интерпретатор выводит их в **случайном** порядке.

Тогда как же получить** доступ к определенному элементу**, если индексация не возможна в принципе? Ответ: в словаре **доступ** к значениям **осуществляется по ключам**, которые заключаются в **квадратные** скобки \(по а**налогии с индексами строк и списков**\).

```
>>> dic ={'cat':'кошка','dog':'собака','bird':'птица','mouse':'мышь'} >>> dic['cat']
'кошка'
>>> dic['bird']
'птица'
>>>
```

**Словари**, как и списки, являются **изменяемым типом данных**: можно _изменять_, _добавлять_ и _удалять_ элементы \(_пары "ключ:значение"_\).

**Изначально** словарь можно **создать пустым** \(_например, d = {}_\) и лишь **потом заполнить его элементами**. _Добавление и изменение_ имеет одинаковый синтаксис: **словарь\[ключ\] = значение**. **Ключ** может быть как **уже существующим** \(тогда происходит **изменение значения**\), так и **новым** \(происходит **добавление элемента словаря**\).

**Удаление** элемента словаря осуществляется с помощью функции **del\(\)**.

```
>>> dic ={'cat':'кошка','dog':'собака','bird':'птица','mouse':'мышь'} 
>>> dic['elephant'] = 'бегемот' # добавление "бегемота" 
>>> dic['fox'] = 'лиса' # добавление "лисы"
>>> dic
{'fox': 'лиса', 'dog': 'собака', 'cat': 'кошка', 'elephant': 'бегемот', 'mouse': 'мышь', 'bird': 'птица'}
>>> dic['elephant'] = 'слон' # изменение "бегемота" на "слона"
>>> del(dic['bird']) # удаление "птицы"
>>> dic
{'fox': 'лиса', 'dog': 'собака', 'cat': 'кошка', 'elephant': 'слон', 'mouse': 'мышь'}
>>>
```

**Тип данных ключей и значений** словарей **не обязательно должны быть строками**. Значения словарей могут быть более сложными \(содержать **структуры данных**, например,** другие словари** или **списки**\).

```
>>> d = {1:'one',2:'two',3:'three'}
>>> d
{1: 'one', 2: 'two', 3: 'three'}
>>> d = {10:[3,2,8], 100:[1,10,5], 1000:[23,1,5]} 
>>> d
{1000: [23, 1, 5], 10: [3, 2, 8], 100: [1, 10, 5]} >>> d = {1.1:2, 1.2:0, 1.3:8}
>>> d
{1.3: 8, 1.2: 0, 1.1: 2}
>>> d = {1.1:2, 10:'apple', 'box':100}
>>> d
{'box': 100, 10: 'apple', 1.1: 2}
>>>
```

Словари — это широко используемый тип данных языка Python. Для работы с ними существует ряд **встроенных функций**.

### Цикл for в языке программирования Python

**Цикл for** представляет собой **цикл обхода заданного множества элементов** \(символов **строки**, объектов **списка** или **словаря**\) и **выполнения в своем теле различных операций** над ними.

Например, если имеется **список чисел**, и необходимо **увеличить значение каждого элемента на две единицы**, то можно **перебрать список** с помощью цикла **for**, выполнив над **каждым** его элементом соответствующее действие.

```
>>> spisok = [0,10,20,30,40,50,60,70,80,90]
>>> i = 0
>>> for element in spisok:
    spisok[i] = element + 2
    i=i+1
>>> spisok
[2, 12, 22, 32, 42, 52, 62, 72, 82, 92]
>>>
```

В примере **переменная i **нужна для того, чтобы **записать изменившееся значение элемента в список**. В ней хранится значение **индекса** очередного **элемента** списка. В то время, как переменная element связывается со значением очередного элемента данных. В заголовке цикла **for** происходит обращение **очередному элементу** списка. В теле цикла элементу **с индексом i** присваивается **сумма значения текущего** \(_обрабатываемого_\) элемента и **двойки**.

Далее **индекс увеличивается на единицу**, а поток выполнения программы **переходит** снова** в заголовок цикла for**, где происходит **обращение к следующему элементу** списка.

Когда **все** элементы **обработаны** цикл **for заканчивает свою работу**. **Отсутствие** очередного элемента является условием завершения работы цикла **for** \(для сравнения: в цикле **while** **условием** **завершения** служит результат **false** логического выражения в заголовке\). Еще один момент: если счетчик **не увеличивать** на единицу \(выражение **i = i + 1**\), то не смотря на то, что все элементы списка будут обработаны, результат **все время будет присваиваться первому элементу списка** \(с индексом **0**\).

С таким же успехом перебирать можно и строки, если **не пытаться их при этом изменять**:

```
>>> stroka = "привет"
>>> for bukva in stroka:
    print(bukva, end=' * ')
п * р * и * в * е * т * 
>>>
```

Цикл **for** используется и для работы **со словарями**:

```
>>> d = {1:'one',2:'two',3:'three',4:'four'}
>>> for key in d:
d[key] = d[key] + '!'
>>> d
{1: 'one!', 2: 'two!', 3: 'three!', 4: 'four!'} >>>
```

Цикл **for** является важным инструментом при обработки структур данных.

Также следует **запомнить**, что **цикл for в Питоне особенный**. Он **не является аналогом циклов for во многих других языках программирования **\(!!!\), где представляет собой, так называемый, _цикл со счетчиком_.

### Функции в программировании

**Функции** в программировании это **изолированный блок кода**, обращение к которому в процессе выполнения программы может быть **многократным**. В первую очередь **такие блоки нужны** чтобы **сократить** объем кода:  **вынести часто повторяющиеся выражения** в отдельный блок и, затем, по мере надобности, обращаться к нему.

Представим себе следующую ситуацию. Требуется написать скрипт, который при выполнении должен **три раза запрашивать у пользователя разные данные**, но выполнять с ними **одни и те же действия**.

```
a = int(input('Введите первое число: '))
b = int(input('Введите второе число: '))
if a > b:
    print(a-b)
else:
    print(b-a)
c = int(input('Введите первое число: '))
d = int(input('Введите второе число: '))
if c > d:
    print(c-d)
else:
    print(d-c)
e = int(input('Введите первое число: '))
f = int(input('Введите второе число: '))
if e > f:
    print(e-f)
else:
    print(f-e)
```

Данная программа находит **модуль разницы двух чисел**. Очевидно, что такая запись исходного кода не рациональна: получаются **три почти одинаковых блока кода**.

Почему бы не использовать цикл **while** для организации **повторения**?

```
i=0
while i < 3:
    a = int(input('Введите первое число: '))
    b = int(input('Введите второе число: '))
    if a > b:
        print(a-b)
    else:
        print(b-a)
    i=i+1
```

В этом случае есть один нюанс. Вводимые пользователем данные **всегда** связываются с переменными **a** и **b**. При **каждом** витке цикла **прежние данные утрачиваются**. Что же делать, если **все шесть чисел**, введенных пользователем **надо сохранить** для дальнейшего использования в программе?

Рассмотрим решение этой задачи **с использованием функции**.

```
def diff():# задаём имя функции
    m = int(input('Введите первое число: ')) # обычный ввод целого числа с клавиатуры
    n = int(input('Введите второе число: ')) 
    if m > n: # выбор ветви исполенния
        print(m-n)
    else:
        print(n-m)
    return m,n # 'return' - это выдача ( её ещё называют "возврат" ) переменных и их значений 
a,b = diff() # функция в коде вызывается три раза и каждый раз m и n переприсваиваются новым переменным 
c,d = diff()# за пределы функции
e,f = diff()
```

**def**– это инструкция \(команда\) языка программирования Python, позволяющая **создавать функцию **\( обособленный блок кода \). **diff **– это **имя функции**, которое \(так же как и имена переменных\) может быть _**почти**_** любым**, но **желательно** **осмысленным**. После **в скобках** перечисляются **параметры функции**. Если их **нет**, то скобки остаются **пустыми**.

Далее идет **двоеточие**, обозначающее **окончание заголовка** функции \(аналогично с _условиями_ и _циклами_\). После заголовка **с новой строки и с отступом** следуют **выражения тела функции**.

В **конце тела** функции присутствует инструкция **return** \( **может** и не быть \), которая **возвращает значение\(я\)** в **основную ветку программы**. В данном случае, **если бы в функции не было** инструкции **return**, то в основную программу ничего бы не возвращалось, и переменным **a** и** b** \(**c** и **d**, а также **e** и **f**\) числовые значения **не присваивались**.

После функции идет **основная ветка программы**, в которой переменным **попарно присваивается результат выполнения вызываемой функции diff**.

В иных ситуациях, когда функция не возвращает значений, ее вызов не связывается с переменной.

**Выражения тела функции выполняются лишь тогда**, когда она **вызывается** в **основной** ветке программы. Так, например, **если функция присутствует в исходном коде, но нигде не вызывается в нем, то содержащиеся в ней инструкции не будут выполнены ни разу **\( !!! \).

### Параметры и аргументы функций. Локальные и глобальные переменные

**Параметры** и **аргументы** функций

Функция используется для обработки данных, **полученных из внешней для нее среды** \(из _основной ветки программы_\). Данные **передаются** функции при ее вызове **в скобках и называются аргументами**. Однако, чтобы функция могла **"взять" передаваемые ей данные**, необходимо при ее создании описать параметры \(в скобках **после** имени функции\), представляющие собой переменные.

![](/assets/Снимок экрана 2017-05-28 в 22.20.14.png)Когда функция **вызывается**, конкретные аргументы **подставляются вместо параметров-переменных**. Почти **всегда** количество аргументов и параметров **должно совпадать** \( хотя **можно** запрограммировать **переменное количество** принимаемых аргументов \).

В качестве **аргументов** могут выступать как **непосредственно значения**, так и **переменные, ссылающиеся на них**.

### Локальные и глобальные переменные

Если записать в IDLE \( официальная интегрированная среда разработки на Python \) приведенную ниже функцию, и затем попробовать **вывести значения переменных**, то обнаружится, что **некоторые из них почему-то не существуют**:

```
>>> def mathem(a,b): 
    a = a/2
    b = b+10
    print(a+b)
>>> num1 = 100
>>> num2 = 12
>>> mathem(num1,num2) 
72.0
>>> num1
100
>>> num2
12
>>> a
Traceback (most recent call last):
 File "<pyshell#10>", line 1, in <module> 
 a
NameError: name 'a' is not defined 
>>> b
Traceback (most recent call last):
 File "<pyshell#11>", line 1, in <module> 
 b
NameError: name 'b' is not defined
>>>
```

Переменные **num1** и **num2** не изменили своих первоначальных значений. Дело в том, что **в функцию передаются копии значений**. **Прежние** значения из основной ветки программы остались по **прежнему связанны с их переменными**.

А вот **переменных a** и **b** оказывается **нет и в помине** \(ошибка "_name 'b' is not defined_" переводится как "_переменная b не определена_"\). Эти переменные **существуют лишь в момент выполнения функции** и называются **локальными**. В противовес им, переменные **num1** и **num2** видны не только **во внешней ветке**, но и **внутри функции**:

```
>>>def mathem2():
    print(num1+num2)
>>>mathem2()
112
>>>
```

Переменные, **определенные в основной ветке программы**, являются **глобальными**.

