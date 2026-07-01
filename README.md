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
