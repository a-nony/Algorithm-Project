This is an algorithm in pseudocode that reads a sentence and determine its lenght, number of words and number of vowels.
1. Initialize counters for lenght, words, and vowels to zero.
2. Read in the sentence character by character unitl the end point is reached.
3. For each charater: a. Increment the lenght counter.
                      b. If the character is a vowel(a,e,i,o,u), increament the vowel counter
		      c. If the character has a space, increment the word counter.

4. Increment the word counter one last time to count the last word.
5. Print out the lenght, number of words and number of vowels.

This is the javascript code for it.
//allows input of sentence
let sentence = prompt("Enter a sentence: ");
//initialization of lenght, words and vowels to 0
let length = 0;
let words = 0;
let vowels = 0;
//creating a for loop for the conditions
for(let i = 0; i < sentence.lenght; i++) {
  let char = sentence[i];
  length++;

  if (char.match(/[aeiou]/i)) {  //the match function is used to check wwether the character is a vowel and the i outside the vowel
squared brackets is a modifier that stands for case-sensitive
    vowels++;
  }

  if (char === " ") {
    words++;
  }

  if (char === ".") {
    break;
  }
}

words++;  // Count the last word
console.log("Length: " + length);
console.log("Words: " + words);
console.log("Vowels: " + vowels);
}
