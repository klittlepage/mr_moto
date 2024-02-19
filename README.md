# Dear Mr. Moto Cipher Challenge

## Challenge

On February 18th, 2024, The Office of Mr. Moto presented Ezily and I with a
business card containing the following cipher text:

```text
0010
1011
1000
1011
10
0110
0011
1
1101

Et Tu, Brute?
```

![Mr. Moto Menu][mr_moto_menu]

![Mr. Moto Business Card][business_card]

## Solution Attempts

Et Tu, Brute is an obvious reference to Cesar, implying the use of a Cesar
cipher. I initially interpreted the cipher text as binary digits indexing
the letters of the alphabet. However, trying every possible Cesar cipher shift
proved fruitless. My next attempt noted that `Et Tu, Brute?` contained the same
number of characters (9) as there were binary digits. This prompted me to
experiment with Vigenère cipher variants in which `ettubrute` was the key or
the ciphertext. This also proved fruitless.

## Solution

It subsequently occurred to me that the 0s and 1s might not be binary and that
Morse code was another contender. Treating `0` as a dash (`-`) and `1` as a dot
(`.`) produced valid Morse (the inverse did not). Brute forcing all possible
Cesar cipher shifts produced one plausible candidate: `tomodachi`. Googling
revealed:

```text
Tomodachi (友達; ともだち; or トモダチ) is a Japanese word meaning "friend(s)"
```

I subsequently discovered [jmdict][jmdict], which contained a reference to
`Tomodachi`, and updated the solution to word split the dictionary using
nltk, automating the solution end-to-end in case Mr. Moto changes his code.
Visiting the [himitsu][himitsu] section of Mr. Moto's site and entering
`TOMODACHI` succeeded.

### Result

As a token of our appreciation, we are happy to provide you with the following
rewards:

1. Access to reservations up to 60 days in advance. Please contact us at
   concierge@dearmrmoto.com for advanced reservations. Standard cancellation
   policies apply.
2. Complimentary glass of sake courtesy of Mr. Moto if you bring the business
   card back on the day of your new reservation.

\*Please note these benefits are non-transferable.

[mr_moto_menu]: ./images/mr_moto_menu.jpg
[business_card]: ./images/mr_moto_business_card.jpg
[jmdict]: https://www.edrdg.org/jmdict/j_jmdict.html
[himitsu]: https://www.dearmrmoto.com/himitsu
