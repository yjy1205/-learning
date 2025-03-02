二叉树深度优先搜索（DFS）
class Treenode:
    def __init__(self,value):
        self.value=value
        self.left=None
        self.right=None

#最基础的DFS实现
def simple_dfs(node):
    #出利空节点
    if node is None:
        return 
    
    #首先处理当前节点
    print(f'访问节点：{node.value}')

    #处理左子节点
    simple_dfs(node.left)

    #处理右子节点
    simple_dfs(node.right)


'''
简单的树：（二叉树）图中左支只有左叉，右支只有右叉
       1
      / \
     2   3
    /     \
   4       5
'''

root=Treenode(1)
root.left=Treenode(2)
root.right=Treenode(3)
root.left.left=Treenode(4)
root.right.right=Treenode(5)

print("开始遍历树：")
simple_dfs(root)
