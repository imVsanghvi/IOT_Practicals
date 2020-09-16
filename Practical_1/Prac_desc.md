Done! Congratulations on your new bot. You will find it at t.me/vishal_iotprac_bot. You can now add a description, about section and profile picture for your bot, see /help for a list of commands. By the way, when you've finished creating your cool bot, ping our Bot Support if you want a better username for it. Just make sure the bot is fully operational before you do this.

Use this token to access the HTTP API:
1379359043:AAEaONENxpEBh5zWw7PXDsop_GOHbBvOZ4o
Keep your token secure and store it safely, it can be used by anyone to control your bot.

For a description of the Bot API, see this page: https://core.telegram.org/bots/api

python -m pip install telepot

https://api.telegram.org/bot1379359043:AAEaONENxpEBh5zWw7PXDsop_GOHbBvOZ4o/getMe

{"ok":true,"result":{"id":1379359043,"is_bot":true,"first_name":"VISHAL","username":"vishal_iotprac_bot","can_join_groups":true,"can_read_all_group_messages":false,"supports_inline_queries":false}}

https://api.telegram.org/bot1379359043:AAEaONENxpEBh5zWw7PXDsop_GOHbBvOZ4o/getUpdates

{"ok":true,"result":[]}

{"ok":true,"result":[{"update_id":814801778,
"message":{"message_id":25,"from":{"id":1113753715,"is_bot":false,"first_name":"\ud83d\udd75\ud83d\udd0d\ud83d\uddc4\ud83d\udd12\ud83d\udddd\ud83d\udd13\ud83d\uddc3\ud83d\uddc2 \ud83d\udcbb\ud83d\udcc7\ud83d\udcc2\ud83d\udcc1\ud83d\udcd1\u2709\ud83d\udce5\ud83d\udce8\ud83d\udce6\ud83d\udcee\ud83d\udceb\ud83d\udcea\ud83d\udcec\ud83d\udced\u2622\u2623\ud83d\udc64","language_code":"en"},"chat":{"id":1113753715,"first_name":"\ud83d\udd75\ud83d\udd0d\ud83d\uddc4\ud83d\udd12\ud83d\udddd\ud83d\udd13\ud83d\uddc3\ud83d\uddc2 \ud83d\udcbb\ud83d\udcc7\ud83d\udcc2\ud83d\udcc1\ud83d\udcd1\u2709\ud83d\udce5\ud83d\udce8\ud83d\udce6\ud83d\udcee\ud83d\udceb\ud83d\udcea\ud83d\udcec\ud83d\udced\u2622\u2623\ud83d\udc64","type":"private"},"date":1600252742,"text":"Hello!"}}]}

https://api.telegram.org/bot1379359043:AAEaONENxpEBh5zWw7PXDsop_GOHbBvOZ4o/sendMessage?chat_id=1113753715&text=WeLoveIoT

{"ok":true,"result":{"message_id":26,"from":{"id":1379359043,"is_bot":true,"first_name":"VISHAL","username":"vishal_iotprac_bot"},"chat":{"id":1113753715,"first_name":"\ud83d\udd75\ud83d\udd0d\ud83d\uddc4\ud83d\udd12\ud83d\udddd\ud83d\udd13\ud83d\uddc3\ud83d\uddc2 \ud83d\udcbb\ud83d\udcc7\ud83d\udcc2\ud83d\udcc1\ud83d\udcd1\u2709\ud83d\udce5\ud83d\udce8\ud83d\udce6\ud83d\udcee\ud83d\udceb\ud83d\udcea\ud83d\udcec\ud83d\udced\u2622\u2623\ud83d\udc64","type":"private"},"date":1600252796,"text":"WeLoveIoT"}}

import telepot
token = '1379359043:AAEaONENxpEBh5zWw7PXDsop_GOHbBvOZ4o'
TelegramBot = telepot.Bot(token)
print(TelegramBot.getMe())
def handle(msg):
    content_type, chat_type, chat_id = telepot.glance(msg)
    print(content_type, chat_type, chat_id)

    if content_type == 'text':
        TelegramBot.sendMessage(chat_id, "You said '{}'".format(msg["text"]))


TelegramBot.message_loop(handle)

>>> 
= RESTART: C:\Users\Kalpesh\Desktop\Vishal\B.Sc. IT\SEMESTER 5\Internet of Things\PRACTICALS\1.py
{'id': 1379359043, 'is_bot': True, 'first_name': 'VISHAL', 'username': 'vishal_iotprac_bot', 'can_join_groups': True, 'can_read_all_group_messages': False, 'supports_inline_queries': False}
>>> text private 1113753715
