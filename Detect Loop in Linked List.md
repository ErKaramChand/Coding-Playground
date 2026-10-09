## 01. Detect Loop in Linked List

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/detect-loop-in-linked-list/1)

### Problem Description

**Task:** Given a singly linked list, find if the given linked list contains a loop or not. A loop exists in a linked list if the next pointer of the last node points to any other node in the list (including itself), rather than being null.Note: Internally, pos(1 based index) is used to denote the position of the node that tail's next pointer is connected to. If pos = 0, it means the last node points to null. Note that pos is not passed as a parameter.Examples:Input: pos = 2, Output: true

#### Examples

##### Example 1

- **Explanation:** There exists a loop as last node is connected back to the first node.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-08-04 21:14:34
- **Status:** Correct
- **Marks:** 4

```cpp
/*
class Node {
   public:
    int data;
    Node *next;

    Node(int x) {
        data = x;
        next = NULL;
    }
} */

class Solution {
  public:
    bool detectLoop(Node* head) {
        // code here
        if(head == NULL || head->next == NULL)
        return false;
        struct Node*slow,*fast;
        slow = head;
        fast = head;
        while(fast && fast->next){
            slow = slow->next;
            fast = fast->next->next;
            if(slow == fast){
                return true;
            }
        }
        return false;

    }
};
```

*Generated on: 10/9/2026, 10:53:53 AM*