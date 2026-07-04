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

# To print the encrypted code having only the positive and integer between 1 and 25.

def caesar(text, shift):

    if not isinstance(shift, int):
        return 'Shift must be an integer value.'

    if shift < 1 or shift > 25:
        return 'Shift must be an integer between 1 and 25.'

    alphabet = 'abcdefghijklmnopqrstuvwxyz'

    if encrypt != True :
        shift = -shift
        
    shifted_alphabet = alphabet[shift:] + alphabet[:shift]
    translation_table = str.maketrans(alphabet + alphabet.upper(), shifted_alphabet + shifted_alphabet.upper())
    encrypted_text = text.translate(translation_table)
    return encrypted_text
encrypted_text = caesar('freeCodeCamp', 3)
print(encrypted_text) 

# If the function should encrypt the text passed to it (default behavior, encrypt=True), or if it should decrypt an encrypted message.
 Enable the shift to take place in the opposite direction with respect to the encryption process.

 
Declare two functions named encrypt and decrypt, both with text and shift parameters.

You'll use encrypt for the encryption process, and decrypt for the decryption, labeling the two actions with a descriptive name.

def caesar(text, shift, encrypt=True):

    if not isinstance(shift, int):
        return 'Shift must be an integer value.'

    if shift < 1 or shift > 25:
        return 'Shift must be an integer between 1 and 25.'

    alphabet = 'abcdefghijklmnopqrstuvwxyz'

    if not encrypt:
        shift = - shift
    
    shifted_alphabet = alphabet[shift:] + alphabet[:shift]
    translation_table = str.maketrans(alphabet + alphabet.upper(), shifted_alphabet + shifted_alphabet.upper())
    encrypted_text = text.translate(translation_table)
    return encrypted_text

def encrypt(text, shift) :
    return caesar(text, shift)
def decrypt(text, shift) :
    return caesar(text, shift,False)   

encrypted_text = caesar('freeCodeCamp', 3)
print(encrypted_text)
 
