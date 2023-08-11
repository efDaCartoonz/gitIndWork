# Работа с GitHub по SSH через прокси
Для возможности подключения к GitHub по SSH через прокси без авторизации необходимо установить NCat и в настройках `~/.ssh/config` указать настройки подключения:
```
Host github.com
    HostName github.com
    ServerAliveInterval 55
    ForvardAgent yes
    ProxyCommand ncat --proxy <proxy-address>:<proxy-port> --proxy-type http %h %p
```
---
# Простейший Python скрипт
Скрипт выводит сообщение "Hello World!" и версию Вашего интерпретатора.
__Код скрипта:__
```python
import sys

print("Hello World!")
print("Your Python version: {0}".format(sys.version))
```