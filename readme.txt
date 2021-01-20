Создание бота в телеграмм для отправки сообщений через node.js в телеграмме:
    1. вызвать BotFather  и  в нем набрать:          /start
    2. создать нового бота :                                      /newbot
    3. завести имя бота (любое доступное) :          my_project
    4. завести nik_name bota с окончанием bot:    my_project_bot
    5. BotFather присылает token для HTTP API (выделяет красным)
 primerno56789067898789098890cwR9aso
6. создать группу, куда бот будет кидать сообщения,
Вводим /join @ник_бота в созданном чате, потому что бывает,
 что не добавляется в логи запись о приглашении бота в группу.

7. Идем в браузер и в адресной строке вводим:
https://api.telegram.org/botXXXXXXXXXXXXXXXXXXXXXXX/getUpdates
где XXXXXXXXXXXXXXXXXXXXXXX — токен бота,

Получить токен от BotFather : "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
вставить токен в api: 
https://api.telegram.org/botXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/getUpdates
Получить id Chat (для группы он идет с минусом) : "id":-88888888999,
для 1 человека без минуса : "id": 7777777777

{"ok":true,"result":[{"update_id":381802470,
{"id":-NNNNNNNNNN,"title":"GROUP_TESTER","type":"group",
"from":{"id":NNNNNNNNN,"is_bot":false,"first_name":"

установить config.js  для добавленных в группу
{
  "telegram": {
    "token": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
    "chat": "-NNNNNNNNNN"
  }
}

Для упрощения процесса запроса установлен пакет 'request'.

npm i request
