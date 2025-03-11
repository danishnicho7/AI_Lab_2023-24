# Ex.No: 2  Implementation of Depth First Search
### DATE:04/03/2025                                                                      
### REGISTER NUMBER :212222040030
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:
```
graph = {
    '5': ['3', '7'],
    '3': ['2', '4'],
    '7': ['8'],
    '2': [],
    '4': ['8'],
    '8': []
}

def dfs(graph, node, visited=None):
    if visited is None:
        visited = set()  

    if node not in visited:
        print(node)
        visited.add(node)
        
        for neighbour in graph[node]:
            dfs(graph, neighbour, visited)

print("Following is the Depth-First Search:")
dfs(graph, '5')
```

### Output:

![image](https://github.com/user-attachments/assets/ecc6b336-6256-4734-9b8f-fb6da5102d7a)


### Result:
Thus the depth first search order was found sucessfully.
