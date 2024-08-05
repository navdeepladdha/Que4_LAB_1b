# Que4_LAB_1b
getMin(int dist[], bool visited[])
Description: This function finds the vertex with the minimum distance value that has not been visited yet.

Parameters:
dist[]: Array of distances from the source to each vertex.
visited[]: Array of boolean values indicating whether a vertex has been visited.
Returns: The index of the vertex with the minimum distance value that hasn't been visited.

Details:
It initializes min to INT_MAX and key to 0.
It iterates through all vertices, checking if a vertex is unvisited and if its distance is less than the current minimum.
It updates min and key accordingly and returns the vertex index with the smallest distance.
display(int dist[], int par[])
Description: This function displays the shortest paths and their distances from the source to all other vertices.

Parameters:

dist[]: Array of distances from the source to each vertex.
par[]: Array containing the parent vertices of each vertex in the shortest path tree.
Returns: Nothing.

Details:

For each vertex i, it traces the path from i to the source using the par array and prints the path.
It then prints the distance from the source to vertex i.
dijkstra(int src)
Description: This function implements Dijkstra's algorithm to find the shortest paths from the source vertex to all other vertices in the graph.

Parameters:

src: The source vertex.
Returns: Nothing.

Details:

Initializes par[] and dist[] arrays, and a visited[] array to keep track of visited vertices.
Sets all distances to INT_MAX initially, except the source vertex, which is set to 0.
Sets the parent of the source vertex to -1.
Iterates n-1 times, each time selecting the vertex u with the minimum distance that hasn't been visited.
Marks u as visited.
Updates the distance values of the adjacent vertices of u if a shorter path is found.
Calls display() to print the shortest paths and their distances.
main()
Description: The main function that drives the program. It takes input from the user, initializes the cost matrix, and calls the Dijkstra's algorithm function.

Parameters: None.

Returns: 0 on successful execution.

Details:

Prompts the user to enter the number of vertices n.
Prompts the user to enter the cost matrix, which represents the graph.
Prompts the user to enter the source vertex.
Calls dijkstra(src) to compute and display the shortest paths from the source vertex.
Example Usage
When you run the program, it will prompt you for the number of vertices, the cost matrix, and the source vertex. It will then calculate and display the shortest paths and distances from the source to all other vertices using Dijkstra's algorithm
