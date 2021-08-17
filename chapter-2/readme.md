# Why algoritms matter

## Ordered Arrays and linear search

- To insert into an ordered array you need to check if an element is less than the next value.
- To insert something into an ordered array your math formular is: N + 2 steps in total.(N being the size of the array)

```javascript
// linear search an array
function linearSearch(array, element) {
	for (let i = 0; i < array.length; i++) {
		if (array[i] === element) {
			return i;
		} else if (array[i] > element) {
			break;
		}
		return -1;
	}
}
```

Test an array and an element, if an element is in an array return it or else if the next element is greater than the element passed in break the loop.

If nothing is found then return -1.

Linear can take less steps in an ordered array than in a non ordered array.

## Binary search and ordered arrays

- Binary search halfs arrays and then checks if the element is in that half.
- Binary search will only work in an ordered array.

```javascript
function binarySearch(array, element) {
	let lowerBound = 0;
	let upperBound = array.length - 1;

	while (lowerBound <= upperBound) {
		let middle = Math.floor((lowerBound + upperBound) / 2);
		let valueAtMiddle = array[middle];

		if (valueAtMiddle === element) {
			return middle;
		} else if (element < valueAtMiddle) {
			upperBound = middle - 1;
		} else if (element > valueAtMiddle) {
			lowerBound = middle + 1;
		}
	}
	return -1;
}
```

We search the array and is in the middle we return and thats the end of that search.

If not we look dead in the middle and see if the element is less than the middle element, if it is then we search the left half, if it is greater than the middle element we search the right half.

Linear search will take 100 steps in an array of 100 elements.

Binary search will take 7 steps in an array of 100 elements.

## Questions

- How many steps would it take to perform a linear search for the number 8 in the ordered array, [2,4,6,8,10,12,13]; **4 Steps**
- How many steps would binary search take in the previous example? **1 Step**
- What is the maximum number of steps it would take to perform a binary search on an array of 100 000 elements? **We divide this by 2 each time worst case scenario is 16 times with a remainder on 1.53**
