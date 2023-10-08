# Pastry

Introduction

This report offers a summary of the planning and execution of a Python Pastry network 
simulation. A decentralized peer-to-peer overlay network called Pastry is used to efficiently 
route messages in a distributed setting. The implemented code supports the fundamental 
operations of Pastry nodes, including joining and leaving the network, sending and receiving 
messages, updating routing tables, creating neighborhood sets, and creating leaf sets.
Implementation
Explanation of each function is:
1. calculate_distance():This function calculates the "XOR distance" between two 4-bit node IDs. 
In simpler terms, it measures how different two node IDs are by counting the number of 
differing bits.
2. PastryNode class:
This is a constructor for creating a PastryNode object. It initializes a node with a unique ID set 
by user at runtime, an empty routing table, an empty neighborhood set, an empty combined 
leaf set, and records the time when the node joins and leave the network.
3. add_node() This function is use to add a new node in to the Pastry network. It also update
the routing tables in order to keep track of, neighborhood sets, and combined leaf sets of 
existing nodes to include information about the new node.
4. update_leaf_set(): This function updates the combined leaf set of a node by considering the 
distance between the node and all other nodes in the network.
5. display_neighborhood_set():This function displays the neighborhood set of a specific node. 
The neighborhood set contains information about nearby nodes in the network.
6. find_neighbor_with_largest_prefix():This function finds the neighbor in the network that 
shares the largest common prefix with a given target node ID. In simpler terms, it looks for the 
node that is most similar to the target node in terms of their IDs.
7. display_routing_table(): This function displays the routing table of a specific node. The 
routing table is used for efficient message routing within the network.
8. delete_node(): This function removes a node from the network. It updates the routing tables, 
neighborhood sets, and combined leaf sets of other nodes to remove references to the deleted 
node.
9. print_network_routing_tables(network) This function prints the routing tables for all nodes 
in the network. It provides an overview of how each node knows about other nodes in the 
network.
10. calculate_common_prefix_length(): This function calculates the length of the common 
prefix between two node IDs. In simpler terms, it determines how many leading bits two node 
IDs share.
11. display_combined_leaf_set() This function displays the combined leaf set of a specific node. 
The combined leaf set contains information about nodes that are both smaller and larger than 
the node.
12. route_message(): This function simulates the routing of a message from a source node to a 
target node within the Pastry network. It follows specific routing rules based on the IDs of the 
source and target nodes.
The driver code at the end, allows users to interact with the simulated network and perform
basic operations such as, adding and deleting nodes, displaying network information of 
particular node, and routing messages between nodes which implements using if-else 
statements with 9 different options.

Instructions To Compile And Run The Code:

1. Make sure you have installed any python supported IDE or you can use Google colab
notebook.
2. Copy the provided code into that IDE`.
3. Open a terminal or command prompt and navigate to the directory where the Python file is 
located/or simply run the code in google colab.
5. Follow the on-screen menu to play with the different options. You can add nodes, delete 
nodes, display routing tables, neighborhood sets, combined leaf sets, and route messages 
between nodes.
6. Choose option 9 to exit the simulation when you are don
