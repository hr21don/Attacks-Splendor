# Attacks-Splendor

We know that MD5 is a one-way digest algorithm which means that we can't get the original string back once its get hashed/digested. But, can we get back the original string from the md5 hash?

In this tutorial, we will look at a simple approach to get back the original string after its been hashed using reverse lookup/brute force. 

***********
## So how can we decrypt the md5 hashes?
MD5 always generates the same hash key for a given input string.


## Lets start!

We create a database (mapped) between the original string and the md5 hash key for all possible characters of the desired length of string and their permutations. 

Then, at last, we will have a database of all the possible strings and their relative hashed keys.

For instance, consider the table below:

| hash_key	| original_string|
|-------- | --------------|
| 02ffa6505a9717c36292cd9bf76972fc	| qwerty@12345  |
| e48d951cfe51481996d8d464054f0305  |	1qaz2wsx      |
| f68e2a0caa1d7bc2d30ddcb5db33e9d4	| simplep@ssw0rd|
| d214619d0fe4908521715650a9cd515d	| newyork911    |
| bf9fa62a42004ff20576e9af0df2aca4	| g8882684832   |
| caefb5c2bb419fdd69cdfd8d47979c4f  | 1sexgod       |
| 8c32e5048bc4fbfc5dc53c89a36c0812	| ytrewq        |
| babb564668e27ce28f3a3c64e3dc0d0b	| cat01         |
| e00f71ce2f129eff14d93f4fcf2169c5  | dogcat@1920   |
| 2962fa06ab6b807c54f2aeafccf5f67a	| loveme99      |

## Things to try for yourself || Based on the same technique || MD5 decryption Link provided in Resources

So why not use this online md5 decrypting website for the table above and  try decrypt a few hask keys yourself! 

****************************************************************************************************************

## How are these hashes broken down in the real world?

Most hashes are broken in the real world using dictionary attacks like John The Ripper and Rainbow Crack.

* John The Ripper is best suited for salted passwords where the attacker knows the salt value.
* Rainbow Crack is good for passwords with small unknown salts and straight hashes like md5($pass).

## What is brute force?

A brute force attack occurs when malicious actors use trial and error to crack passwords, login credentials, and encryption keys.

* It's a simple yet reliable tactic for gaining unauthorized access to individual accounts and organizations’ systems and networks.
* The hacker tries multiple usernames and passwords, often using a computer to test a wide range of combinations, until they find the correct login information.

## What is Reverse Brute Force

A reverse brute force attack reverses the attack strategy by starting with a known password. 

***********

## Getting Started

Clone repo from my github page

## Run the following commands

```
python Bruteforceattack.py
```

## Paste your md5 here

```
add md5
```

## Hit Enter and Enjoy!

***********

## Testing

In this example, the program executed and successfully returned the password 'new1' within 38s. 

<img width="381" alt="Capture" src="https://user-images.githubusercontent.com/91548582/145726987-3e3da530-f394-4843-b1d7-5562fa32a661.PNG">

***********
## Resources
* MD5Decrypt.net(2021).https://bit.ly/3oOAjVM. Date Accessed: 12/12/21
* SurajKumar(2018).https://webkul.com/blog/decrypting-md5/. Date Accessed:12/12/21  
* Col.Shrapnel(2021).https://web.archive.org/web/20100730040942/https://stackoverflow.com/questions/2768248/is-md5-really-that-bad. Date Accessed: 12/12/21
* Charles R. Severance(2021).https://www.wa4e.com/assn/crack/. Date Accessed:12/12/21
