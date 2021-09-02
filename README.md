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
    def printInorder(root):
        if root:
            printInorder(root.left)
            print(root.val),
            printInorder(root.right)
