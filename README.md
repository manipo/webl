# webl
Web
From Wikipedia, the free encyclopedia
Jump to navigationJump to search
	Look up Web, web, or webs in Wiktionary, the free dictionary.
Web usually refers to:

Spider web, a silken structure created by the animal
World Wide Web or the Web, an Internet-based hypertext system
Web or WEB may also refer to:

""" program to Delete a Tree """

# Helper function that allocates a new 
# node with the given data and None 
# left and right poers.								 
class newNode: 

	# Construct to create a new node 
	def __init__(self, key): 
		self.data = key 
		self.left = None
		self.right = None

""" This function traverses tree in post order to 
	to delete each and every node of the tree """
def deleteTree( node) : 

	if (node == None): 
		return

	""" first delete both subtrees """
	deleteTree(node.left) 
	deleteTree(node.right) 
	
	""" then delete the node """
	print(" Deleting node:", node.data) 


# Driver Code 
if __name__ == '__main__': 
	root = newNode(1) 
	root.left = newNode(2) 
	root.right = newNode(3) 
	root.left.left = newNode(4) 
	root.left.right = newNode(5) 
	deleteTree(root) 
	root = None

	print("Tree deleted ") 

# This code is contributed by 
# Shubham Singh(SHUBHAMSINGH10) 

