# PyShiki
Python lib for working with [shikimori.org](http://shikimori.org/) api

Installing:
```
# Linux:
sudo pip3 install pyshiki

# Windows:
pip3 install pyshiki
```

****

## Examples
```python
import pyshiki
from pprint import pprint

api = pyshiki.Api("YOUR_NICKNAME", "YOUR_PASSWORD")

# GET  http://shikimori.org/api/animes/search?q=Lucky+Star
ls = api.animes("search", q="Lucky Star").get()
pprint(ls)

# POST http://shikimori.org/api/devices
# {
#   "device": {
#     "user_id": 23456813,
#     "token": "test",
#     "platform": "ios",
#     "name": "test"
#   }
# }
dev = api.devices(device={"user_id": 23456813,
                          "token": "test",
                          "platform": "ios",
                          "name": "test"}).post()
pprint(dev)
```

## Changelog
#### v 1.1.3
+ Refactored code
+ Changed license to MIT

#### v 1.1.4
+ Fixed error with api v2 [#1](https://github.com/OlegWock/PyShiki/issues/1)

#### v 1.1.6
+ Fixed error with api v2 (one more) [#2](https://github.com/OlegWock/PyShiki/issues/2)
+ Some license fixes

#### v 1.1.7

+ Fixed stupid bug with _isv2