# Attacks-Splendor

We know that MD5 is a one-way digest algorithm which means that we can't get the original string back once its get hashed/digested. But, can we get back the original string from the md5 hashes.

In this tutorial, we will look at one appraoch to get back the original string after its been hashed using reverse lookup/brute force. 

## So.. how can we decrypt the md5 hashes?
MD5 always generates the same hash key for a given input string.

How to solve this?

We create a database (mapped) between the original string and the md5 hash key for all possible characters of the desired length of string and their permutations. 

Then, at last, we will have a database of all the possible strings and their relative hashed keys.


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

## How are these hashes broken down in the real world?

Most hashes are broken in the real world using dictionary attacks like John The Ripper and Rainbow Crack.

* John The Ripper is best suited for salted passwords where the attacker knows the salt value.
* Rainbow Crack is good for passwords with small unknown salts and straight hashes like md5($pass).

## What is brute force?

A brute force attack occurs when malicious actors use trial and error to crack passwords, login credentials, and encryption keys.

* It's a simple yet reliable tactic for gaining unauthorized access to individual accounts and organizations’ systems and networks.
* The hacker tries multiple usernames and passwords, often using a computer to test a wide range of combinations, until they find the correct login information.




