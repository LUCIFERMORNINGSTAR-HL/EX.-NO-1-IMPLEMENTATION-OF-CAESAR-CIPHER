# EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```PYTHON
def encrypt(text, shift):
    result = ""
    for ch in text:
        if ch.isalpha():
            base = ord('A') if ch.isupper() else ord('a')
            result += chr((ord(ch) - base + shift) % 26 + base)
        else:
            result += ch
    return result

def decrypt(text, shift):
    return encrypt(text, -shift)

message = input("Enter message: ")
shift = int(input("Enter shift value: "))

encrypted = encrypt(message, shift)
decrypted = decrypt(encrypted, shift)

print("\nEncrypted:", encrypted)
print("Decrypted:", decrypted)

```
## OUTPUT:
<img width="409" height="298" alt="image" src="https://github.com/user-attachments/assets/8c1cbfd4-a71d-49d2-8fe0-8b209a3e7725" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
