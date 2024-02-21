# SimpleEncode
[?] A simple library for encode, decode and hash data.

## Installation

[Python](https://python.org) require 3.6+

install SimpleEncode libary:
```sh
pip install SimpleEncode
```

## Examples
### Encode and decode string and dict:
```python
from SimpleEncode import SimpleEncode as SE

str_encoded = SE.Encode("hello world!").b64_str()
print(str_encoded) # aGVsbG8gd29ybGQh
str_decoded = SE.Decode(str_encoded).b64_str()
print(str_decoded) # hello world!
```
example use b64_dict:
```python
from SimpleEncode import SimpleEncode as SE

mydict = dict(hello_content="hello", username="world", use_important=True, important_suffix="!")

str_encoded = SE.Encode(mydict).b64_dict()
print(str_encoded) # {'hello_content': 'aGVsbG8=', 'username': 'd29ybGQ=', 'use_important': 'VHJ1ZQ==', 'important_suffix': 'IQ=='}
str_decoded = SE.Decode(str_encoded).b64_dict()
print(str_decoded) # {'hello_content': 'hello', 'username': 'world', 'use_important': 'True', 'important_suffix': '!'}

# use b64_dict argument encode keys:

str_encoded = SE.Encode(mydict).b64_dict(encode_keys=True)
print(str_encoded) # {'aGVsbG9fY29udGVudA==': 'aGVsbG8=', 'dXNlcm5hbWU=': 'd29ybGQ=', 'dXNlX2ltcG9ydGFudA==': 'VHJ1ZQ==', 'aW1wb3J0YW50X3N1ZmZpeA==': 'IQ=='}
str_decoded = SE.Decode(str_encoded).b64_dict(encode_keys=True)
print(str_decoded) # {'hello_content': 'hello', 'username': 'world', 'use_important': 'True', 'important_suffix': '!'}
```

#### Documentation for the library: in progress....

##the library will be constantly updated and will be better soon!