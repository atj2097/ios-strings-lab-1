# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String) 
```swift 
var range = 1...10
for num in range {
    print(String(num))
```
***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.
```swift 
var range = 5...51
for num in range  {
if num%2 == 0 {
print(String(num))
}
else {
print(" ")
}
}


```
***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.
```swift 
var endsInFour = " "
for i in 1...60 {
if i%10 == 4 {
endsInFour += String(i) + " "
}
}
print(endsInFour)



```
***
## Question 4

Print each character in the string `"Hello world!"`
```swift 
var str = "Hello, playground"
for letter in str {
print(letter)

}



```
***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"` 
```swift 

let myStringSeven = "Hello world!"
print(myStringSeven.last)
```

***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

```swift 
var name = "Adam"
if name.count%2 == 0 {
   for i in name {
       if name.count%2 == 0  {
           print(i)
        }
       else if name.count%2 != 0 {
           for a in name {
                print(name.firstIndex(of: a) ?? 0 + 2)
           }       }
   }
}


```




***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it. 
```swift 
var emptyString = String()
var randomCharacter = "a"
print(Character(randomCharacter) == Character("a"))



```

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent. 
```swift 
let precomposed = "\{uC1}"
let decomposed = "\{u41}\{uB4}"
let eAcute: Character = "\u{E9}"                         // é
let combinedEAcute: Character = "\u{65}\u{301}"          // e followed by
if eAcute == combinedEAcute {
print("these two are the same \(eAcute) = \(combinedEAcute)")
}

let specialO: Character = "\u{D3}"
let decomposedSpecialO: Character = "\u{4F}\u{301}"
if specialO == decomposedSpecialO {
print("these two are the same \(specialO) = \(decomposedSpecialO)")
}

let specialU = "\u{DC}"
let decomposedSpecialU = "\u{55}\u{A8}"

let specialY = "\u{DD}"
let decomposedSpecialY = "\u{59}\u{301}"
if specialY == decomposedSpecialY {
print("these two are the same \(specialY) = \(decomposedSpecialY)")
}

let specialA = "\u{C5} "
let decomposedSpecialA = "\u{41}\u{BA} "



```

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"` 
```swift 
let helloWorldUnicode = "\u{48}\u{45}\u{4C}\u{4C}\u{4F}" + " " + "\u{57}\u{4F}\u{52}\u{4C}\u{44} "


```

***
## Question 10

**Using only Unicode**, print out your name. 
```swift 
let myName = "Adam"
let myUnicodeName = "\u{41}\u{64}\u{61}\u{6D}"
```

***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.
```swift 
let holaMundo = "\u{48}\u{4F}\u{4C}\u{C1}" + " " + "\u{4D}\u{55}\u{4E}\u{44}\u{4F}"
print(holaMundo)

```
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
``` 

```swift 
//White chess
var king = "\u{2654}"
var queen = "\u{2655}"
var rook = "\u{2656} "
var bishop = "\u{2657}"
var knight = "\u{2658} "
var pawn = "\u{2659} "
//Black chess
var kingBlack = "\u{265A} "
var queenBlack = "\u{265B} "
var rookBlack = "\u{265C}"
var bishopBlack = "\u{265D} "
var knightBlack = "\u{265E} "
var pawnBlack = "\u{265F} "

print(rook, knight,  bishop,  king , queen ,  bishop , knight,  rook)
print(pawn , pawn , pawn , pawn , pawn , pawn , pawn )
print(separator: " ")
print(pawnBlack, pawnBlack, pawnBlack, pawnBlack, pawnBlack, pawnBlack, pawnBlack)
print(rookBlack, knightBlack, bishopBlack, kingBlack, queenBlack, bishopBlack, knightBlack, rookBlack)
13
var aString = "JAGGED EDGE"
print("Prior string is \(aString)")
var newString = aString.replacingOccurrences(of: "E", with: "*")

print("New string is \(newString)")

```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
print(aString)
var reverse = String(aString.reversed())
print("\(reverse)")

```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"
var reverse = String(aString.reversed())
if aString == reverse {
print("this is a pallindrome")
}
else {
print("not a pallindrome")
}

```
***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"
for i in problem {
print(i , terminator: " ")
}

```


Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem: String = "find the longest word in the problem description"
var problemArr = problem.components(separatedBy: " ")
var maxWord: String = ""

for word in problemArr {
//maxWordCount += 1
if word.count > maxWord.count {
maxWord = word
}

}

```



***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
let tuple: Int = (a:vowels.count, b:consonants.count )

```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

***
