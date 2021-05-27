# Arrays and Strings

- [Arrays and Strings](#arrays-and-strings)
  - [Arrays and Strings](#arrays-and-strings-1)
    - [Is Unique](#is-unique)
      - [Q. Implement an algorithm to determine if a string has all unique characters. What is you cannot use additional data structures?](#q-implement-an-algorithm-to-determine-if-a-string-has-all-unique-characters-what-is-you-cannot-use-additional-data-structures)
    - [Check Permutation](#check-permutation)
      - [Given two strings, write a method to decide if one is a permutation of the other.](#given-two-strings-write-a-method-to-decide-if-one-is-a-permutation-of-the-other)
    - [URLify](#urlify)
      - [Write a method to replace all spaces in a string with '%20'. You may assume that the string has sufficient space at the end to hold the additional characters, and that you are given the 'true' length of the string. (Note: If implementing in Java, please use a character array so that you can perform this operation in place.)](#write-a-method-to-replace-all-spaces-in-a-string-with-20-you-may-assume-that-the-string-has-sufficient-space-at-the-end-to-hold-the-additional-characters-and-that-you-are-given-the-true-length-of-the-string-note-if-implementing-in-java-please-use-a-character-array-so-that-you-can-perform-this-operation-in-place)
    - [Palindrome Permutation](#palindrome-permutation)
      - [Given a string, write a function to check if it is a permutation of a palindrome. A palindrome is a word or phrase that is the same forwards and backwards. A permutation is a rearrangement of letters. The palindrome does not need to be limited to just dicionary words.](#given-a-string-write-a-function-to-check-if-it-is-a-permutation-of-a-palindrome-a-palindrome-is-a-word-or-phrase-that-is-the-same-forwards-and-backwards-a-permutation-is-a-rearrangement-of-letters-the-palindrome-does-not-need-to-be-limited-to-just-dicionary-words)
    - [One Away](#one-away)
      - [There are three types of edits that can be performed on strings: insert a character, remove a character, or replace a character. Given two strings, write a function to check if they are one edit(or zero edits) away.](#there-are-three-types-of-edits-that-can-be-performed-on-strings-insert-a-character-remove-a-character-or-replace-a-character-given-two-strings-write-a-function-to-check-if-they-are-one-editor-zero-edits-away)
    - [String Compression](#string-compression)
      - [Implement a method to perform basic string compression using the counts of repeated characters. For example, the string aabcccccaaa would become a2b1c5a3. If the 'compressed' string would not become smaller than the original string, your method should return the original string. You can assume the string has only uppercase and lowercase letters (a-z)](#implement-a-method-to-perform-basic-string-compression-using-the-counts-of-repeated-characters-for-example-the-string-aabcccccaaa-would-become-a2b1c5a3-if-the-compressed-string-would-not-become-smaller-than-the-original-string-your-method-should-return-the-original-string-you-can-assume-the-string-has-only-uppercase-and-lowercase-letters-a-z)
    - [Rotate Matrix](#rotate-matrix)
      - [Given an image represented by an N\*N matrix, where each pixel in the image is 4 bytes, write a method to rotate the image by 90degs. Can you do this in place?](#given-an-image-represented-by-an-nn-matrix-where-each-pixel-in-the-image-is-4-bytes-write-a-method-to-rotate-the-image-by-90degs-can-you-do-this-in-place)
    - [Zero Matrix](#zero-matrix)
      - [Write an algorithm such that if an element in an M\*N matrix is 0, its entire row and column are set to 0.](#write-an-algorithm-such-that-if-an-element-in-an-mn-matrix-is-0-its-entire-row-and-column-are-set-to-0)
    - [String Rotation](#string-rotation)
      - [Assume you have a method is_substring which checks if one word is a substring of another. Given two strings, s1 and s2, write code to check if s2 is a rotation of s1 using only one call to is_substring (e.g., 'waterbottle' is a rotation of 'erbottlsewat')](#assume-you-have-a-method-is_substring-which-checks-if-one-word-is-a-substring-of-another-given-two-strings-s1-and-s2-write-code-to-check-if-s2-is-a-rotation-of-s1-using-only-one-call-to-is_substring-eg-waterbottle-is-a-rotation-of-erbottlsewat)

## Arrays and Strings

### Is Unique

#### Q. Implement an algorithm to determine if a string has all unique characters. What is you cannot use additional data structures?

<details>

  <summary>Solution</summary>

- we can use an constant space array with a length of 128.
- we iterate through the string and store true in the array at index which is the ascii value of the character.
- next time we find alread a true boolean value at the ascii index of the character, we return false
- Time Complexity is, $O(1)$
- Space Complexity is, $O(1)$

</details>

### Check Permutation

#### Given two strings, write a method to decide if one is a permutation of the other.

<details>

  <summary>Solution</summary>

1. Sorting

   - Time Complexity is, $O(nlogn)$
   - Space Complexity is, $O(1)$

2. Checking frequencies characters of both strings
   - Time Complexity is, $O(n)$
   - Space Complexity is, $O(1)$

</details>

### URLify

#### Write a method to replace all spaces in a string with '%20'. You may assume that the string has sufficient space at the end to hold the additional characters, and that you are given the 'true' length of the string. (Note: If implementing in Java, please use a character array so that you can perform this operation in place.)

<details>

  <summary>Solution</summary>

- The algorithm employs a two-scan approach. In the first scan, we
  count the number of spaces. By tripling this number, we can compute how many extra characters we will
  have in the final string. In the second pass, which is done in reverse order, we actually edit the string. When
  we see a space, we replace it with %20. If there is no space, then we copy the original character.
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

### Palindrome Permutation

#### Given a string, write a function to check if it is a permutation of a palindrome. A palindrome is a word or phrase that is the same forwards and backwards. A permutation is a rearrangement of letters. The palindrome does not need to be limited to just dicionary words.

<details>

  <summary>Solution</summary>

- We can find the frequency of each character in the string. If the length if even, then all frequencies should be even, and if the length is odd then all the frequencies except one shoud be even.
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

### One Away

#### There are three types of edits that can be performed on strings: insert a character, remove a character, or replace a character. Given two strings, write a function to check if they are one edit(or zero edits) away.

<details>

  <summary>Solution</summary>

- We need to check the absolute difference between the lengths of both strings should be <= 1
- implment oneReplaceAway, oneInsertAway, and oneRemoveAway to solve the problem
- Time Complexity is, $O(length of the smaller string)$
- Space Complexity is, $O(1)$

</details>

### String Compression

#### Implement a method to perform basic string compression using the counts of repeated characters. For example, the string aabcccccaaa would become a2b1c5a3. If the 'compressed' string would not become smaller than the original string, your method should return the original string. You can assume the string has only uppercase and lowercase letters (a-z)

<details>

  <summary>Solution</summary>

- Iterate through the array of characters
- check whether the next character is same
- if same find how many characters are there and append it to the new string
- otherwise simply append the character to the new string
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

### Rotate Matrix

#### Given an image represented by an N\*N matrix, where each pixel in the image is 4 bytes, write a method to rotate the image by 90degs. Can you do this in place?

<details>

  <summary>Solution</summary>

- we can achieve it by rotation left -> top, top -> right, right -> bottom, bottom -> left
- we could either use an array which would take an auxiliary space of O(n) or we could swap individual elements which doesn't require any space
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(1)$

* For rotating 90deg clockwise

  - find the transpose of the given matrix
  - reverse every rows of the matrix

* For rotating 90deg anticlockwise

  - find the transpose of the given matrix
  - reverse every column of the matrix

</details>

### Zero Matrix

#### Write an algorithm such that if an element in an M\*N matrix is 0, its entire row and column are set to 0.

<details>

  <summary>Solution</summary>

- we can create row_array and column_array to store the row index and column index where zeroes have been found.
- on the next iteration change the values to zeros taking into account the values stored in row_array and column_array
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n)$

</details>

### String Rotation

#### Assume you have a method is_substring which checks if one word is a substring of another. Given two strings, s1 and s2, write code to check if s2 is a rotation of s1 using only one call to is_substring (e.g., 'waterbottle' is a rotation of 'erbottlsewat')
