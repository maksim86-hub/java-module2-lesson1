**Строки** в Java представляют собой последовательности символов и являются объектами класса `String`. Они позволяют легко выполнять различные операции, такие как сравнение, извлечение подстрок, поиск и замена символов. В Java строки неизменяемы (immutable), что означает, что после их создания нельзя изменить содержимое. Ниже рассмотрим основные методы и операции для работы со строками.

#### 1. Создание строк
Строки могут быть созданы с помощью литералов или конструктора класса `String`. Литералы создаются непосредственно в коде, а конструктор позволяет создать строку из массива символов или другой строки.

**Пример:**
```java
String str1 = "Hello, World!"; // Создание строки с помощью литерала
String str2 = new String("Java Programming"); // Создание строки с помощью конструктора
```

<hr>

#### 2. Длина строки **[length()]**
Метод `length()` возвращает количество символов в строке, что позволяет узнать, сколько символов она содержит.

**Пример:**
```java
String str = "Hello";
int length = str.length(); // length равно 5
```

<hr>

#### 3. Конкатенация строк **[concat()]**
Метод `concat()` объединяет две строки, создавая новую строку. Также можно использовать оператор `+` для конкатенации.

**Пример:**
```java
String str1 = "Hello, ";
String str2 = "World!";
String result = str1.concat(str2); // result равно "Hello, World!"
```

<hr>

#### 4. Извлечение подстроки **[substring()]**
Метод `substring(int beginIndex, int endIndex)` позволяет извлекать часть строки. Он принимает начальный и конечный индексы и возвращает подстроку.

**Пример:**
```java
String str = "Hello, World!";
String sub = str.substring(7, 12); // sub равно "World"
```

<hr>

#### 5. Поиск символа **[indexOf()]**
Метод `indexOf(char ch)` возвращает индекс первого вхождения символа в строке. Если символ не найден, возвращается -1.

**Пример:**
```java
String str = "Hello, World!";
int index = str.indexOf('o'); // index равно 4
```

<hr>

#### 6. Замена символов **[replace()]**
Метод `replace(CharSequence oldChar, CharSequence newChar)` заменяет старые символы на новые в строке.

**Пример:**
```java
String str = "Java Programming";
String replaced = str.replace("Java", "Python"); // replaced равно "Python Programming"
```

<hr>

#### 7. Преобразование регистра **[toUpperCase(), toLowerCase()]**
Методы `toUpperCase()` и `toLowerCase()` изменяют регистр строки на верхний или нижний соответственно.

**Пример:**
```java
String str = "Hello";
String upper = str.toUpperCase(); // upper равно "HELLO"
String lower = str.toLowerCase(); // lower равно "hello"
```

<hr>

#### 8. Проверка на равенство **[equals()]**
Метод `equals(Object anObject)` проверяет, равны ли две строки.

**Пример:**
```java
String str1 = "Hello";
String str2 = "Hello";
boolean isEqual = str1.equals(str2); // isEqual равно true
```

<hr>

#### 9. Форматирование строки **[String.format()]**
Метод `String.format(String format, Object... args)` позволяет создавать отформатированные строки, используя различные параметры.

**Пример:**
```java
String name = "Alice";
int age = 30;
String formatted = String.format("Имя: %s, Возраст: %d", name, age); // formatted равно "Имя: Alice, Возраст: 30"
```

<hr>

#### 10. Разделение строки **[split()]**
Метод `split(String regex)` разбивает строку на подстроки на основе заданного регулярного выражения и возвращает массив строк.

**Пример:**
```java
String str = "Java,Python,C++,JavaScript";
String[] languages = str.split(","); // Разделение строки по запятой
// languages равно ["Java", "Python", "C++", "JavaScript"]
```

<hr>

#### Выполните следующий код:

```java
public class StringDemo {
    public static void main(String[] args) {
        // 1. Создание строк
        String str1 = "Hello, World!";
        String str2 = new String("Java Programming");
        System.out.println("Строка 1: " + str1);
        System.out.println("Строка 2: " + str2);

        // 2. Длина строки
        System.out.println("\nДлина строки 1: " + str1.length()); // 13

        // 3. Конкатенация строк
        String concatenated = str1.concat(" " + str2);
        System.out.println("Конкатенированная строка: " + concatenated);

        // 4. Извлечение подстроки
        String substring = str1.substring(7, 12);
        System.out.println("Извлеченная подстрока: " + substring); // "World"

        // 5. Поиск символа
        int index = str2.indexOf('a');
        System.out.println("Индекс первого 'a' в строке 2: " + index); // 1

        // 6. Замена символов
        String replaced = str2.replace("Java", "Python");
        System.out.println("Строка после замены: " + replaced); // "Python Programming"

        // 7. Преобразование регистра
        String upperCase = str1.toUpperCase();
        System.out.println("Строка в верхнем регистре: " + upperCase); // "HELLO, WORLD!"
        String lowerCase = str2.toLowerCase();
        System.out.println("Строка в нижнем регистре: " + lowerCase); // "java programming"

        // 8. Проверка на равенство
        boolean isEqual = str1.equals("Hello, World!");
        System.out.println("Строка 1 равна 'Hello, World!': " + isEqual); // true

        // 9. Форматирование строки
        String formatted = String.format("Строка 1: %s, Длина: %d", str1, str1.length());
        System.out.println(formatted); // "Строка 1: Hello, World!, Длина: 13"

        // 10. Разделение строки
        String str3 = "Java,Python,C++,JavaScript";
        String[] languages = str3.split(","); // Разделение строки по запятой
        System.out.println("Языки программирования:");
        for (String language : languages) {
            System.out.println(language); // Вывод: Java, Python, C++, JavaScript
        }
    }
}
```