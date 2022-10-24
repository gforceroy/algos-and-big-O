#### #1: `O(n)`

```javascript
function wordOccurrence(word, phrase){
  let result = 0
  const array  = phrase.split(' ')
  for(let i = 0; i < array.length; i++){
    if(word.toLowerCase() === array[i].toLowerCase()){
      result++;
    }
  }
  return result
}
```

#### #2: `O(n^2)`

```javascript
function bubble_sort(list){
  for(let i = 0; i < list.length - 1; i++){
    for(let j  = 0; j < list.length - 2; j++){
      if(list[j+1] < list[j]){
        const temp = list[j];
        list[j] = list[j+1];
        list[j+1] = temp;
      }
    }
  }
  return list;
}
```

#### #3: `O(n)`
```javascript
function factorial(n){
  if(n === 0){
    return 1;
  }else{
    return n * factorial(n-1);
  }
}
```

#### #4: `O(1)`

```javascript
function bobIsFirst(people){
  return people[0] == 'bob'
}
```

#### #5: `O(n)`

```javascript
function isPalindrome(input){
  const stack = [];
  let output = "";
  for(let i = 0; i < input.length; i++){
    stack.push(input[i]);
  }
  while(stack.length){
    output += stack.pop();
  }
  return output == input
}
```

#### #6: `O(n)`
```javascript
function sumOfDivisors(n){
  let result = 0;
  let i = 1;
  while(i < n){
    if( n % i == 0){
      result += i;
    }
    i++;
  }
  return result
}
```

#### #7: `O(n)`
```javascript
function printAllNumbersThenSumPairs(numArray){
  numArray.forEach((num)=>{
    console.log(num);
  });
  numArray.forEach((num, index)=>{
    if(index < numArray.length - 1){
      console.log(num + numArray[index+1])
    }
  });
}
```

#### #8: `O(n)`
```javascript
function isPrime(num){
  if(num == 1 || num == 2){
    return false
  }
  for(let i = 2; i < num - 1; i++){
    if(num % 1 == 0){
      return false
    }
  }
  return true
}
```

#### Note: 
A common mistake for students is describing functions like `isPalindrome()` as `O(2n)`, as they loop over the input twice. However, Big O only describes the growth rate in complexity as the input grows, so even with two `for` loops, complexity still increases in a linear fashion. Big O does not compute how many operations a function will perform — it computes the rate at which it will scale with increasing input. Hence, the correct answer is still `O(n)`.
