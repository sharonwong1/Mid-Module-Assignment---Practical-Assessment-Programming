# Mid-Module-Assignment---Practical-Assessment-Programming

Floyd-warshall - Rewrite Floyd’s algorithm
----

This README includes the introduction, main code of the Floyd Warshall algorithm, implementation of the Floyd Warshall algorithm,etc. 

Contents
----

Introduction

Main code of Floyd Warshall algorithm

Implementation of the Floyd Warshall algorithm 


Introduction
----

Actually, Floyd-Warshall Algorithm is an algorithm to figure out the shortest path between all the pairs of vertices in a graph(weighted graph). The built algorithm is able to work for the directed and undirected weighted graphs and the algorithm does not work for the graphs which has the negative cycles. The negative cycles refers to the sum of the edges in the cycle is a negative number.

Main code of Floyd Warshall algorithm 
----
for k in range(n) :
<br>  for i in range(n) :
<br>    for j in range(n) :
<br>      graph[i][j] = min(graph[i][j], graph[i][k] + graph[k][j])
      

Implementation of the Floyd Warshall algorithm 
----
import sys 

sys.setrecursionlimit(100000000)

#Floyd’s algorithm
<br>def floyd():
<br>n=len(graph)
<br>for k in range(n) :
<br>for i in range(n) :
<br>for j in range(n) :

<br>if graph [i][k] + graph [k][j] < graph [i][j] :
<br>graph [i][j] = graph[i][k] + graph [k][j]
<br>parents [i][j] = parents [k][j] 

<br>#print all the paths 
<br>def print_path (I, j) : 
<br>if i!= j :
<br>print_path(I, parents[i][j])
<br>print(j, end=‘—>’)

Reference 
----
Anon. (n.d) Floyd-Warshall Algorithm. Available at : https://www.programiz.com/dsa/floyd-warshall-algorithm (Accessed 1 Many 2023)
