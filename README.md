playfair-cipher
===============

Version:0.1 \n
Function:simple python code implemented Playfair cipher.

Example:
========
Encrypting:
key:PlayfairExample
Message:Hide the gold in the tree stump
>BMODZBXDNABEKUDMUIXMMOUVIF

Decrypting:
Key:PlayfairExample
Cipher:BMODZBXDNABEKUDMUIXMMOUVIF
<< hidethegoldinthetreestump

BUG:
====
1)The plaintext after decrypting,will lost original space.So it became hard to read.
2)Unable to recognise punctuation .

Rules: 
======
The Playfair cipher is a manual symmetric encryption technique and was the first literal digraph substitution cipher.The technique encrypts pairs of letters (digraphs), instead of single letters as in the simple substitution cipher and rather more complex Vigenère cipher systems then in use. 

1)If both letters are the same (or only one letter is left), add an "X" after the first letter. Encrypt the new pair and continue. 
2)If the letters appear on the same row of your table, replace them with the letters to their immediate right respectively (wrapping around to the left side of the row if a letter in the original pair was on the right side of the row).
3)If the letters appear on the same column of your table, replace them with the letters immediately below respectively (wrapping around to the top side of the column if a letter in the original pair was on the bottom side of the column).
4)If the letters are not on the same row or column, replace them with the letters on the same row respectively but at the other pair of corners of the rectangle defined by the original pair. The order is important – the first letter of the encrypted pair is the one that lies on the same row as the first letter of the plaintext pair.

Reference:http://en.wikipedia.org/wiki/Playfair_cipher

不足：
a,用I代替J，那么真正出现J的时候就会有错误；//
b,相同字母在第一个字母后添加X，那么真正出现是X的时候会有错误；
c,奇数位在最后添加X，如果本身最后一个就是X，那么也会出现错误；
d,用playfair解密出来的message，没有空格，难以区分出单词与单词；
e,大小写也没有控制好。

#test