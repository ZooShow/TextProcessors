# TextProcessors
1. Создаем файл `touch first.txt`
2. `ctrl+c, ctrl+v` мой любимый стих (чутка переделан - спасибо THE RETUSES)
3. Создаем файл `touch second.txt`
4. `tail -n 40 first.txt | cat >  second.txt` - последние 40 строк скопированы
5. Создаем файл `touch third.txt`
6. `head -n 10 second.txt | cat > third.txt` - первые 10 строк скопированы
7. В третьем файле несколько местоимений "Я", заменим их на "Не я" `sed -r 's/Я/Не я/g' second.txt | grep 'Не я' | head -n 3 | cat >> third.txt`
8. Сортируем файл `sort third.txt | uniq -c` (если добавить в команду `| cat > third.txt` почему-то весь файл очищается, хотя без этого, на консольке все выводится нормально) ![пруф](https://github.com/ZooShow/TextProcessors/blob/main/proof.JPG)
