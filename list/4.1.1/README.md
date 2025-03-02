# Домашнее задание к занятию 4.1 Коллекции List
## Задача 1. Записная книга

### Описание
Мы уже делали записную книжку с описанием дел, но не сохраняли их в какую-то структуру данных. Списки дел можно хранить в 
массивах и списках. Массивы имеют фиксированную длину, и после того как массив создан, он не может расти или уменьшаться. 
ArrayList (одна из имплементаций списка) может менять свой размер во время исполнения программы, при этом не обязательно указывать размерность при создании объекта.
Кроме того, вы без проблем можете вставить новый элемент в середину коллекции, а также спокойно удалить элемент из любого места.
Поэтому очень удобно использовать List для ведения списка дел, ведь часто бывает, что нужно добавить какие-то дела в середине дня или же что-то удалить.

Необходимо реализовать программу, в которой пользователь вводит с консоли описание дел (одно дело — одна строка, затем Enter) в бесконечном цикле, пока не введет ключевое слово "end". Программа сохраняет все эти дела в списке "List" и после команды "end" выводит их в консоль.

### Функционал программы
1. Запрос списка задач/дел у пользователя;
2. Возможность добавить задачу в список;
2. Возможность удалить задачу из списка;
3. Возможность вывода всех задач.

### Пример
```
Выберите действие:
1. Добавить задачу
2. Вывести список задач
3. Удалить задачу
0. Выход
1 <enter>
Введите задачу для планирования:
Почитать про ArrayList

Выберите действие:
1. Добавить задачу
2. Вывести список задач
3. Удалить задачу
0. Выход
1 <enter>
Введите задачу для планирования:
Повторить примитивные типы данных

Выберите действие:
1. Добавить задачу
2. Вывести список задач
3. Удалить задачу
0. Выход
2 <enter>
Список задач:
1. Почитать про ArrayList
2. Повторить примитивные типы данных

Выберите действие:
1. Добавить задачу
2. Вывести список задач
3. Удалить задачу
0. Выход
0 <enter>
```

### Процесс реализации
1. Используя `Scanner scanner = new Scanner(System.in)` и `scanner.nextLine()`, в бесконечном цикле необходимо последовательно получить названия дел или слово `end`. 
Перед каждым запросом на ввод нужно выводить сообщение `System.out.println("Введите название задачи (для завершения введите end)")`, чтобы пользователь понимал, что ему вводить.

2. Добавьте проверку, равно ли введенное значение условию для выхода из цикла - строке `end`.

3. Если не введено слово `end`, то сохраните введенное значение в переменную task типа String `String task = scanner.nextLine()` и добавьте его в список `list`.

4. Если введено слово `end`, то используя цикл, выводим задачи в консоль вместе с их номерами.

### * Дополнительное задание: дополните программу выше функцией удаления. 

После вывода списка дел в консоль, программа дает пользователю возможность удалить из списка определенное дело по индексу. 
Это происходит в бесконечном цикле, пока пользователь не введет ключевое слово "Finish".

### Процесс реализации

1. Используя `Scanner scanner = new Scanner(System.in)` и `scanner.nextLine()` в бесконечном цикле, получите 
   индекс дела, которое необходимо удалить, и сохранить это значение в переменную `String input = scanner.nextLine()`. 

2. Добавьте проверку, равно ли введенное значение условию для выхода из цикла — строке `Finish`.

3. Используя метод ArrayList `remove(int index)`, удалите дело из списка. Обратите внимание, что необходимо будет перевести String в int.

4. Если введено слово `Finish`, то, используя цикл, выведите задачи в консоль вместе с индексом. Убедитесь, что дело корректно удалилось из списка и индексы были сдвинуты влево.
