## Implement strStr()
Given two strings needle and haystack, return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

Clarification:

What should we return when needle is an empty string? This is a great question to ask during an interview.

For the purpose of this problem, we will return 0 when needle is an empty string. This is consistent to C's strstr() and Java's indexOf().

```
var strStr = function(haystack, needle) {
    // return 0 if empty string
    if (needle == "") {
        return 0;
    }
    // return the index of first occurrence of needle in haystack
    return haystack.indexOf(needle);
};
```

## Remove Element
Given an integer array nums and an integer val, remove all occurrences of val in nums in-place. The relative order of the elements may be changed.

Since it is impossible to change the length of the array in some languages, you must instead have the result be placed in the first part of the array nums. More formally, if there are k elements after removing the duplicates, then the first k elements of nums should hold the final result. It does not matter what you leave beyond the first k elements.

Return k after placing the final result in the first k slots of nums.

Do not allocate extra space for another array. You must do this by modifying the input array in-place with O(1) extra memory.

```
var removeElement = function(nums, val) {
    // create k variable and have it equal a int
    let k = 0;
    for (let i = 0; i < nums.length; i++) {
        // If the current number is different from val, assign it to index k 
        if (nums[i] !== val) {
            nums[k] = nums[i];
            // move to next index
            k++;
        }
    }
    // return k
    return k
};
```

## Length of Last Word
Given a string s consisting of words and spaces, return the length of the last word in the string.

A word is a maximal substring consisting of non-space characters only.

```
var lengthOfLastWord = function(s) {
    let wordLength = 0;
    let count = 0;
    for (let i = 0; i < s.length; i++) {
        if (s[i] === " ") 
        count = 0
        else
        count++
        if (count > 0) 
        wordLength = count
    }
    return wordLength;
};
```