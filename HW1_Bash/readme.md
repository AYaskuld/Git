## Задание 1 ##  

**1) Посмотреть где я** 
```bash
pwd
```  
**2) Создать папку**  
```bash
mkdir
```  
**3) Зайти в папку**  
```bash
cd dirname
```  
**4) Создать 3 папки**  
```bash
mkdir qa1 qa2 qa3
```  
**5) Зайти в любоую папку**  
```bash
cd qa1
```  
**6) Создать 5 файлов (3 txt, 2 json)**  
```bash
touch Hello.txt Git.txt Bash.txt 1.json 2.json
```  
or  
```bash
cat > Hello.txt Git.txt Bash.txt 1.json 2.json
``` 
**7) Создать 3 папки(одна/в/другой/)**  
```bash
mkdir -p одна/в/другой/
```  
**8) Вывести список содержимого папки**  
```bash
ls
``` 
**9) Открыть любой txt файл**  
```bash
Nano Hello.txt
```
**10) Написать туда что-нибудь, любой текст**  
```bash
Hellow
my
name
is 
Artyom
123
``` 
**11) Cохранить и выйти**
```bash
^w; ^x
```  
**12) Выйти из папки на уровень выше**  
```bash
Cd ..
``` 
**—**  
**13) Переместить любые 2 файла, которые вы создали, в любую другую папку**  
```bash
mv qa1/Git.txt qa1/Bash.txt qa2
``` 
**14) Скопировать любые 2 файла, которые вы создали, в любую другую папку**  
```bash
cp qa1/Git.txt qa1/Bash.txt qa1/data
``` 
**15) Найти файл по имени**  
```bash
find -name *.txt
``` 
**16) Просмотреть содержимое в реальном времени (команда grep) изучите как она работает**  
Просмотр содержимого в реальном времени с поиском конкретного термина
```bash
tail -F 1.json | grep search_term
``` 
**17) вывести несколько первых строк из текстового файла**  
```bash
head -n3 qa1/Hello.txt
``` 
**18) вывести несколько последних строк из текстового файла**  
```bash
tail -n3 qa1/Hello.txt
``` 
**19) просмотреть содержимое длинного файла (команда less) изучите как она работает**  
```bash
less qa1/Hello.txt
```   
q - выход  
  
**20) вывести дату и время**  
```bash
date
``` 
## Задание 2 ##
**1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request**  
```bash
curl http://162.55.220.72:5005/terminal-hw-request
```   
``` bash 
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   283  100   283    0     0   3079      0 --:--:-- --:--:-- --:--:--  3179{
  "Intro": "Hello!! This is your the first response from server",
  "Tasks": {
    "Task_1": "Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)",
    "result": [
      "Your_String",
      "Your_number"
    ]
  }
}

```
Полученный ответ направил на следующее задание. Необходимо в URL добавить свое имя и возраст.
```bash
curl 'http://162.55.220.72:5005/get_method?name=Artyon&age=27'
``` 

       % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
    100    24  100    24    0     0    247      0 --:--:-- --:--:-- --:--:--   252[
      "Artyon",
     "27"
    ]

**2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13**  
1. Для выполнения этого задания я создал отдельную дерикторию "Byscrypt" в корневой папке. Bash чувствителен к регистру символов.  
2. Далее создал файл "myscrypt" и заполнил следующими строками:  
```bash
#!/bin/bash
#3) Зайти в папку
cd Byscrypt
#4) Создать 3 папки
mkdir qa1 qa2 qa3
#5) Зайти в папку
cd qa1
#6) Создать 5 файлов (3 txt, 2 json)
touch Hello.txt Git.txt Bash.txt 1.json 2.json
#7) Создать 3 папки
mkdir -p одна/в/другой/
#8) Вывести список содержимого папки
ls
#13) Переместить любые 2 файла, которые вы создали, в любую другую папку.
mv Git.txt Bash.txt ../qa2
```  
3. Запустил скрипт командой 
```bash
./myscrypt
```
