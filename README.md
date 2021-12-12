# Attacks-Splendor

We know that MD5 is a one-way digest algorithm which means that we can't get the original string back once its get hashed/digested. But, can we get back the original string from the md5 hashes.

In this tutorial, we will look at one appraoch to get back the original string after its been hashed using reverse lookup/brute force. 

## So.. how can we decrypt the md5 hashes?
MD5 always generates the same hash key for a given input string.

How can we get around this?

We create a database (mapped) between the original string and the md5 hash key for all possible characters of the desired length of string and their permutations. 

Then, at last, we will have a database of all the possible strings and their relative hashed keys.



| hash_key	| original_string|
|-------- | --------------|
| 02ffa6505a9717c36292cd9bf76972fc	| qwerty@12345  |
| 6d0952a65f2fcf9fa553a8956414e596  |	md5decrypt    |
| f68e2a0caa1d7bc2d30ddcb5db33e9d4	|simplep@ssw0rd |

## How are these hashes broken down in the real world?

Most hashes are broken in the real world using dictionary attacks like John The Ripper and Rainbow Crack.

* John The Ripper is best suited for salted passwords where the attacker knows the salt value.
* Rainbow Crack is good for passwords with small unknown salts and straight hashes like md5($pass).




