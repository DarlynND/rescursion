Idea

A word is a palindrome if it reads the same forward and backward.

Algorithm (step by step)

If the word is empty or has one character → palindrome.

Compare the first and last characters:

If they are different → not a palindrome.

If they are the same → repeat the process on the word without the first and last characters.

Continue until a stop condition is reached.

Example (recursive solution in JavaScript)
function isPalindrome(word) {
  if (word.length <= 1) {
    return true;
  }
  if (word[0] !== word[word.length - 1]) {
    return false;
  }
  return isPalindrome(word.slice(1, -1));
}

Examples

gag → true

kayak → true

php → true

hello → false
