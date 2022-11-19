# Работа с модулями и пакетами

Модуль — это скрипт на языке Python (файл с расширением `*.py`).

Пакет — каталог с файлом `__init__.py` и несколькими модулями Python.

Файл `__init__.py` является заголовком пакета и содержит перечень идентификаторов, которые становятся доступными при импорте пакета.

Ключевое слово `import` используется для подключения модулей и пакетов.

Стандартные пакеты находятся в подкаталоге `Lib`, внутри каталога, где установлен Python

Пакеты сторонних разработчиков находятся в подкаталоге `Lib\site-packages`, внутри каталога, где установлен Python

Подключение модуля или пакета происходит с помощью ключевых слов `import` и `from`:

```python
import math2
# Переменные и функции из модуля/пакета доступны как math2.PI

import math2 as m
# Переменные и функции из модуля/пакета доступны как m.PI

from math2 import a_plus_b
# Из модуля/пакета импортируется только переменная/функция c
# именем a_plus_b и к ней можно обращаться непосредственно, не
# указывая имени модуля/пакета

from math2 import *
# Из модуля/пакета импортируются все переменные/функции и к ним 
# можно обращаться непосредственно, не указывая имени 
# модуля/пакета
```

Импорт всех имен (`from math2 import *`) не рекомендуется использовать, т.к. он может приводить к замещению имен переменных или функций в текущем контексте.

Каждая функция, класс, модуль или пакет могут содержать строку документации. Строка документации оформляется следующим образом:

```python
def a_plus_b(a, b):
    """
    Эта функция складывает два числа
    """
    return a + b
```
