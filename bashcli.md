## Основны Bash CLI

Bash -терминал, командная строка, консоль. Ещё Bash - это скриптовый ЯП

### Терминал

Слвинуть вверх лог выполненных ранее команд
```shell
Ctrl+L
```
Очистить весь экран терминала
```shell
clear
```
```shell
reset
```
Получить историю всех ранее введённых команд
```shel
history
```
Выполнить команду по её порядковому №
```shell
!53
```
где 53 - это порядковый № команды из списка 'history'
```shell
!!
```
Перелистывание ранее введённых команд
'Стрелки вверх/вниз'

Дописывание команд и имён файлов/каталогов при помощи 'Tab'

Выйти из текущего терминала
```shell
exit
```

### Linux

Получить информацию по дистрибутиву
```shell
lsb_release -a
```
или красивей
```shell
fastfetch
```
или технические подробности
```shell
inxi -F
```
Системный монитор
```shell
htop
```
Получить t и CPU|GPU и скорость вращения вентиляторов(Fan)
```shell
sensors
```
Получить состояние оперативной памяти и подкачки (swap)
```shell
free -h
```
Получить имена текущих пользователей
```shell
w
```
Получить id текущего пользователя
```shell
id
```
Получить список групп, в которых числится текущий пользователь
```shell
groups
```


### Софт

Показать календарь
```shell
cal
```
Получить дату и время
```shell
date
```
Получить содержимое текстового файла
```shell
cat имя_файла
```
Отредактировать текстовый файл
```shell
nano имя_файла
```
Получить имя компьютера
```shell
hostname
```
Получить текущий ip компьютера
```shell
hostname -i
```
Информация по сети
```shell
ifconfig
```
или
```shell
ip -c a
```
Пинг адреса
```shell
ping 8.8.8.8
```
```shell
ping ya.ru
```
Чтобы выйти из бесконечного пинга, выполните "Ctrl+C"
 Выполнить пинг указанное количество раз
 ```shell
 ping -c 4 ya.ru
 ```
Получить информацию по указанному домену
```shell
whois ozon.ru
```
Получить список портов
```shell
netstat -an
```
Получить список портов
```shell
netstat -an
```
Получить маршруты
```shell
route
```


## Управление компьютером

Перезагрузка
```shell
reboot
```
или
```shell
sudo shutdown -r now
```
или
```shell
sudo systemctl reboot
```
Выключение
```shell
poweroff
```
```shell
sudo shutdown -p now
```
или
'''shell
sudo systemctl poweroff
```

### Файловые операции

Получить абсолютный путь к текущей дириктории
```shell
pwd
```

Получить содержимое текущей директории
```shell
ls
```

или получить подробное содержимое указанного каталога, включая скрытые файлы и папки
```shell
ll
```
Примеры скрытых файлов и папок: `.gitignore` и `.git`

или указанной папки
```shell
ll dir_name
```

Получить древовидную структуру текущей директории
```shell
tree
```

Создать новый пустой файл
```shell
touch newFile.txt
```

Правила именования каталогов и файлов:
1. Только по-английски
1. Без пробелов и спец.символов
1. Если имя файла или каталога состоит из нескольких англ.слов., то имя можно создать так: `firstOfall` или `first_of_all`
1. В имени файлов лучше всегда указывать расширение `fileName.txt`

> **Важно:** для программирования прописные и строчные буквы - это разные буквы. `w` и `W` - это разные буквы

Получить общие сведения о файле
```shell
file имя_файла
```
Получить подробные сведения о файле
```shell
stat имя_файла
```
Получить содержимое текстового файла
```shell
cat имя_файла
```
Отредактировать текстовый файл
```shell
nano имя_файла
```
Сохранить `Ctrl+S`, выйти `Ctrl+X`

или через **Micro**
```shell
micro file_name.txt
```
Сохранить по **Ctrl+S**, выйти по **Ctrl+Q**

Переименовать файл
```shell
mv old_name.txt new_name.txt
```
Создать пустой каталог
```shell
mkdir NewFolder
```
Переименовать указанный каталог
```shell
mv newFolder/ newDir
```
Скопировать файл в указанную папку
```shell
cp other_name.txt newDir/
```
Удалить файл
```shell
rm other_name.txt
```
Создать новый пустой файл
```shell
touch newFile.txt
```
Переместить файл
```shell
mv more_file.txt newDir/
```
Зайти в указанную папку
```shell
cd newDir
```
Выйти из текущей папки
```shell
cd ..
```
Вернуться в предыдушую папку
```shell
cd -
```
Удалить указанную папку
```shell
rm -rf newDir
```

Знаки:
- `\` - обратный слэш (бэкслэш) - признак каталога, Windows
- `/` - прямой слэш - признак каталога, Unix/Linux/Android/macOS,iOS,BSD:
- `|` - вертикальный слэш - признак разделения команд пользователя
- `~` - тильда, признак домашнего каталога текущего пользователя

### Работа с разными языками программирования (выполнять в Ubuntu WSL)

Создать файл скрипта
```shell
nano main.py
```
Текст скрипта
```python
print('Hello!')
```
Запустить программу
```shell
python3 main.py
```
Создать файл программы на C++
```shell
nano main.cpp
```
Текст программы
```shell
#include <iostream>
int main() {
    std::cout << "Hello!" << std::endl;
    return 0;
}
```
Скомпилировать программу
```shell
g++ main.cpp -o main.bin
```
или
```shell
clang++ main.cpp -o main.bin
```
Запустить программу
```shell
./main.bin
```
Получить зависимости от библиотек указанной программы
```shell
ldd main.bin
```
Получить время выполения скрипта или программы
```shell
time python3 main.py
```

### Конвейерная обработка файлов и каталогов

Создать сразу несколько пустых файлов
```shell
touch {1..3}.txt
```
Создать сразу несколько пустых папкок
```shell
mkdir folder{1..3}
```
Удалить сразу несколько файлов
```shell
rm {1..3}.txt
```
Удалить сразу несколько папок
```shell
rm -rf folder{1..3}
```
Создать сложную структуру проекта
```
project/
├── css/
├── js/
├── img/
│   └── ico/
├── fonts/
└── pages/
```
Одной командой
```shell
mkdir -p project/{css,js,img/ico,fonts,pages}
```

### Пасхалки

Матрица
```shell
cmatrix
```
Выйти из матрицы по `Q`

Поезд
```shell
sl
```
ещё поезд
```shell
sl -a
```
и ещё поезд
```shell
sl -l
```
и ещё
```shell
sl -F
```
Огонь
```shell
cacafire
```
Попугай
```shell
curl parrot.live
```
Бегущий человек
```shell
curl ascii.live/forrest
```
Поющий человек
```shell
curl ascii.live/can-you-hear-me
```
Аквариум
```shell
snap install asciiquarium && asciiquarium
```
или
```shell
docker run -it --rm macabees/asciiquarium
```
Выйти из аквариума по '**Q**'

Хакерский терминал
```shell
docker run --rm -it bcbcarl/hollywood
```
Остановить показ по `Ctrl+C` и выйти `exit`

Мнямка
```shell
nyancat
```
Дум
```shell
docker run --rm -it --shm-size=512m -p 6901:6901 -e VNC_PW=password kasmweb/doom:1.19.0
```
[После установки открыть в браузере этот адрес](https://localhost:6901/)

Логин: `kasm_user`
Пароль: `password`

***

### Ресурсы

- [Linux Cheat Sheet — шпаргалка по командам Linux](https://github.com/justxor/Linux-/)