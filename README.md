# JavaScript-Coding-Test
**JavaScript Interview Coding Test Questions and Answers.**
**1. Write a function that returns the reverse of a string?
2. Write a function that returns the longest word in the sentence?
3. Write a function that checks whether a given string is a palindrome or not>
4. Write a function to remove duplicate elements from an array?
5. Write a function that checks whether two strings are anagram or not?
6. Write a function that returns the number of vowels in a string?
7. Write a function to find the largest number in an array?
8. Write a function to check if a given number is prime or not?
9. Write a function to calculate the factorial of a number?
10.Write a program to remove all whitespace characters from a string?**

**//Write a function that returns the reverse of a string?**
function reverseString(str){
  return str.split("").reverse().join('');
}
console.log(reverseString("Sachin"));

function ReverseByLoop(str){
  let result="";
  for(var i=str.length-1; i>=0; i--){
    result +=str[i];a
  }
  return result;
}
console.log(ReverseByLoop("Sachin"));
=====================

**//Write a function that returns the longest word in the sentence?**

function FindLongestWord(str){
  var sentence = str.split(' ');
  var longWord="";
  
  for(const val of sentence){
    if(val.length > longWord.length) {
      longWord = val;
    }
  }
  
  return longWord;
}

console.log(FindLongestWord("This is my World and I am the king of this universe"));
==================================

**//Write a function that checks whether a given string is a palindrome or not**

function checkPalindrom(str){
  var txt = str.split('').reverse().join('').toLowerCase();
  if(txt== str.toLowerCase()){
    return true;
    } else {
      return false;
    }
}

console.log(checkPalindrom("Jahaj"));

===========================

**//Write a function to remove duplicate elements from an array?**

 function duplicateElm(elm){
  
  var arr=elm;
  var uniqElm=[];
  var count =0;
  
 //1. Approch: 
  //uniqElm = [...new Set(elm)];
  
  //2. Approch:
  //elm.forEach((element)=> {
  //   if(!uniqElm.includes(element)){
  //     uniqElm.push(element);
  //   }
  // })
  
 // 3. Approch:
  for(var i=0; i<elm.length;i++){
    if(!uniqElm.includes(elm[i])){
      uniqElm.push(elm[i]);
    }
  }
    
   return uniqElm;
 
 }
 var elm = [1,2,5,5,3,2,6,7];
 console.log(duplicateElm(elm))

===========================================

**// Write a function that checks whether two strings are anagram or not?**
function checkSameWord(str1, str2){
  var word1 = str1.split('').sort().join('');
  var word2 = str2.split('').sort().join('');
  
  return (word1 === word2) ? "This is anagram string" : "This is not anagram string";
  
}

console.log(checkSameWord("listen", "silent"));

=======================================

**//Write a function that returns the number of vowels in a string?**

function countVowels(str){
  var vowels = ['a','e','i','o','u'];
  var text = str.split('');
  var count=0;
  for(let i of text) {
    for (let v of vowels){
      if(i==v){
         count++;
      }
    }
  }
   return count;
}

console.log(countVowels("love enumorous"));


========================================

**//Write a function to find the largest number in an array?**

function findLargestNum(num){
  var largetNum=0;
  for(let i of num){
    if(i > largetNum) {
      largetNum=i;
    }
  }
  return largetNum;
}

var arr = [1,66,3,54,79,99,1,3,100];
console.log(findLargestNum(arr));

==================================

**//Write a function to check if a given number is prime or not?**

function primeNum(num){
  return (num%2==0) ? num+ " is prime number" : num+ " is not prime number";
}
console.log(primeNum(2));

====================================

**//Write a function to calculate the factorial of a number?**

function calFactor(num){
 
  var result=[];
   for(let i=0; i<num; i++){
    if(num%i==0){
      result.push(i);
    }  
  }
  return result;
  
}

console.log(calFactor(30));

========================================

**///Write a program to remove all whitespace characters from a string?**

function removeWhiteSpace(str){
  //1. Approch whithout trim() method.
  //var result = str.split(' ').join('');
  
  //2. Approch using trim();
  var result = str.trim();
  return result;
}

console.log(removeWhiteSpace(" There are many white space"));


