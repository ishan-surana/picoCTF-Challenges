***PicoCTF Challenges***

-Ishan Surana

Challenge 1:- **New Caesar**

This was my first challenge ever on picoCTF and I had absolutely no idea what to do even after watching some of the recommended videos. So, I searched on YouTube and found a video that helped me a lot and the link will be attached at the end.

I first downloaded the file and attempted to read through what is happening, and this is where the video helped me a lot. The code is basically taking the string to be encoded and performing operations to it, which are as follows:-

- Take the binary form of the ASCII value of a character uptill 8 digits and split it in 2 halves.
- Take the 2 halves and put the character corresponding to the number (binary→integer→character) side by side. Do this to each character of the string to be encoded.
- When we receive the modified string, shift each of the letter as per key.


**My Code:-**

![](Aspose.Words.826e0a68-e3da-4cde-9494-09340ab456e2.001.png)

**Notes:-**

- Here, the question code had an assert which checked that the key should be a single character only.
- Also, since the 8 digit binary was split into two halves, the sets of 4 would correspond to only 16 characters, hence there was the error prevention assert as well which checked for characters > p character.
- Here, the shift code snippet had part which said key[i] % len[key], but since the length of key should be 1 for code to work and “any number % 1” = 0, there was actually no shift.

The code I created resembles the one from the video because I have only basic knowledge of python commands and I am more proficient in C. But since the C code I would have created would have been huge and very complex as well, I chose to recreate the same python code from the video. I have understood each and every line of the code as I am still learning python, but I may be able to create the code from scratch myself.

**Link to the video:-**

- <https://www.youtube.com/watch?v=UReq8akjTYA>

Challenge 2:- **Caesar**

The challenge is a simple caeser cipher question. The message when opened with a text editor gives picoCTF{gvswwmrkxlivyfmgsrhnrisegl} which appears similar to what the flag should be. But it is not the correct flag, so I used caeser cipher as challenge title hints. I bruteforced all possible combinations using the website dcode.fr/caesar-cipher. The correct combination is crossingtherubicondjneoach, where “crossing the rubicon” is a famous event in Julius-Caesars’ history, where the famous phrase “The die has been cast” was uttered.

![](Aspose.Words.826e0a68-e3da-4cde-9494-09340ab456e2.002.png)
