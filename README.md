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
ls -la
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

1. Сделать папку dir_1
```
mkdir dir_1
```

2. Зайти в папку dir_1
```
cd dir_1
```

3. Создать папку inner_dir_1
```
mkdir  inner_dir_1
```

4. Посмотреть где ты находишься
```
pwd
```

5. Находясь в папке dir_1 , создать пустой текстовый файл tf_1.txt
```
touch tf_1.txt
```

6. Находясь в папке dir_1 , через команду cat создать текстовый файл tf_2.txt со следующими строками:
- the first 1
- the second 2
- the third 3
```
cat > tf_2.txt
the first 1
the second 2
the third 3
```

7. Зайти в папку inner_dir_1
```
cd inner_dir_1
```

8. Через cat сделать текстовый файл tf_3.txt  c любыми строками
```
cat > tf_3.txt
13243535436
w3536346
46wewtwrfhfh
```

9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2”
```
cat >> tf_3.txt
the second 2
```

10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2”
```
cat >> tf_3.txt
the sec 2
```

11. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3”
```
cat >> tf_2.txt
the sec 3
```

12. Через cat добавить в текстовый файл tf_3.txt строку “the SeCoNd 2”
```
cat >> tf_3.txt
the SeCoNd 2
```

13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2”
```
cat >> tf_2.txt
the seConD 2
```

14. Сделать текстовый файл tf_4.txt , в котором будет 15 строк
```
seq 15 | cat > tf_4.txt
```

15. Сделать текстовый файл tF_5.txt , в котором будет 13 строк
```
seq 13 | cat > tF_5.txt

16. Вывести список всех файлов в папке
```
ls -la
```

17. Выйти из папки inner_dir_1
```
cd ..
```

18. Вывести содержимое файла tf_3.txt в терминал
```
cat inner_dir_1/tf_3.txt
13243535436
w3536346
46wewtwrfhfh
the second 2
the sec 2
the SeCoNd 2
```

19. Найти путь к файлу tf_4.txt
```
find $(pwd) -name tf_4.txt
/c/Users/anils/dir_1/inner_dir_1/tf_4.txt
```

20. Отчистить файл tf_4.txt от содержимого без удаления самого файла
```
cat > tf_4.txt
```

21. Найти путь к файлам, у которых есть  “tf” в названии
```
find $(pwd) -name "*tf*"
/c/Users/anils/dir_1/inner_dir_1/tf_2.txt
/c/Users/anils/dir_1/inner_dir_1/tf_3.txt
/c/Users/anils/dir_1/inner_dir_1/tf_4.txt
/c/Users/anils/dir_1/tf_1.txt
/c/Users/anils/dir_1/tf_2.txt
/c/Users/anils/dir_1/tf_4.txt
```

22. Найти путь к файлам, у которых есть  “tf” в названии и буквы в любом регистре
```
find $(pwd) -iname "*tf*"
/c/Users/anils/dir_1/inner_dir_1/tf_2.txt
/c/Users/anils/dir_1/inner_dir_1/tf_3.txt
/c/Users/anils/dir_1/inner_dir_1/tf_4.txt
/c/Users/anils/dir_1/inner_dir_1/tF_5.txt
/c/Users/anils/dir_1/tf_1.txt
/c/Users/anils/dir_1/tf_2.txt
/c/Users/anils/dir_1/tf_4.txt
```

23. Найти строки в файлах, где есть комбинация букв “sec” в текущей папке
```
grep sec *
```

24.
