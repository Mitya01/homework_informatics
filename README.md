# Лабораторная работа по теме "Планировщик задач cron"

## Разминка (ее в отчет включать не нужно!)

Перед выполнением основного задания, выполните следующее простое задание, чтобы ознакомиться с основами работы cron:

### Шаги выполнения:

Cоздайте файл с именем `hello.sh`.
Вставьте следующий код:
```bash
#!/bin/bash
OUTPUT_FILE="/path/to/your/output.txt"
echo "Hello, world! The current date and time is $(date)" >> "$OUTPUT_FILE"
```
Замените `/path/to/your/output.txt` на путь к файлу, в который вы хотите записывать вывод скрипта.
Сохраните файл и закройте редактор.

Сделайте скрипт исполняемым:
```bash
chmod +x hello.sh
```
Эта команда устанавливает разрешения на выполнение для файла `hello.sh`.

Настройте crontab для автоматического выполнения скрипта:
   - Откройте файл crontab для редактирования:
     ```bash
     crontab -e
     ```
   - Добавьте следующую строку в конец файла, чтобы запускать скрипт каждую минуту:
     ```
     * * * * * /path/to/hello.sh
     ```
   - Сохраните изменения и выйдите из редактора.

Убедитесь, что задание добавлено, выполнив команду:
```bash
crontab -l
```

Проверьте выполнение задания:
   - Подождите одну минуту и проверьте указанный файл (`output.tx`). Вы должны увидеть строку с сообщением "Hello, world!" и текущей датой и временем.

## Задание лабораторной работы

На основе изученного материала лабораторной работы, напишите скрипт, который будет выполнять резервное копирование указанной директории в заданное время. Для резервного копирования используйте встроеннный архиватор tar.

## Что вам нужно знать, чтобы успешно защитить работу:

- Как использовать планировщик задач cron и его синтаксис.
- Как проверять выполнение задач cron и управлять ими.

## Дополнительные источники

1. [Информация про cron](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#CRONREF)
2. [Документация Ubuntu по cron](https://help.ubuntu.ru/wiki/cron)
3. [Архиватор tar](https://losst.pro/komanda-tar-v-linux#sintaksis-komandy-tar)
