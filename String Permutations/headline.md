# String Permutations

## Learning Objective

- Apply recursion to classic permutation problem

## Interviewer Prompt

Given a string, return an array of all the permutations of that string. The permutations of the string should be the same length as the original string (i.e. use each letter in the string exactly once) but do not need to be actual words.

The array that is returned should only contain unique values and its elements should be in alphabetical order.

## Examples

```javascript
stringPermutations("one");
// should return  [ 'eno', 'eon' 'neo', 'noe', 'oen', 'one']
stringPermutations("app");
// should return  [ 'app','pap','ppa']
stringPermutations("nn"); //should return  [ 'nn' ]
```
