# python_DSA_notes

BFS recursive traversal in a binary tree

    class BinaryTree:
        def __init__(self, value):
            self.value = value
            self.left = None
            self.right = None

    def bfs(node):
      if node is None:
        return

      print(node.value)
      bfs(currNode.left)
      bfs(currNode.right)

