# password-checking
import re

def is_strong_password(password: str) -> bool:
    if len(password) < 8:
        return False
    if not re.search(r"[A-Z]", password):  # uppercase
        return False
    if not re.search(r"[a-z]", password):  # lowercase
        return False
    if not re.search(r"\d", password):     # digit
        return False
    if not re.search(r"[^\w\s]", password):  # special char
        return False
    return True

# Example usage
pw = "P@ssw0rd!"
print(is_strong_password(pw))  # True or False
