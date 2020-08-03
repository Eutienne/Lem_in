# Lem_in
A path finding algorithm, where we code a manager of a ant farm.<br>
I did this project with [@evitao](https://github.com/evitao)

## Project

 The goal of this project is to ﬁnd the quickest way to get n ants across the farm.<br>
 In this project it's the you searching for the fastest path, but also for the most paths.<br>
 So you can find a combination to bring the ants on the quickest way from start to end, without being in the same room on the same time. <br>
 (Quickest way means the solution with the least number of lines, respecting the output format requested below)<br>
 
 ## Rules
 
 * At the beginning of the game, all the ants are in the room ##start.
 The goal is to bring them to the room ##end with as few turns as possible. 
 Each room can only contain one ant at a time. (except at ##start and ##end which can contain as many ants as necessary.)
 * At each turn you will only display the ants that moved.
 * At each turn you can move each ant only once and through a tube (the room at the receiving end must be empty).
 * You must to display your results on the standard output in the following format:
 ```
 number_of_ants 
 the_rooms 
 the_links
 
 Lx-y Lz-w Lr-o ...
```
   x, z, r represents the ants’ numbers (going from 1 to number_of_ants) and y, w, o represents the rooms’ names.
### Example:
* Finally, we ask that the algorithm be able to use the best combination of paths according to the number of ants in cases such as the one presented below:
```
    [start] 
    /   | 
  [3]  [1]--[5] 
  /     |    | 
 [4]--[2]   [6] 
       |   / 
       [end]

By numbers of two ant's you want to use path: "start - 1 - 2 -end"
On this moment are te total instructions 4. 
(it will be the same as you use path "start - 3 - 4 - 2 - end" AND "start - 1 - 5 - 6 - end")
It is nicer to use one path in state (my opinion)
If you got more ants than two, you want to use the paths: 
"start - 3 - 4 - 2 - end" AND "start - 1 - 5 - 6 - end" 
because that will always have less instructions than path "start - 1 - 2 -end"
The question is, how do your algorithem solve this problem?
```

#### Algorithems you can check for this project
^ Breadth-first search (BFS)<br>
^ Depth-first search (DFS)<br>
^ A-star Algorithem (A*)<br>
^ Dijkstra Shortest Path First algorithm (SPF)<br>
^ Dinic's algorithm<br>

## Bonus
We made the following bonusses:<br>
A test script with invalid maps, to check if lem-in gives an error message.<br>
A test script that generates maps with the generator, uses those maps on lem-in and gives a results if you failed or passed<br>
depending on how many lines lem-in used and on Linux it gives the average time your lem-in takes.<br>
A python program that makes an image from the maps lem-in uses, but with random coordinates.<br>

You can read the README's of the bonusses in my other git repositories(named: Tester-lem-in and map_image_lemin).

## Usage
Run the following command:
```
$ make
$ ./lem-in < [filename]
```
