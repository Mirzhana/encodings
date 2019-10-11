## Unicode - the global standard for supporting all languages of the world
[RU](https://mirzhana.github.io/encodings/index_eng)   [GitHub](https://github.com/Mirzhana/encodings/)

### Before **Unicode**

In computer systems, all information is managed and stored by the processor as a set of digits. Initially, symbols in computer systems were in the form of binary code and occupied 8 bits in the computer's memory. To make the binary code writing easier, a special ASCII encoding was developed for the Latin alphabet, which included 128 characters (uppercase and lowercase letters (A-Z, a-z), numbers (0-9) and technical characters). ASCII encoding was self-sufficient only for English-speaking users and did not cover other languages. Therefore, users began to create their own local encodings.

Along with the new encodings, compatibility problems appeared (the same number could represent different characters in different encodings). With the advent of the Internet, this has led to frequent data corruption during transmission between computers and even programs.



 ASCII| Binary    | Ыньищд
------| ---------| ----
65| 01000001|A
74| 01001010 |J
46| 00101110 |.


### **Unicode**

Global Unicode encoding standard was created to solve the compatibility problems of the encoding and extenssions of the symbols used.

Unicode provides each character with a unique sequence of digits (bits) regardless of language, country, platform and program. Thanks to this standard, today many languages are used on the Internet, users and programmers can create content and information systems in their native languages.

It is important to understand that Unicode is a standard that defines whether a certain character belongs to a specific set of digits. If we talk about ways to store and transmit characters, then this is determined by encodings based on the Unicode standard.

### **Unicode** encodings

Having understood the relevance of using the Unicode standard, programmers discover that there are several popular encoding methods. The most common Unicode-based encoding formats are UTF-8 and UTF-16.

UTF-8 and UTF-16 are distinguished by the number of bytes used in character encoding. The maximum of both formats is up to 4 bytes (for example, to output Emoji). At a minimum, UTF-8 uses 1 byte (for example, to output the letter "O"), while UTF-16 uses 2 bytes at least.

### **UTF-8** and **UTF-16** comparison

_Compatibility with ASCII encoding_
Since ASCII code appeared much earlier than the Unicode standard many data is still encoded using ASCII. As mentioned in the previous section, ASCII encoded characters occupy 8 bits in computer memory, as well as UTF-8. At the same time, UTF-16 will have 8 empty bits when working with ASCII encoding since it is designed for 16 bits minimum.

_Occupied memory_
In standard cases, a file encoded using the UTF-8 format takes two times less computer memory than a file encoded in UTF-16.

_High-order symbols_
Often, some local and not widespread characters take up less memory in UTF-16 encoding than in UTF-8 encoding. That is, in some cases, UTF-8 can allocate 4 bytes per character encoding while UTF-16 allocates a minimum of 2 bytes. For most data and programs using Asian languages and characters, UTF-16 is more efficient.

_Example_

![alt text](https://github.com/Mirzhana/encodings/blob/master/img/example.jpg?raw=true " ")



### **UTF-8** and **UTF-16** comparison table
 ASCII             | UTF-8    | UTF-16
-------------------| ---------| ----
Used memory | 8 bit |16 bit
ASCII compatibility| better | worse
High-order symbols| worse |better



### Internal encoding in different programming languages
 Language             | encoding   
-------------------| ---------
C/C++| UTF-8
C#		|UTF-16
Go	|	UTF-8
Java	|	 UTF-16
JavaScript |	No internal encoding
Kotlin	|	UTF-8
PHP		| ASCII
Python	| Less memory used is choosen
Swift	|	UTF-8


