# BFSandEditDistance
Implementation of BFS tasks &amp; Edit Distance (Wagner Fischer) in Java

* Problem 1 (BFS) 
The BFS width search in a G graph selects a G top s as a starting point (in our program the top 1 is always selected as a starting point, since there will always be a node numbering starting from 1). The BFS algorithm belongs to the category of graph exploration algorithms and orders the graph in the form of a tree, exploring the peaks of G per level d = 0.1.2…, ie at increasing distance from s. (Level d: the peaks at a distance d from s). It is called against width because the current level d is plotted horizontally and examined top to top to give the next level d + 1. In our program we first read the file and create a list of neighbors, we use a queue to enter the neighboring peaks we are exploring, but also a HashMap <Integer, Boolean> type structure to note which peaks we have visited. The final BFS tree depends on the order of insertion of the adjacent peaks of a peak in the queue, but regardless of the series all BFS trees with the same starting point will have the same peaks at each level. The algorithm visits each peak at most once. 

In BFS we have the following types of acne: 
Acne Tree: that leads to a first-time visitor Acne. 
Acne Horizontal:  that connects two nodes at the same level Acne.
Acne Cross: all the others Acnes.

Complexity: O (m + n), where m is the set of edges and n is the set of vertices / nodes.


* Problem 2 (Edit Distance)
To calculate the minimum cost of aligning two strings known as edit distance, I decided to implement the Wagner-Fischer algorithm as a dynamic programming algorithm as you ask in your pronunciation. You basically rely on this algorithm observation that if we store in a table all the individual corrective distances, ie those between all the prefixes of the first with the second string then in the last element of the table there will be the corrective distance of the two strings. Details regarding the implementation of the algorithm itself are available in the comments of the code as well as the printing is possible. of the table (on the console) if you are uncommenting in series 97-119 of the EditDistance.java class and run the application. It is worth noting that in our implementation we do not have a case-sensitive policy, ie we treat every character, pedestrian or capital, the same, for example, a and A are equal. Still, each string is not limited to 100 characters, ie it has no limit (beyond what java has for Strings) in order to use it to calculate the edit distance between entire texts and in general to have a greater freedom for the user of the application. Finally, we added a little extra function to its appearance the similarity percentage of the two strings (the type that calculates the percentage exists in series 129 of the EditDistance.java class), so that the user understands that the smaller the edit distance, the higher the similarity rate.

Complexity: O (n * m), where n is the length of the first string and m is the length of the second string.
