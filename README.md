# python_DSA_notes
Common data structure and algorithm in python


**DFS recursive traversal in a binary tree**

    class BinaryTree:
        def __init__(self, value):
            self.value = value
            self.left = None
            self.right = None

    def bfs(node):
      if node is None:
        return
        
      if node.left is None and node.right is None:
		# do something

      print(node.value)
      bfs(currNode.left)
      bfs(currNode.right)

Print in-order
<br/>

    def printInorder(root):
        if root:
            printInorder(root.left)
            print(root.val),
            printInorder(root.right)

**Reverse array**

	def reverseArrayInPlace(array):
		start = 0
		end = len(array) - 1
		while start < end:
			array[start], array[end] = array[end], array[start]
			start += 1
			end -= 1
			
**Binary Search (recursive)**

	def binarySearchHelper(array, target, left, right):
		if left > right:
			return -1
		middle = (left + right) // 2
		if target == array[middle]:
			return middle
		elif target < array[middle]:
			return binarySearchHelper(array, target, left, middle - 1)
		else:
			return binarySearchHelper(array, target, middle + 1, right)
			
**Binary Search (iterative)**

	def binarySearchHelper(array, target, left, right):
		while left <= right:
			middle = (left + right) // 2
			if target == array[middle]:
				return middle
			elif target < array[middle]:
				right = middle - 1
			else:
				left = middle + 1
		return -1
		
**Shift array and update one item**

	def shiftAndUpdate(array, num, idx):
		for i in range(idx + 1):
			if i == idx:
				array[i] = num
			else: 
				array[i] = array[i + 1]
	
**Bubble Sort**
```
"""
Traverse from right to left for each iteration, and left bound increments to the right
O(n^2) time | O(1) space
"""

def bubbleSort(array):
	for i in range(len(array)):
		swapped = False
		for j in range(len(array)-1 , i, -1):
			if array[j] < array[j-1]:
				array[j], array[j-1] = array[j-1], array[j]	
				swapped = True			
		if swapped == False:
			break	
	return array
```

```
"""
Iterate from left to right 
Use while loop instead of double for loops
"""

def bubbleSort(array):
	isSorted = False
	counter = 0
	while not isSorted:
		isSorted = True
		for i in range(len(array) - 1 - counter):
			if array[i] > array[i + 1]:
				array[i], array[i+1] = array[i+1], array[i]
				isSorted = False
    	counter += 1
	return array
```

