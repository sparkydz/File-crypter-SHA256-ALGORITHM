from hashlib import sha256
input1 = input("entrer le nom de fichier a chiffrer : ")
output1 = input("entrer le nom de fichier output : ")
key = input("entrer le cle : ")

keys = sha256(key.encode('utf-8')).digest()

with open(input1,'rb') as f_input:
  with open(output1,'wb') as f_output:
    i = 0
    while f_input.peek():
      c = ord(f_input.read(1))
      j = i % len(keys)
      b = bytes([c^keys[j]])
      f_output.write(b)
      i = i + 1
