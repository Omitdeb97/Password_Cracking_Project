# Password_Cracking_Project

# Description
This project demonstrates the use of John the Ripper for cracking hashed passwords.Generated password hashes using openssl and attempt to crack them using wordlist-based methods.

# Tools used
John the Ripper: A password cracking tool that supports multiple hash algorithms.
OpenSSL: Used to generate hashed passwords for cracking.
Linux Terminal: Used for executing commands and interacting with John the Ripper and OpenSSL.
Wordlist: A file containing a list of potential passwords used for cracking the hashes.

# Process of working on this project
1. Generating a Password Hash Using OpenSSL:
used the openssl command to generate a hashed password (MD5 hash) that will be cracked using John the Ripper.
openssl passwd -1 "Deb042387"
Result:
$1$EQ9tLdIJ$uWXopACkXOBziXpbO432b.

2. Creating a Wordlist
A wordlist (mylist.txt) was created that contains potential passwords. This is the list that John the Ripper will attempt to use to crack the password hash.
echo -e "123456\npassword\nadmin\npassword123\nletmein" > mylist.txt

3. Storing the Hash in a File
stored the generated password hash in a text file (password1.txt):
echo "$1$EQ9tLdIJ$uWXopACkXOBziXpbO432b." > password1.txt

4. Cracking the Hash with John the Ripper
used the following command to attempt cracking the password hash:
john --wordlist=mylist1.txt password1.txt --format=md5crypt
this cmd processes the wordlist and attempts to match one of the passwords with the hash.

5. Viewing the Cracked Password
After John the Ripper finishes running, you can see the cracked password:
john --show password1.txt

# Screenshots

# Learning
From this project, I learned the following:

1. The process of how password hashes work and the importance of using strong passwords.
2. How password cracking tools, such as John the Ripper, can attempt to brute-force a password using common wordlists.
3. How to generate password hashes using OpenSSL and how different hashing algorithms work (MD5 in this case).




