# Terminal
---
## HW_1

### Linux terminal (GitBash) commands
1. Посмотреть где я     
```
pwd
```
    
2. Создать папку
```
mkdir test1
```

3. Зайти в папку
```
cd test1
```

4. Создать 3 папки
```
mkdir dir_1 dir_2 dir_3
```

5. Зайти в любую папку
```
cd dir_1
```

6. Создать 5 файлов (3 txt, 2 json)
```
touch 1.txt 2.txt 3.txt 1.json 2.json
```

7. Создать 3 папки
```
mkdir 1_1 1_2 1_3
```

8. Вывести список содержимого папки
```
ls
```

8. Открыть любой txt файл
```
vim 1.txt
```

9. Открыть любой txt файл
```
vim 1.txt
``` 

10. Написать туда что-нибудь, любой текст (см. пункт 9)
```
test test test 
test test test
``` 

11. Сохранить и выйти (см. пункт 9)
```
Esc :qw
``` 

12. Выйти из папки на уровень выше
```
cd ..
``` 

13. Переместить любые 2 файла, которые вы создали, в любую другую папку
```
mv 1.txt 2.txt 1_1
``` 

14. Cкопировать любые 2 файла, которые вы создали, в любую другую папку
```
cp 1.json 2.json 1_1
``` 

15. Найти файл по имени
```
find . -name "*.json"
``` 

16. Просмотреть содержимое в реальном времени (команда grep) изучите как она работает
```
grep "$" 1.txt
```

17. Вывести несколько первых строк из текстового файла
```
head -n 1 1.txt
```

18. Вывести несколько последних строк из текстового файла
```
tail -n 3 1.txt
```

19. Просмотреть содержимое длинного файла (команда less) изучите как она работает
```
less 1.txt
```

20. Вывести дату и время
```
date
```

Задание *
1) Отправить http запрос на сервер
```
curl "http://162.55.220.72:5005"
```

2) Написать скрипт, который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

```
cat >> myscript.sh
#!/bin/bash
func() {
       cd test1
       mkdir dir_1 dir_2 dir_3
       touch 1.txt 2.txt 3.txt 1.json 2.json
       mkdir 1_1 1_2 1_3
       echo $(ls)
}
func
move() {
        cd dir_1
	mv 1.txt 1_1/1.txt
	mv 2.txt 1_1/2.txt
}

Нажать CTRL + C

chmod +x ./myscript.sh
./myscript.sh
```

---
## HW_2
