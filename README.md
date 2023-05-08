Download Link: https://assignmentchef.com/product/solved-project-4-graphs
<br>
Your job is to write a class that can load an (undirected) graph from a file. Then, your class should support a number of options, all accessed through a text-driven menu. Let’s list the things you’re going to need to be able to do.

<ol>

 <li><strong>Loading the Graph</strong>: You will need to open the file specified by the user and read in a representation of an undirected graph.</li>

 <li><strong>Display a menu</strong>: Display a menu the user can make choices from. Each choice will either give information about the currently loaded graph or transform it in some way.</li>

 <li><strong>Is Connected</strong>: You will need to determine whether or not the graph is connected.</li>

 <li><strong>Minimum Spanning Tree</strong>: If the graph is connected, you will need to find a minimum spanning tree for the graph and print an error otherwise.</li>

 <li><strong>Shortest Path</strong>: Prompt the user for a node. Then, print the lengths of the shortest paths from that node to all other nodes and the actual paths as well.</li>

</ol>

<h1>Loading the Graph</h1>

When your program starts, you must prompt the user for a graph file. This graph file will start with a number saying the number of nodes in the graph. Then, each line after that will correspond to a

particular node. Each such line will start with a number specifying the number of edges connected to a node. The rest of the line will give a series of pairs of numbers. The first number in the pair gives the number of node that the current node is connected to. The second gives the length of the edge connecting them.

We will use the following graph for many of our examples.

The input file for this graph is as follows

6

2 1 5 5 6

<ul>

 <li>0 5 2 3</li>

 <li>1 3 3 4 5 2</li>

</ul>

2 2 4 4 5

<ul>

 <li>3 5 5 7</li>

 <li>0 6 2 2 4 7</li>

</ul>

<h1>Display a Menu</h1>

After the graph has been loaded, display a menu the user can make choices from. Each choice will either give information about the currently loaded graph or transform it in some way.

The choices for the menu are:

<ol>

 <li>Is Connected</li>

 <li>Minimum Spanning Tree</li>

 <li>Shortest Path</li>

 <li>Quit</li>

</ol>

The user should be able to pick any sequence of choices repeatedly until finally selecting Quit (4). Sample output for the menu is as follows.

<ol>

 <li>Is Connected</li>

 <li>Minimum Spanning Tree</li>

 <li>Shortest Path</li>

 <li>Quit</li>

</ol>

Make your choice (1 – 4):

<h1>Is Connected</h1>

If the user selects choice 1, you will need to determine whether or not the graph is connected. If the graph is connected, print Graph is connected. Otherwise print Graph is not connected.

Output for the sample graph is as follows.

Graph is connected.

<h1>Minimum Spanning Tree</h1>

If the graph is connected, you will need to find a minimum spanning tree for the graph. Otherwise, print Error: Graph is not connected. Print the MST in the same general format that is used for the graph input file.

The MST for the sample graph is as follows.

Output for the sample graph is as follows.

6

<ul>

 <li>1 5</li>

 <li>0 5 2 3</li>

 <li>1 3 3 4 5 2</li>

</ul>

2 2 4 4 5

1 3 5

1 2 2

<h1>Shortest Path</h1>

Prompt the user for a node. Then, print the lengths of the shortest paths from that node to all other nodes in parentheses. For the starting node, print (0). For unreachable nodes, print (Infinity). After the length of each shortest path, print a tab and then the nodes visited in the path itself, separated by arrows. Note that you will need to keep a back pointer giving the previous node in the path as well as the best distance found so far in order to produce each shortest path.

If a user entered node 0 for this choice, the output for the sample graph would be as follows.

From which node would you like to find the shortest paths (0 – 5): <em>0</em>

0: (0) 0

1: (5) 0 -&gt; 1

2: (8) 0 -&gt; 1 -&gt; 2

3: (12) 0 -&gt; 1 -&gt; 2 -&gt; 3

4: (13) 0 -&gt; 5 -&gt; 4

5: (6) 0 -&gt; 5

<h1>Hints</h1>

Start early. Try to work on the pieces in the order they are given to you.

You are allowed to implement the graph with an adjacency matrix or with adjacency lists. It’s up to you.

Think before you code. 1 minute of design == 10 minutes of coding == 100 minutes of debugging. You may use the Java Collection Framework if you need lists, queues, or stacks. Very little there is likely to help you much. You are (naturally) forbidden from using graph libraries such as JGraph and JGraphT.