Комиты:

1. Выгрузить конфигурацию из базы данных (инструкция ниже).
2. Командой git status вывести новые и измененные файлы.
3. Командой git add добавить новые файлы.
4. Если есть измененные файлы в папке etc, восстановить командой git checkout -- имя файла.
5. Командой git commit -a -m "вменяемое имя коммита" закомитить.
6. Открыть в браузере /write_from_db.php для восстановления состояния папки etc.

Пулреквесты:

1. Запушить все коммиты на гит командой: git push.
2. Проверить по гитхабу конфликты с мастером.
3. Если есть конфликты, смержить с мастером, и исправить соответствующие файлы.
4. Злить на тестовый сервер. Проверить работоспособность. Проверить отсутствие ошибок в логах.
5. При наличии ошибок исправить и вернуться к пункту 1.
6. Отправить коммит в пулреквест (если не отправлен) и пометить пулреквест лейблом "Ready for review".

Выгрузка конфигурации базы данных:

1. Подключится к контейнеру: docker exec -ti hobby bash
2. Перейти в нужную папку: cd /var/www/xcom-hobby.ru/htdocs/bin/ConfigManager
3. Выгрузить конфигурацию командой: php write.php
4. Отсоединиться от контейнера командой: exit
