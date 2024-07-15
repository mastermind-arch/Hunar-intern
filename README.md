# Password Strength Checker

This is a simple Python tool that checks the strength of a password. It analyzes passwords and determines if they are weak, okay, or strong.

## Features
- Checks for password length
- Checks for the presence of lowercase and uppercase letters
- Checks for the presence of digits
- Checks for the presence of special characters

## Usage

Run the script and enter a password to check its strength.

```python
import re

def check_password_strength(password):
    if len(password) < 8:
        return "Weak"
    elif not re.search("[a-z]", password):
        return "Weak"
    elif not re.search("[A-Z]", password):
        return "Weak"
    elif not re.search("[0-9]", password):
        return "Weak"
    elif not re.search("[_@$]", password):
        return "Weak"
    elif re.search("\s", password):
        return "Weak"
    else:
        return "Strong"

password = input("Enter your password: ")
strength = check_password_strength(password)
print(f"The password is {strength}")



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
