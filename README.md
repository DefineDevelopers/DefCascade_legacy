# RUSSIAN DESCRIPTION
## Что это?
Маленький perl-скрипт, который нужен для работы с css-файлами.
## Конкретнее?
Вводится тип единицы измерения для замены на тот тип, который будет указан при вторичном вводе.  
На третьем этапе просят ввести соотношение первой единицы ко второй.  
## Использование:
```bash
perl main.pl <file_list>
```  
### Пример:
Есть файл **"style.css"**, в котором содержится следующая строка:
```html
min-width: 200px;
```
Вводим последовательно 3 значения:  
**px** -> как вариант, первая единица измерения;  
**vw** -> как вариант, второая единица измерения;  
**2.0** -> коэффициент (в дальнейшем "k". Значение может быть не только целым числом);  
**Внимание**: это будет применяться ко всем строкам файла.  
После окончания этапа ввода, в итоге, создаётся файл **"Dstyle.css"**, в котором предыдущая строка заменена на следующее:
```html
min-width: 400vw;
```
То есть, принцип следующий: **X<первая единица измерения> -->X*k<вторая единица измерения>**.  
Файл создаётся в той же директории, что и местоположение запущенного скрипта.
