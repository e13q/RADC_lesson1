# Угадай строку, guess.py

Игра в "Угадай строку" с 6 попытками. 
Игра заканчивается, если пользователь отгадал все буквы или ввёл 6 неправильных.

## Как установить

Для работы скрипта необходим установленный Python3.
Используйте `pip` (или `pip3`, если при вызове происходит конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```
Также, необходимо создать/загрузить файл data\\sowpods.txt со списком слов.

## Функции
### play()

Функция описывает игру в "Угадай строку" с 6 попытками. 
По загаданной строке создается аналогичная строка, в которой буквы заменены символом '-'.
После чего в консоль выводятся загаданая строка с подмененными на '-' символами и у пользователя запрашивается символ.
Если символ является буквой, то он запоминается и, если буква угадана, замещает прочерк, либо, если буква не угадана, добавляется в словарь неправильных букв.
Если пользователь вводит корректный ранее вводимый символ, то пользователь получит информацию о том, что символ ранее вводился.
Игра заканчивается оповещением в консоли, если пользователь отгадал все буквы или ввёл 6 неправильных.

### print_game()

Функция отображает информацию по игре:

* Выводит некорректно выбранные пользователем буквы, которых нет в слове
* Отображает правильно выбранную букву, учитывая позицию в слове
* Отображает итоговое слово с прочерками вместо букв, исключая пробелы.

Пример работы функции:

![image](https://github.com/e13q/RADC_lesson1/assets/110967581/e4ec4d22-a4f5-4aa1-b8ff-4ec48d9e4312)

### get_letter()

Функция проверяет длинну вводимой строки (не больше 1), содержится-ли вводимый символ в ascii (является-ли буквой) и вводился-ли символ ранее.
В случае некорректных символов/длинны/повторного ввода в консоль - выводится информация об ошибке ввода.

### get_rand_word()

Функция открывает файл sowpods.txt со списком слов и выбирает случайную подстроку, переводя все символы в нижний регистр.

## Цели проекта

Данный код написан в образовательных целях, как часть онлайн курса для веб-разработчиков на платформе [dvmn.org](https://dvmn.org/).
