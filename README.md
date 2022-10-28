# fb-chat

# Fix

- In folder where the `fbchat` module is installed `lib/python3.9/site-packages/fbchat/` replace these files:
  - _state.py
  - _util.py
  - _client.py

# Launch

## Main Script
```
from fbchat import Client
from fbchat.models import *

cookies = {}
with open('session.json', 'r') as f:
        cookies = json.load(f)
        
client = Bot("<name>", "<password>", session_cookies=cookies, user_agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/99.0.4844.84 Safari/537.36")

client.listen()
```

## Session.json
Sign into Facebook and paste your cookies here:
```
{
    "datr":"<value>",
    "sb":"<value>",
    "c_user":"<value>",
    "m_pixel_ratio":"1",
    "oo":"v1",
    "dpr":"1.25",
    "x-referer":"<value>",
    "xs":"<value>",
    "fr":"<value>",
    "presence":"<value>"
}

```
