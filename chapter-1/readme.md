# Why datastructures matter?

You can end up with 2 versions of the same code you need to find which is better.

```javascript
function printEven() {
	let num = 2;
	while (num <= 100) {
		if (num % 2 === 0) console.log(num);
		num += 1;
	}
}
```

```javascript
function printEven() {
	let num = 2;
	while (num <= 100) {
		console.log(num);
		num += 2;
	}
}
```

You can interact with Data structures in 4 ways

- Read
- Search
- Insert
- Delete

**- When we question how fast an operation takes we dont only question the speed, we questions how many steps it took to complete the task.**

**- Searching an array is more difficult than reading an array**

When you search an array of 5 elements you perform 5 steps to find the element you are looking for if its the last.

We can then say N amount of Elements will be equal to N amount of search steps..

When you insert data into the beginning of an array this will take the most steps because you need to shift each element to the right.

The formula is N + 1 steps for an array of N elements.

**Deletion needs to close the gap in the array for instance if you remove the 3rd item there is a gap in the array and all elements needs to be shifted accordingly so that space can be cleared up in memory**

# Exercises

## For an array of 100 elements, provide the number of steps the following operation would take.

1 Reading - **Would take one step.**
2 Searching for a value not contained in the array - **100 steps.**
3 Insertion at the beginning of the array - **101 steps N + 1**
4 Insertion at the end of the array - **1 step**
5 Deletion from the beginning of the array - **100** N
6 Deletion from the end of the array - **1 step**

## For an array-based set containing 100 elements, provide the number of steps the following operation would take:

1 Reading - **would take one step.**
2 Searching for a value not contained in the array - **100 steps.**
3 Insertion at the beginning of the array - **201 We need to search the array, that would take a 100 steps, after we are done we need to shift all hundred elements by one and then insert the 1st value 201 steps.**
4 Insertion at the end of the array - **101 step N + 1**
5 Deletion from the beginning of the array - **100 removes 1 and shifts 99** N
6 Deletion from the end of the array - **1 step removes the last**

## Normally the search operation in an array looks for the first instance of a given value. But sometimes we may want to look for every instance of a given value. For example, say we want to count how many times the value "apple" is found inside an array. How many steps would it take to find all the "apples" in terms of N

**N will be equal to the amount of times apple appears in the array**
