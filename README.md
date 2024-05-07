# python_typing_practice

### example
```
import typing

def hello_world(message:typing.Union[str, typing.List[str]]="Hello world!"):
    if isinstance(message, str):
        print(message)
    elif isinstance(message, list):
        for sentence in message:
            print(sentence)
    else:
        raise TypeError('The type of message parameter should be str or List[str], \
                        found:',type(message))
```
from python 3.10, it is possible to use " | " instead of typing.Union :
```
...

def hello_world(message:str|typing.List[str]="Hello world!"):

...
```
