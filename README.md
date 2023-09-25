# Dijkstra-Algorithm
Short Description of Solution Method:
We use the Dijkstra algorithm to calculate the shortest path between two nodes of a weighted graph. This
algorithm is described in the following.
1. First, we set the traversed cost for the initial nodes equal to zero, which is quite apparent because there
is no cost to transfer to the node itself.
2. We consider the initial node a “Visited” or traversed node.
3. We add the initial node's cost (zero) to the weights of each edge between this node and its neighbors
to determine traversed cost between them.
4. From the nodes whose cost has been calculated, we choose the node with the lowest cost as the next
node to traverse.
5. Consider the one with the lowest cost specified in the previous step as the current node, and then
calculate the traversal cost to its neighboring nodes.
6. In this step, Compute the cost of traversing adjacent nodes by adding the edge weight between the
current node and its neighbors, and the transition cost to the current node.
7. If a node from a neighboring node from which we calculated a transition cost in previous steps does
not exceed the cost calculated for this vertex in the sixth step, the new value replaces the cost-related
value for that node.
8. we select the node with the lowest traversed cost from all the nodes for which we calculated the
traversed cost and considered it the current node.
9. Follow the above steps until it reaches the destination node.
10. In this step, the list returns to the beginning of the destination and retrieves all the nodes with the
lowest cost.
11. Finally, we invert the nodes list to consider those from the initial to the end nodes in the return output,
giving us the shortest path.
My System Config:
CPU: AMD A4 1.9GHz
RAM: 3.5 GB
It you have static parameter for InitNode and TermNod, the Run Time is 0.0468747615814209 seconds.
You can see the Computation Time with dynamic parameters in the output after running the code.Short Description of Code:
## 1. Create Class Graph: To implement the Dijkstra algorithm, we first create a class called Graph to
define the list of edges of the graph. Inside the class constructor, we should define its
attributes. Edges attribute maintains the edges of corresponding graphs. In Weights attribute with its
empty default value, the pair of nodes coordinates at the beginning and end of the edge is considered the
Key, and the edge’s weight is considered the value. We also define the AddEdg() method in which a list of
graph nodes connected by an edge and their weight is taken from the input. Then the corresponding edges
and their weight are generated and added to the list of graph edges.
## 2. Dijkstra Algorithm: For this method, we have considered three input parameters, the first parameter
is defined to pass the object created from the Graph class to the mentioned method, and the second and
third parameters, respectively, show the initial and end node to pass the values to calculate the shortest
path between them. Inside the Dijkstra () method, we have defined a variable called
the ShortestPaths dictionary to hold the current node as the key and the previous node pair and the
weight of the edge between them as the value. Hence, the initial value of this variable is equal to the
initial node and corresponding value to None and 0. The “CurrentVertex” variable holds the current node,
and the “visited” variable holds the traversed nodes in the graph. We then define a while loop to be
repeated to reach the end node I defined. We have defined a variable called Destinations that holds the
values assigned to the currentVertex key in the edges dictionary. All nodes connected to the current node
through graph edges are assigned to the Destination variable; thus, we access the neighboring nodes of
the current node. We have also defined another variable called weightToCurrentVertex to hold the
weight of the edge between this node and the node traversed from the shortestPaths dictionary. We have
now defined a for loop in which we intend to calculate the route cost from the current node to each
neighboring node (i.e., attributed nodes to the Destinations variable). The calculated cost is then added
to the shortestPaths dictionary if the cost to any of the adjacent nodes has not been calculated yet.
Otherwise, it replaces this cost with path cost to the node if it is smaller than the cost stored
in shortestPaths dictionary. We have considered another variable called nextDestinations of the
dictionary type to select the one with the lowest cost from all the nodes that have not been traversed and
consider it as the current node. Call the predefined function min() to specify the node with the lowest
route cost. We define a list type variable called path to print the shortest path by specified nodes. Finally,
we have a list that goes back to the beginning of the destination and we have retrieved all the nodes with
the lowest cost which leads to this node.
## 3. Calling the algorithm: We create a graph object from the Graph class, open the network data file,
and do some editing to have the desired format.
## 4. Running the program: Finally, by executing the Dijkstra () method on the given graph, the shortest
path between the initialnode and termnode you enter is returned to the output.
## 5. Calculating the Travel time of the Shortest Path: it can achieve the lowest cost between two nodes
of the given graph. The word "cost" in this algorithm means the Travel time of the shortest path.
