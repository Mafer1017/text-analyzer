# Mr. Roboger's Neighborhood

##### By: Marcus Ferreira

#### An Application that analyzes a user inputted sentence and returns information about the sentence.

## Technologies Used

* Javascript
* HTML/CSS
* Bootstrap

## Setup/Installation Requirements

* Clone or download this repository onto your desktop
* Navigate to top-level of directory
* Open index.html in the browser of your choice

## Tests:

Describe: wordCounter()

Test: "It should return 0 for an empty string."
Code: wordCounter("");
Expected Output: 0

Test: "It should return 1 if a passage has just one word."
Code:
const text = "hello";
wordCounter(text);
Expected Output: 1

Test: "It should return 2 if a passage has two words."
Code:
const text = "hello there";
wordCounter(text);
Expected Output: 2

Test: "It should return 0 for a string that is only spaces."
Code: wordCounter("            ");
Expected Output: 0

Test: "It should not count numbers as words."
Code: wordCounter("hi there 77 19");
Expected Output: 2



Describe: numberOfOccurrencesInText()

Test: "It should return 0 occurrences of a word for an empty string."
Code:
const text = "";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return 1 occurrence of a word when the word and the text are the same."
Code:
const text = "red";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 1

Test: "It should return 0 occurrences of a word when the word and the text are different."
Code:
const text = "red";
const word = "blue";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return the number of occurrences of a word."
Code:
const text = "red blue red red red green";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 4

Test: "It should return a word match regardless of case."
Code:
const text = "red RED Red green Green GREEN";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Test: "It should return a word match regardless of punctuation."
Code:
const text = "Red! Red. I like red, green, and yellow.";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Test: "If an empty string is passed in as a word, it should return 0."
Code:
const word = "";
const text = "red RED Red!";
wordCounter(word, text);
Expected Output: 0

Describe: boldPassage()

Test: "It should return a non-matching word in a p tag."
Code:
const word = "hello";
const text = "yo";
boldPassage(word, text);
Expected Output: "<p>yo</p>"

Test: "It should return a matching word in a b tag."
Code:
const word = "hello";
const text = "hello";
boldPassage(word, text);
Expected Output: "<p><b>hello</b></p>"

Test: "It should wrap words that match in `b` tags but not words that don't."
Code:
const word = "hello";
const text = "hello there";
boldPassage(word, text);
Expected Output: "<p><b>hello</b> there</p>"

#### Describe: beepBoop()

- Test: "It should return an array of numbers from 0 to the user's inputted number.
- Code: beepBoop(5)
- Expected Output: [0, 1, 2, 3, 4, 5]
---
#### Describe: changeValue()

- Test: "It should substitute the number 1 with the phrase "Beep!"
- Code: changeValue(myArray)
- Const myArray = beepBoop(5)
- Expected Output: [0, "Beep!", 2, 3, 4, 5]
---
- Test: "It should substitute the number 2 with the phrase "Boop!"
- Code: changeValue(array)
-Expected Output: [0, "Beep!", "Boop!", 3, 4, 5]
---
- Test: "It should substitute the number 3 with the phrase "Won't you be my neighbor?"
- Code: changeValue(myArray)
- Const myArray = beepBoop(5)
- Expected Output: [0, "Beep!", "Boop!", "Won't you be my neighbor?", 4, 5]
---
- Test: "It should prioritize replacing numbers with phrases following a hierarchy of substitutions. The substitution for the number 1 should apply unless there's a 2 or 3 present in the number. Then, the substitution for the number 2 should apply unless there's a 3 present in the number.
- Code: changeValue(myArray)
- Const: myArray = beepBoop(20)
- Expected Output: [0, 'Beep!', 'Boop!', "Won't you be my neighbor?", 4, 5, 6, 7, 8, 9, 'Beep!', 'Beep!', 'Boop!', "Won't you be my neighbor?", 'Beep!', 'Beep!', 'Beep!', 'Beep!', 'Beep!', 'Beep!', 'Boop!']
---

## License

[MIT](https://opensource.org/licenses/MIT)


Copyright (c) 2021 Marcus Ferreira