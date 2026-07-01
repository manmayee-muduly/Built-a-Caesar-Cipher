# Built-a-Caesar-Cipher
<h3>Built a Caesar Cipher , a simple encryption method that shifts letter in the alphabets to encode messages.</h3>
<br>
alphabet = 'abcdefghijklmnopqrstuvwxyz'
shift = 5
shifted_alphabet = alphabet[shift:] + alphabet[:shift]
translation_table = str.maketrans(alphabet, shifted_alphabet)
text = 'hello world'
encrypted_text = text.translate(translation_table)
print(encrypted_text)

# Make the caesar code reusable

def caesar(text, shift):
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    shifted_alphabet = alphabet[shift:] + alphabet[:shift]
    translation_table = str.maketrans(alphabet, shifted_alphabet)
    encrypted_text = text.translate(translation_table)
    print(encrypted_text)

encrypted_text = caesar('freeCodeCamp', 3)

# Output = iuhhCrghCdps
           None

# although the message is encrypted, the uppercase characters have been left untouched. This happens because the translation table does not include uppercase letters.

def caesar(text, shift):
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    shifted_alphabet = alphabet[shift:] + alphabet[:shift]
    translation_table = str.maketrans(alphabet + alphabet.upper(), shifted_alphabet + shifted_alphabet.upper())
    return text.translate(translation_table)

encrypted_text = caesar('freeCodeCamp', 3)
print(encrypted_text)

# Output = iuhhfrghfdps
    
