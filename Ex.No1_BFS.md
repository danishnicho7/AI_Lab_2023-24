# Ex.No: 1  Implementation of Breadth First Search 
### DATE:04/03/2025                                                                            
### REGISTER NUMBER :212222040030
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
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

def bfs(graph, start_node):
    visited = []  
    queue = [] 

    visited.append(start_node)
    queue.append(start_node)

    print("Following is the Breadth-First Search:")

    while queue:
        node = queue.pop(0) 
        print(node, end=" ")

        for neighbour in graph[node]:
            if neighbour not in visited:
                visited.append(neighbour)
                queue.append(neighbour)
bfs(graph, '5')
```

### Output:

![image](https://github.com/user-attachments/assets/0f6bb956-ed91-492e-9f41-670276c649d4)


### Result:
Thus the breadth first search order was found sucessfully.
