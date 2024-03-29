# russian-symbols-cpp-fix
Дамы и господа, мы
готовы предоставить вам спасение нашей любимой кириллицы на c++!

Мы переделали базовые операторы ввода-вывода (cout, cin).
Теперь они более адаптированы к русским буквам.


# Как использовать
 0. Прежде всего удостоверяемся, что мы НЕ используем setlocale и подобные вещи. Они мешают работе библиотеки.
 1. Подключаем файл в проект
 2. Подключаем заголовочный файл в ваш основной:
    `#include "russian_fix.h"`
 3. Радуемся!


## Пример
Всё достаточно просто, как можно заметить. Необходимо лишь подключить инклюд.
В данном примере std::cout сразу же поглощает "неподготовленную" строку, автоматически трансформируя её.
Плюс, cin так же и работает.
```cpp
#include <iostream>
#include "russian_fix.h"


int main()
{
    std::string test;

    std::cout << "Русские символы в консоли, товарищи!\nВведите текст в консоли: ";

    std::cin >> test;
    std::cout << "\n" << test;
    return 0;

    /*    ВЫВОД ИЗ КОНСОЛИ    */

    /*  
        Русские символы в консоли, товарищи!
        Введите текст в консоли: тест тест тест
        тест тест тест
    */
}
```
----
Так же всё это дело совместимо с \<fstream\>. Пример - ниже.
```cpp
#include <iostream>
#include <fstream>
#include "russian_fix.h"

void UnitTest();

int main()
{
	UnitTest();
	return 0;
}


void UnitTest()
{
	// cin
	std::string str;
	std::cin >> str;

	// cout
	std::cout << str << "ТЕЕЕСТ";

	// fstream
	std::ofstream stream = std::ofstream();
	stream.open("test.txt");
	stream << str;
	stream.close();


}
```



## Авторство
**ImRibka** и **Nao**

"*[Чтобы накачаться за два дня, надо всего лишь...](https://youtu.be/MVIBf3cnTf0)*" **by Nao**

"*лол, люблю плюсы за то, что если тыкать указатели-адреса в рандомные места, то это многое меняет. Даже чинит проблемы*" **by ImRibka**
