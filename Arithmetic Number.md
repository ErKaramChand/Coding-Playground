## 01. Arithmetic Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/arithmetic-number2815/1)

### Problem Description

**Task:** Given three integers 'a' denotes the first term of an arithmetic sequence, 'c' denotes the common difference of an arithmetic sequence and an integer 'b'. you need to tell whether 'b' exists in the arithmetic sequence or not.Examples:Input: a = 1, b = 3, c = 2

#### Examples

##### Example 1

- **Output:**
```text
false
```
- **Explanation:** 2 is not present in the sequence.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(1)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-12 08:21:11
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
	public:
	int inSequence(int a, int b, int c) {
		// code here
		bool flag = false;
		for (int i = 1; i<b; i++) {
			if (b == a + (b - i)*c) {
				flag = true;
				break;
			}
			else {
				flag = false;
			}
		}
		if( flag == false)
		return flag;
	}
};
```

*Generated on: 10/12/2026, 8:21:53 AM*