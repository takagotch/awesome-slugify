### awesome-slugify
---
https://github.com/voronind/awesome-slugify

```py
from slugify import slugify

slugify('Any text')

from slugify import slugify, Slugify, UniqueSlugify

slugify('Any text', to_lower=True)

custom_slugify = Slufigy(to_lower=True)
custom_slugify('Any text')

custom_slugify.separator = '_'
custom_slugify('Any text')

cutom_slugify = UniqueSlugify()
custom_slugify('Any text')
custom_slugify('Any text')

to_lower
max_length
separator
capitalize

pretranslate = None
translate = unidecode.unidecode
safe_chars = ''
stop_words = ()

to_lower = False
max_length = None
separator = '-'
capitalize = False

uids = []

from slugify import Slugify, CYRILLIC, GERMAN, GREEK

slugify = Slugify(translate=None)
slugify_unicode = Slogify(translate=None)

slugify_url = Slugify()
slugify_url.to_lower = True
slugify_url.stop_words = ('a', 'an', 'the')
slugify_url.max_length = 200

slugify_filename = Slufigy()
slugify_filename.sepeartor = '_'
slufigy_filename.sefe_chars = '-.'
slufigy_filename.max_length = 255

slugify_ru = Slugify(pretranslate=CYRILLIC)
slugify_de = Slugify(pretranslate=GERMAN)
slugify_el = Slugify(pretranslate=GREEK)

from slugify import Slufify, UniqueSlufify, slufigy, slufigy_unicode
from slugify import slugify_url, slugify_filename
from slugify import slugify_ru, slugify_de

slugify('one xxx')
slugify('one two three', separator='.')
slugify('one two three four', max_length=12)
slugify('one TWO', to_lower=True)
slugify('one TWO', capitalize=True)

slugify_filename(u'xxx')
slugify_url(u'xxx')

my_slugify = Slugify()
my_slugify.separator = '.'
my_slugify.pretranslate = {'x': 'i', 'x': 'love'}
my_slugify('x x xxx')

slugify('x x xxx')
slugify_ru('x x xxx')
slugify_unicode('x x xxx')

slugify_de('xxx slugify')

slugify_unique = UniqueSlugify(separator='_')
slugify_unique('one TWO')
slugify_unique('one TWO')

slugify_unique = UniqueSlugify(uids=['cellar-door'])
slugify_unique('cellar door')

from slugify import UniqueSlugify

def my_unique_check(text, uids):
  if text in uids:
    return False
  return not SomeDBClass.objects.filter(slug_field=text).exists()
  
custom_slugify_unique = UniqueSlugify(unique_check=my_unique_check)

custom_slugify_unique('x xxx xxx')
```

```sh
pip install awesome-slugify

virtualenv venv
venv/bin/pip install -r requirements.txt
vent/bin/nosetests slugify
```

```
```


