# russian-symbols-cpp-fix
 Заменяет базовые **cout, cin** на адаптированные к русским символам. Имеет функцию **r** для трансформации строки в русскую.

Дамы и господа, мы
готовы предоставить вам спасение нашей любимой кириллицы на c++!

Мы переделали базовые операторы ввода-вывода (cout, cin).
Теперь они более адаптированы к русским буквам.

Так же была добавлена функция для трансформации неприспособленной строки, в строку с понятными символами

# Как использовать
 1. Подключаем файл в проект
 2. Подключаем заголовочный файл в ваш основной:
    `#include "russian_fix.h"`
 3. Радуемся!

## Пример
Всё достаточно просто, как можно заметить. Необходимо лишь подключить инклюд.
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
}
```


Функция r() возвращает переформатированную строку, с которой уже можно и работать
```cpp
#include <iostream>
#include "russian_fix.h"


int main()
{
    std::string test = r("Йоу, плесень, как кости кинуть на гроустрит?");

    std::cout << test;

    return 0;
}
```



### Авторство
**ImRibka** и **Nao**

"*Путешествие в тысячу Ли начинается с одного шага*" © Лао-цзы **by Nao**

"*лол, люблю плюсы за то, что если тыкать указатели-адреса в рандомные места, то это многое меняет. Даже чинит проблемы*" © ImRibka **by ImRibka**