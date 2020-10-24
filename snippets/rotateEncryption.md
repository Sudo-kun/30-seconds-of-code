---
title: rotateEncryption
tags: string,encryption,intermediate
---

Rotates the given imput a with the given amount.

- It rotates the given string (only letters) with the given amount.
- It checks if the char given is a letter and rotates shifts the char with the given amount,
- when the new char ist not a letter anymore it starts from the beginning
 

```js
const rotateEnctryption = (input, amount = 13) => {
  input = [...input];
  input.forEach((letter, index) => {
	if(letter.match(/[a-z]/)) {
    	input[index] = String.fromCharCode(((letter.charCodeAt() - 'a'.charCodeAt() + amount)%26)+'a'.charCodeAt());
    }
    else if(letter.match(/[A-Z]/)) {
    	input[index] = String.fromCharCode(((letter.charCodeAt() - 'A'.charCodeAt() + amount)%26)+'A'.charCodeAt());
    }
  })
  
  return(input.join(''));
}
```

```js
rotateEncryption("test TEST 1234");
```
