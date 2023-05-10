# python_selflearning
Code to demonstrate how RSA and DH works (Note written in Japanese)

Features
--
 - RSA
   - Encrypt Input and return Encrypted message
   - Decrypt encryped message and return original message
 - DH
   - Creates same key to use out of both's pair of private and public key

Purpose
--
The purpose of this project is to demonstrate how RSA and DH works. The project is designed for personal study purposes and is not intended for production use. The input of RSA is limited to 1000 due to calcalation process.

Disclaimer
--
By downloading and using the code, you assume all risks associate with the software. The project is provded "as is", and the author assumes no liability for any damages or losses that may occur from using this software.


Usage
--
 - RSA

```
# Assign 2 prime numbers as a key
p = 91
q = 83

# Creates RSA object
obj = rsa(p,q)

# Creates a encrypted message
cypher = obj.encyprt(message)

# Decryptes encypted message
msg = obj.decrypt(cypher)
```

 - DH

```
# Generates p and g
dh1 = dh(0,0,0,p1)

# Assign values generated from dh1
dh2 = dh(1,dh1.p,dh1.g,p2)

# Creates sending key
message1 = dh1.remainder(dh1.p,send2,dh1.key)
message2 = dh2.remainder(dh1.p,send1,dh2.key)

# >> It results in 2 same value, which is used as key for encrypting
```
