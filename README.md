import re

def is_allowed_specific_char(string):
    char_re = re.compile(r'[^a-zA-Z0-9]')
    match = char_re.search(string)
    return not bool(match)

print("==== Alphanumeric String Checker ====")
print(is_allowed_specific_char("ABCDEFabcdef123450"))
print(is_allowed_specific_char("*&%@#!}{"))

OUTPUT:
==== Alphanumeric String Checker ====
True
False
